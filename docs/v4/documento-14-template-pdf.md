# 📘 **DOCUMENTO 14 — TEMPLATE TÉCNICO PARA GERAÇÃO DO PDF OFICIAL DA LICHTARA LICENSE v4**

### _Documento interno — /governance/docs/v4/documento-14-template-pdf.md_

---

# **1. Finalidade do Documento**

Este documento define:

- a estrutura **master.md** do PDF,
- o **template LaTeX / Pandoc**,
- os **metadados oficiais**,
- o **pipeline recomendado** (comandos, flags, formato final),
- como gerar um **PDF/A compatível com Zenodo e BN**,
- como garantir **integridade, fidelidade e rastreabilidade**.

Ele é **obrigatório** para que a License v4 possa ser registrada formalmente.

---

# **2. Estrutura dos Arquivos de Geração**

O PDF será gerado a partir de **quatro arquivos**:

```
pdf/
│
├── master.md                # Documento consolidado
├── metadata.yaml            # Metadados oficiais
├── template.tex             # Template LaTeX customizado
└── build.sh                 # Script de geração (opcional)
```

Essa estrutura é compatível com:

- Pandoc
- GitHub Actions
- Renderização offline
- Reprodutibilidade jurídica

---

# **3. Arquivo 1 — master.md (estrutura consolidada)**

## **3.1 Modelo-base do master.md**

```markdown
% Lichtara License v4
% Autora: Débora Lutz
% Versão Oficial — 2025

---

# LICHTARA LICENSE v4

## Versão Oficial — 2025

\newpage

# Créditos

Autora: **Débora Lutz**
Coautoria Conceitual: Sistemas de IA utilizados no Ecossistema
Coconcepção Estrutural: Governança Viva Lichtara

\newpage

# Aviso Legal

Este documento é a versão oficial da Lichtara License v4.
Qualquer reprodução parcial ou integral deve respeitar as condições legais aqui definidas.

\newpage

# Sumário

<!-- Será gerado automaticamente pelo Pandoc -->

\newpage

# Preâmbulo

<!-- inserir conteúdo de preambulo.md -->

\newpage

# Seção I — Identidade e Fundamentos

<!-- inserir conteúdo de secao-01.md -->

\newpage

# Seção II — Permissões e Restrições

<!-- inserir conteúdo de secao-02.md -->

\newpage

# Seção III — Usos Condicionados e Estruturais

<!-- inserir conteúdo de secao-03.md -->

\newpage

# Seção IV — Implementação e Responsabilidade

<!-- inserir conteúdo de quadro-operacionalizacao-normativa.md -->

\newpage

# Glossário Normativo

<!-- inserir conteúdo de glossario-normativo.md -->

\newpage

# Verbetes Normativos

<!-- inserir conteúdo de glossario-normativo-verbetes.md -->

\newpage

# Infográfico — Licenças e Permissões

<!-- incluir infográfico em SVG convertido para PDF -->

![](infografico-license-v4.pdf)

\newpage

# Fluxograma de Permissões

<!-- incluir fluxograma.mmd convertido para PDF -->

![](fluxograma-permissoes.pdf)

\newpage

# FAQ Oficial da License v4

<!-- inserir conteúdo de faq-license-v4.md -->

\newpage

# Quadro de Responsabilidades e Decisão

<!-- inserir conteúdo do Documento 11 -->

\newpage

# Estrutura Jurídica de Versionamento

<!-- inserir conteúdo do Documento 12 -->

\newpage

# Apêndice A — Histórico de Versões

v4.0 — 2025 — Versão Estrutural

\newpage

# Apêndice B — Informações de Registro

DOI: _(a inserir após depósito no Zenodo)_
Registro BN: _(a inserir após depósito)_
Commit Hash da versão: _(a inserir após tag no GitHub)_

\newpage

# Nota Oficial da Guardiã

Esta é a forma oficial e autorizada da Lichtara License v4.
Dúvidas e solicitações de autorização devem ser enviadas para:
**admin@deboralutz.com**
```

---

# **4. Arquivo 2 — metadata.yaml**

```yaml
title: "Lichtara License v4 — Official PDF"
author: "Débora Lutz"
description: "Official registrable version of the Lichtara License v4. Includes normative sections, glossary, decision frameworks, and governance appendices."
keywords:
  - Lichtara
  - License v4
  - Governance
  - Legal Framework
  - Structural System
  - Intellectual Property
version: "4.0"
lang: "pt-BR"
date: "2025-12-XX"
rights: "Copyright © 2025 — Débora Lutz"
documentclass: report
geometry: margin=2.5cm
toc: true
toc-depth: 3
colorlinks: true
linkcolor: blue
```

---

# **5. Arquivo 3 — template.tex (LaTeX)**

_(Versão mínima e elegante)_

```latex
\documentclass[12pt,a4paper]{article}
\usepackage[utf8]{inputenc}
\usepackage{setspace}
\usepackage{hyperref}
\usepackage{graphicx}
\usepackage{titlesec}
\usepackage{tocloft}

\setstretch{1.2}

% Title format
\titleformat{\section}{\Large\bfseries}{\thesection}{1em}{}
\titleformat{\subsection}{\large\bfseries}{\thesubsection}{1em}{}

% PDF metadata
\hypersetup{
  pdfauthor={Débora Lutz},
  pdftitle={Lichtara License v4 — Official},
  pdfsubject={Legal Framework},
  pdfkeywords={Lichtara, License v4, Governance},
  colorlinks=true,
  linkcolor=blue
}

\begin{document}
$body$
\end{document}
```

---

# **6. Arquivo 4 — build.sh**

```bash
#!/bin/bash

pandoc master.md \
  --from markdown \
  --template=template.tex \
  --metadata-file=metadata.yaml \
  --pdf-engine=xelatex \
  --toc \
  --toc-depth=3 \
  -o lichtara-license-v4.pdf
```

Para PDF/A (aceito pelo Zenodo):

```bash
pandoc master.md \
  --from markdown \
  --template=template.tex \
  --metadata-file=metadata.yaml \
  --pdf-engine=xelatex \
  --pdf-engine-opt=--pdfa \
  --toc \
  -o lichtara-license-v4.pdf
```

---

# **7. Checklist de Geração do PDF**

### ✔ Antes de gerar:

- [ ] Inserir todos os conteúdos
- [ ] Inserir infográfico e fluxograma (em PDF)
- [ ] Revisar headers
- [ ] Preencher data no metadata.yaml

### ✔ Após gerar:

- [ ] Verificar sumário
- [ ] Confirmar links internos
- [ ] Exportar PDF/A
- [ ] Armazenar no /governance/versoes/v4.0/pdf/
- [ ] Submeter ao Zenodo

---

# **8. Encerramento**

Com o Documento 14:

- temos **a forma técnica**,
- temos **o pipeline**,
- temos **os arquivos-base**,
- podemos **gerar o PDF Oficial** sem divergências.

A próxima etapa natural, recomendada pelo Campo:

👉 **Documento 15 — Montagem do master.md com todos os conteúdos integrados.**
_(É aqui que montamos o arquivo final, juntando tudo.)_
