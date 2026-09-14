# Bíblia Sagrada — Tradução do Pe. Manuel de Matos Soares
### Edição Digital Estruturada e Revisada (Cânon Católico — 73 Livros)

[![Cânon Católico](https://img.shields.io/badge/C%C3%A2non-Cat%C3%B3lico%20(73%20Livros)-blue.svg)](#-cânon-bíblico-integral)
[![Versículos](https://img.shields.io/badge/Vers%C3%ADculos-35.816%20validados-green.svg)](#-integridade-dos-dados)
[![Revisão Textual](https://img.shields.io/badge/Revis%C3%A3o-Corre%C3%A7%C3%B5es%20de%20OCR%20(com%20IA)-orange.svg)](IMPROVEMENTS.md)
[![Repositório](https://img.shields.io/badge/GitHub-bibliacatolica%2Fbiblia-181717?logo=github)](https://github.com/bibliacatolica/biblia)
[![Licença](https://img.shields.io/badge/Licen%C3%A7a-Dom%C3%ADnio%20P%C3%BAblico%20%2F%20CC0-lightgrey.svg)](#-licença-e-créditos)

Este é um projeto pessoal/independente que disponibiliza o texto integral da **Bíblia Sagrada** na tradução do **Padre Manuel de Matos Soares** (1878–1955, traduzida a partir da *Vulgata Latina* com aprovação eclesiástica em 1927/1932) em formato digital estruturado (`JSON`).

O objetivo principal deste repositório é fornecer uma base limpa, organizada e acessível para desenvolvedores, pesquisadores e leitores. O texto base, proveniente de digitalizações públicas na internet, continha diversos artefatos e erros comuns de OCR (reconhecimento óptico de caracteres). Com o auxílio de inteligência artificial e rotinas de automação, foi feito um trabalho de identificação e correção de centenas desses defeitos de digitalização, organizando o conteúdo em um formato pronto para consumo em aplicações.

---

## 📖 Sobre a Tradução do Pe. Manuel de Matos Soares

A tradução das Sagradas Escrituras feita pelo Padre Manuel de Matos Soares é uma das versões católicas mais tradicionais em língua portuguesa. Realizada a partir da **Vulgata Sixto-Clementina** (com consultas aos textos hebraicos e gregos), contou com as seguintes aprovações canônicas de sua época:

* **Nihil Obstat**: Monsenhor Sebastiano Leite de Vasconcellos.
* **Imprimatur**: Dom Manuel, Cardeal Cerejeira, Patriarca de Lisboa (1927 / 1932).

O texto preserva o estilo clássico do português do início do século XX e a ordem e numeração canônica tradicional da Igreja Católica.

---

## 🏛️ Cânon Bíblico Integral (73 Livros)

Esta base contempla os **73 livros canônicos católicos** (incluindo os deuterocanônicos e acréscimos tradicionais de Ester e Daniel), totalizando **1.334 capítulos** e **35.816 versículos**:

- **Antigo Testamento (46 Livros):**
  - *Pentateuco (5):* Gênesis, Êxodo, Levítico, Números, Deuteronômio.
  - *Livros Históricos (16):* Josué, Juízes, Rute, 1 Samuel, 2 Samuel, 1 Reis, 2 Reis, 1 Crônicas, 2 Crônicas, Esdras, Neemias, **Tobias**, **Judite**, Ester (com acréscimos canônicos), **1 Macabeus**, **2 Macabeus**.
  - *Livros Sapienciais (7):* Jó, Salmos (numeração da Vulgata), Provérbios, Eclesiastes, Cântico dos Cânticos, **Sabedoria**, **Eclesiástico (Sirácida)**.
  - *Livros Proféticos (18):* Isaías, Jeremias, Lamentações (com acrósticos hebraicos restaurados), **Baruc** (incluindo a Carta de Jeremias), Ezequiel, Daniel (com seções canônicas de Susana, Bel e o Dragão e Cântico dos Três Jovens), Oseias, Joel, Amós, Abdias, Jonas, Miqueias, Naum, Habacuc, Sofonias, Ageu, Zacarias, Malaquias.
- **Novo Testamento (27 Livros):**
  - *Evangelhos e Atos (5):* São Mateus, São Marcos, São Lucas, São João, Atos dos Apóstolos.
  - *Corpus Paulino (14):* Romanos, 1 Coríntios, 2 Coríntios, Gálatas, Efésios, Filipenses, Colossenses, 1 Tessalonicenses, 2 Tessalonicenses, 1 Timóteo, 2 Timóteo, Tito, Filêmon, Hebreus.
  - *Epístolas Católicas (7):* São Tiago, 1 São Pedro, 2 São Pedro, 1 São João, 2 São João, 3 São João, São Judas.
  - *Profecia (1):* Apocalipse de São João.

*(Em negrito, os livros deuterocanônicos e seções tradicionais presentes no cânon católico).*

---

## 🔍 Revisão Textual e Correções de OCR (com auxílio de IA)

As fontes digitalizadas disponíveis na web contavam com diversos artefatos mecânicos gerados pelo processo de escaneamento e OCR de impressões antigas. Utilizando scripts em Node.js e assistência de modelos de linguagem (IA), foram revisados e ajustados diversos pontos, tais como:

1. **Troca do 'I' Maiúsculo por 'l' Minúsculo em Pronomes:**
   - Correção sistemática em pronomes enclíticos e mesoclíticos onde o OCR confundiu a letra `l` com `I` (`-Ihe` $\rightarrow$ `-lhe`, `-Io` $\rightarrow$ `-lo`, `-Ios` $\rightarrow$ `-los`, `-Ia` $\rightarrow$ `-la`, `no-Ios` $\rightarrow$ `no-los`, etc.).
2. **Nomes Próprios e Topônimos:**
   - Ajuste de palavras corrompidas no scan, como `Betel` (que aparecia como `Betei` em várias passagens), `Misac` em Dn 3,12 (que estava `Jlisac`), `Nicópolis` em Tit 3,12 (estava `Nicópoiis`), etc.
3. **Versículos Faltantes e Acrósticos:**
   - Reintegração de versículo que havia ficado de fora na digitalização original (Lm 5,5) e reinserção dos cabeçalhos dos acrósticos hebraicos em Lamentações.
4. **Apóstrofos Arcaicos em Início de Frase:**
   - Ajuste de notações tipográficas antigas como `A’` e `E’` para `À` e `É`.
5. **Notas Editoriais Acidentais e Duplicações:**
   - Expurgo de termos de cabeçalho que entraram no corpo do texto (como a palavra *"introdução,"* em Pv 22,17) e eliminação de palavras repetidas por quebra de linha.
6. **Acentuação e Pontuação:**
   - Correção de acentos que haviam sumido no OCR (`cítara`, `órgão`, `língua`, etc.) e limpeza de pontuações duplas decorrentes de quebras de página.

Para detalhes sobre as alterações realizadas, consulte o arquivo:
👉 **[IMPROVEMENTS.md](IMPROVEMENTS.md)** *(Registro de alterações e revisões)*.

> ⚠️ **Nota de Transparência:** Este trabalho foi feito de forma independente, com assistência de inteligência artificial e scripts de apoio. Embora tenhamos buscado máximo rigor nas correções e validações, erros pontuais ainda podem ocorrer. Caso encontre alguma discrepância em relação ao texto impresso tradicional do Pe. Matos Soares, contribuições e correções via *Issue* ou *Pull Request* são muito bem-vindas!

---

## 📦 Estrutura dos Dados e Schemas JSON

### Arquivo Consolidado: `biblia-matos-soares-completa.json`

O arquivo contém a Bíblia completa em um único objeto JSON estruturado:

```json
{
  "title": "Bíblia Sagrada — Tradução do Pe. Manuel de Matos Soares",
  "translator": "Pe. Manuel de Matos Soares",
  "approval": "Nihil Obstat & Imprimatur (1927/1932)",
  "canon": "Católico Completo (73 livros)",
  "totalBooks": 73,
  "totalChapters": 1334,
  "totalVerses": 35816,
  "books": [
    {
      "id": "GEN",
      "slug": "genesis",
      "name": "Gênesis",
      "abbrev": "Gn",
      "testament": "AT",
      "chaptersCount": 50,
      "versesCount": 1531,
      "chapters": {
        "1": [
          { "number": 1, "text": "No princípio criou Deus o céu e a terra." },
          { "number": 2, "text": "A terra, porém, era informe e vazia..." }
        ]
      }
    }
  ]
}
```

---

## 💻 Exemplos de Consumo da Base

### 1. Python
```python
import json

with open("biblia-matos-soares-completa.json", "r", encoding="utf-8") as f:
    bible = json.load(f)

# Buscar João 3,16
joao = next(b for b in bible["books"] if b["id"] == "JHN")
versiculo = joao["chapters"]["3"][15] # índice 15 = versículo 16
print(f"Jo 3,16: {versiculo['text']}")
```

### 2. Node.js / TypeScript
```typescript
import fs from "fs";

const data = JSON.parse(fs.readFileSync("biblia-matos-soares-completa.json", "utf8"));

// Consultar o Salmo 22 (Sl 23 no cômputo protestante)
const salmos = data.books.find((b: any) => b.id === "PSA");
console.log("Sl 22,1:", salmos.chapters["22"][0].text);
```

### 3. Bash / `jq`
```bash
# Obter o primeiro versículo de Gênesis
jq -r '.books[] | select(.id=="GEN") | .chapters."1"[0].text' biblia-matos-soares-completa.json
```

---

## 🛡️ Integridade dos Dados

O dataset passa por validação computacional rigorosa:
* **Validação de Cânon:** 73 livros presentes e sequenciados de acordo com a Vulgata Latina.
* **Contagem de Versículos:** Exatamente 35.816 versículos estruturados e não vazios.
* **Validação Sintática:** Arquivo JSON 100% em conformidade com a especificação RFC 8259, codificado em UTF-8 estrito.

---

## ⚖️ Licença e Créditos

- **Texto Bíblico:** A tradução do Padre Manuel de Matos Soares data da primeira metade do século XX (1927–1932), encontrando-se em domínio público conforme as legislações vigentes de direitos autorais.
- **Curadoria Digital e Dados:** Esta compilação estruturada, as correções textuais e o aparato crítico de revisão são disponibilizados sob a licença **Creative Commons Zero (CC0 1.0 Universal / Domínio Público)** e **Open Data Commons**, livres para uso pastoral, acadêmico, pessoal ou comercial.
