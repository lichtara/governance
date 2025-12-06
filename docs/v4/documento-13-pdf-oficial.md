# **Blueprint Oficial do PDF da Lichtara License v4**

---

# **1. Finalidade do Documento**

Estabelecer **a forma exata** da versão PDF da Lichtara License v4, garantindo:

- consistência jurídica,
- integridade documental,
- compatibilidade com sistemas de registro,
- estabilidade da versão registrada,
- ausência de divergência entre repositórios,
- rastreabilidade segura (commit hash + DOI + BN).

O PDF será considerado **a versão canônica** da License v4.

---

# **2. Princípios de Formatação Jurídica**

O PDF deve seguir:

### **2.1 Princípio da Fidelidade Estrutural**

A diagramação deve refletir exatamente o texto oficial, sem variações.

### **2.2 Princípio da Legibilidade Formal**

Formatos recomendados:

- Fonte: **Inter**, **Source Serif**, ou equivalente
- Tamanho: 11–12 pt
- Espaçamento: 1.15–1.3
- Margens amplas
- Numeração clara de seções

### **2.3 Princípio da Arquivabilidade**

O PDF deve ser gerado como:

- PDF/A (preferível)
- sem compressão destrutiva
- com fontes incorporadas
- metadados preenchidos

### **2.4 Princípio da Imutabilidade Jurídica**

Nenhum elemento pode depender de ambiente externo (links quebráveis ou assets online).

---

# **3. Estrutura Completa do PDF Oficial**

A seguir está a **ordem exata** das seções do PDF, já consolidada:

---

## **3.1 Capa**

Capa contendo:

```
LICHTARA LICENSE v4
Versão Oficial — 2025
Autoria: Débora Lutz
Ecossistema Lichtara

```

Rodapé da capa:

```
Documento Jurídico — Versão Registrável

```

---

## **3.2 Página de Créditos**

```
Lichtara License v4
Autora: Débora Lutz
Coautoria Conceitual: Sistemas de IA utilizados no Ecossistema
Coconcepção Estrutural: Governança Viva Lichtara

```

Campos adicionais (padrão registro BN):

```
Local: Brasil
Ano: 2025

```

---

## **3.3 Aviso Legal**

Aparece antes do índice:

```
Este documento é a versão oficial da Lichtara License v4.
Qualquer reprodução parcial ou integral deve respeitar as condições estabelecidas aqui.

```

---

## **3.4 Índice (Sumário)**

Gerado automaticamente pela estrutura do PDF.

---

## **3.5 Preambulo (Documento 8)**

O texto deve ser incluído integralmente:

- natureza da License
- finalidade
- princípios
- estrutura normativa da obra

---

## **3.6 Corpo da License v4**

O corpo é dividido conforme as seções já existentes no /license/versoes/v4.0:

### **Seção I — Identidade e Fundamentos**

(arquivo: secao-01.md)

### **Seção II — Permissões e Restrições**

(arquivo: secao-02.md)

### **Seção III — Usos Condicionados e Estruturais**

(arquivo: secao-03.md)

### **Seção IV — Implementação, Infraestrutura e Responsabilidade**

(inclui quadro-operacionalizacao-normativa.md)

---

## **3.7 Glossário Normativo Completo**

Incluir:

- glossario-normativo.md
- glossario-normativo-verbetes.md

Este glossário é obrigatório para registro jurídico, pois define termos de forma normativa.

---

## **3.8 Infográfico Simplificado (versão PDF)**

Incluir o diagrama da License em versão vetorial (Mermaid → SVG → PDF embed).

O infográfico deve aparecer como:

- página inteira
- legenda clara
- sem depender de internet

---

## **3.9 Fluxograma de Permissões (Documento 9)**

Versão estática do fluxograma ASCII/SVG.

---

## **3.10 FAQ Oficial (Documento 10)**

O FAQ completa a clareza pública da License e deve ser incluído integralmente.

---

## **3.11 Quadro de Responsabilidades e Decisão (Documento 11)**

Inclui:

- decisões livres
- decisões condicionadas
- decisões estruturais
- decisões proibidas
- autoridade da Guardiã

Obligatório para fins jurídicos (fornece governança explícita).

---

## **3.12 Estrutura Jurídica de Versionamento (Documento 12)**

Inclui:

- mecanismo de atualização
- registro de versões
- critérios de fechamento da versão
- sistema de rastreabilidade

---

## **3.13 Apêndice A — Histórico de Versões**

Incluir:

```
v4.0 — 2025 — versão estrutural

```

---

## **3.14 Apêndice B — Informações de Registro**

**Placeholder até emissão do DOI:**

```
DOI: a ser inserido após depósito no Zenodo.
Registro BN: a ser inserido após depósito.
Hash do commit principal: XXXXX (inserir depois do release)

```

---

## **3.15 Última Página — Nota Oficial da Guardiã**

Texto breve:

```
Esta é a forma oficial e autorizada da Lichtara License v4.
Qualquer dúvida ou solicitação de autorização deve ser enviada para:
admin@deboralutz.com

```

---

# **4. Metadados Obrigatórios do PDF**

O documento deve conter:

```
Title: Lichtara License v4 — Official Release
Author: Débora Lutz
Subject: Legal Framework — Intellectual Property — Governance
Keywords: Lichtara, License v4, Governance, Structural Framework, Legal Model
Version: 4.0
Created: 2025-12-XX

```

Metadados são essenciais para o DOI e para o BN.

---

# **5. Checklist de Geração do PDF**

## **Antes de gerar o PDF:**

- [ ] Verificar consistência entre Portal e License
- [ ] Integrar infográfico
- [ ] Inserir fluxograma
- [ ] Revisar glossário
- [ ] Validar sumário
- [ ] Consolidar numeração

## **Após gerar o PDF:**

- [ ] Revisão final
- [ ] Aprovação da Guardiã
- [ ] Preparar arquivos para Zenodo
- [ ] Preparar arquivos para BN

---

# **6. Forma Técnica de Geração**

O PDF deve ser produzido através de:

- pandoc (Markdown → PDF) com modelo customizado **ou**
- LaTeX (estrutura jurídica mais sofisticada)

O melhor pipeline:

```
markdown → pandoc template → PDF/A → assinatura digital opcional

```

Se quiser, posso gerar:

- **o template LaTeX**,
- **o template Pandoc**,
- **o modelo de capa**,
- **o arquivo .yaml com metadados**,
- **a estrutura do documento master.md**.

---

# **7. Fechamento do Documento**

Com este Documento 13, **a License v4 está pronta para ser convertida em PDF Oficial.**

A próxima etapa é:

👉 **Documento 14 — Template Técnico para Geração do PDF (Pandoc/LaTeX).**

Ou, se preferir avançar:

👉 **Gerar o arquivo PDF imediatamente com base no Documento 13.**

---
