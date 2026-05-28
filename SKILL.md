---
name: poc-saude-digital
description: >
  Elabora documentos completos de Prova de Conceito (PoC) para soluções de saúde digital
  no padrão institucional da SES-DF (Secretaria de Estado de Saúde do Distrito Federal).
  Use esta skill SEMPRE que Victor — ou qualquer usuário da SES-DF — mencionar qualquer
  variação de: "elaborar PoC", "criar documento de PoC", "prova de conceito de saúde
  digital", "avaliar solução digital na SES", "PoC de SaMD", "PoC de sistema de saúde",
  "montar PoC", "rascunhar PoC", "documento de avaliação de tecnologia SES-DF", ou
  apresentar um briefing/intenção de avaliar uma solução tecnológica em saúde.
  A skill conduz o processo completo: coleta de informações iniciais (por conversa ou
  documento anexado), elabora o documento estruturado no padrão SES-DF com todas as
  seções obrigatórias, e gera o arquivo DOCX final pronto para tramitação via SEI.
  Não espere o usuário pedir explicitamente um "documento Word" — se há intenção de PoC,
  use esta skill e entregue o DOCX.
---

# Skill: Elaboração de PoC em Saúde Digital — Padrão SES-DF

**Versão:** v1.0 — 2026-05-28
**Repositório:** https://github.com/victorarimatea/skill-poc-saude-digital
**Mantenedor:** victorarimatea

Esta skill produz o documento completo de uma Prova de Conceito (PoC) para soluções
de saúde digital no padrão institucional da SES-DF/DTD. O padrão foi desenvolvido e
amadurecido ao longo da elaboração da PoC MedNear (caso zero do Marco Regulatório
Interno de PoCs em Saúde Digital da SES-DF).

O resultado final é um arquivo `.docx` formatado, com cabeçalho/rodapé institucionais,
tabelas de governança, caixas de alerta, análise normativa e minutas jurídicas quando
aplicável.

---

## IDENTIDADE DO ECOSSISTEMA

- **Usuário GitHub:** victorarimatea
- **Repositório âncora:** ecossistema-sumario
- **URL do sumário:** https://raw.githubusercontent.com/victorarimatea/ecossistema-sumario/main/sumario.md
- **URL da nomenclatura:** https://raw.githubusercontent.com/victorarimatea/ecossistema-sumario/main/nomenclatura.md

---

## ETAPA 0 — Leitura do repositório âncora (obrigatória)

Antes de qualquer outra ação, leia o sumário do ecossistema via web_fetch:

```
GET https://raw.githubusercontent.com/victorarimatea/ecossistema-sumario/main/sumario.md
```

Esta etapa garante que a skill opera com o contexto atualizado do ecossistema.
Nunca pule esta etapa, mesmo que o usuário peça urgência.

---

## ETAPA 1 — Coleta de informações

### 1a. Se o usuário fornecer um documento ou briefing inicial

Extraia do material:
- Nome da solução e empresa fornecedora
- Classificação regulatória (SaMD, software de apoio, dispositivo médico etc.)
- Área de aplicação (APS, urgência, especialidade, gestão etc.)
- Problema institucional que a solução pretende endereçar
- Funcionalidades principais declaradas
- Hardware envolvido (se houver)
- Qualquer informação sobre marco regulatório mencionada

Após extrair, apresente um resumo ao usuário e pergunte se há correções antes de prosseguir.

### 1b. Se o usuário apresentar apenas uma intenção verbal

Conduza uma entrevista estruturada com **no máximo 2 perguntas por rodada**, cobrindo:

**Rodada 1 — Solução e problema:**
- Qual é o nome da solução e quem é a empresa?
- Qual problema operacional ou assistencial ela pretende resolver na SES-DF?

**Rodada 2 — Contexto técnico:**
- A solução envolve hardware (equipamentos, kits, dispositivos)? Se sim, quais?
- Há classificação regulatória conhecida (ANVISA, CFM, COFEN)?

**Rodada 3 — Contexto institucional:**
- Em qual área da rede SES-DF seria testada (APS, hospital, urgência)?
- Há alguma preocupação ou limitação conhecida (integração com sistemas, atribuições profissionais, LGPD)?

Não faça todas as perguntas de uma vez. Aguarde as respostas antes de avançar.

---

## ETAPA 2 — Geração do documento

Após coletar as informações necessárias, leia o arquivo de referência completo antes de gerar:

> 📄 **Leia**: `references/poc-saude-digital-referencia.md`
>
> Este arquivo contém: o padrão completo das 11 seções obrigatórias, os textos-padrão
> reutilizáveis, as regras de conteúdo por seção, as diretrizes de formatação DOCX
> e o script base para geração.

---

## ETAPA 3 — Entrega

Gere o DOCX com:
- Nome do arquivo: `POC_[NomeSolucao]_SES-DF_v0.1.docx`
- Versão inicial sempre `0.1` (documento em elaboração)
- Apresente PDF + DOCX

Após entregar, informe ao usuário:
- Quais campos ficaram em aberto (marcados com `[a definir]`) e precisam ser preenchidos
- Quais deliberações pendentes estão listadas na Seção 10
- Se há análise normativa de exercício profissional pendente de validação pela DIENF

---

## Regras gerais

- **Nunca omita seções obrigatórias** — se não houver informação suficiente para uma
  seção, preencha com `[a definir]` e marque como deliberação pendente
- **Tom institucional neutro** — evite atribuir posicionamentos ou questionamentos a
  equipes ou atores específicos; use formulações como "a coordenação da PoC identificou"
- **Análise normativa de enfermagem** — sempre que o fluxo envolver técnico de
  enfermagem operando sistema de apoio clínico, incluir Seção 9.1 com análise preliminar
  e deliberação de validação pela DIENF/COASIS/SAIS
- **Instrumentos jurídicos** — sempre que houver equipamentos emprestados pelo
  fornecedor, listar os três instrumentos na Seção 11.2 e nas Deliberações Pendentes
- **Versão e rodapé** — versão inicial 0.1; rodapé com "Uso Interno | Confidencial"
- **Nota inaugural** — se for a primeira PoC formal da área/unidade, incluir caixa
  azul ao final da Seção 11 registrando o caráter inaugural

---

## REGRA DE ACENTUAÇÃO — DOCUMENTOS EM PORTUGUÊS

Todo documento gerado por esta skill deve passar obrigatoriamente pelo
processo de correção de acentuação antes da entrega. Sem exceção.

### Por que esta regra existe

O pipeline Node.js + docx library + LibreOffice não garante preservação
de acentuação UTF-8 de forma consistente. Palavras acentuadas no código
fonte podem ser corrompidas no ambiente de execução restrito, resultando
em documentos com mistura de palavras acentuadas e não acentuadas —
aspecto incompatível com documentos institucionais.

### Protocolo obrigatório de correção (3 etapas)

**Etapa A — Substituição global no script de geração**

Antes de executar o script, aplicar substituição global. Cobertura mínima:

Substantivos institucionais: gestão, revisão, seção, informação, saúde,
versão, aprovação, análise, transformação, ação, ações, execução,
elaboração, integração, competência, competências, governança, deliberação,
publicação, comunicação, legislação, solicitação, manutenção, atualização,
identificação, consolidação, avaliação, decisão, criação, distribuição,
capacitação, certificação

Adjetivos: estratégico/a/os/as, técnico/a/os/as, específico/a/os/as,
público/a/os/as, básico/a/os/as, crítico/a/os/as, histórico/a/os/as,
obrigatório/a/os/as, próprio/a/os/as, único/a/os/as, próximo/a/os/as

Palavras funcionais: não, também, além, após, há, está, órgão, órgãos,
área, áreas, número, números, índice, índices

Nomes institucionais: Fórum de Subsecretários, Transformação Digital,
Saúde Digital, Secretaria de Estado de Saúde, Instrumento de Análise
Comparativa, Prova de Conceito, Diretoria de Transformação Digital

**Etapa B — Correção individual de títulos de seção**

Verificar e corrigir cada título individualmente após a substituição
global. Títulos usam função separada e frequentemente escapam da
substituição global.

**Etapa C — Verificação automática do DOCX gerado**

Após gerar o DOCX e antes de converter para PDF:

```python
import zipfile, xml.etree.ElementTree as ET
with zipfile.ZipFile("arquivo.docx") as z:
    with z.open("word/document.xml") as f:
        tree = ET.parse(f)
root = tree.getroot()
ns = "{http://schemas.openxmlformats.org/wordprocessingml/2006/main}"
full = " ".join(t.text for t in root.iter(ns+"t") if t.text)
sem_acento = [
    "gestao","revisao","secao","informacao","saude","versao",
    "aprovacao","analise","transformacao","nao ","recomendacao",
    "convergencia","conclusao","indice ","forum ","deliberacao",
    "governanca","competencia","execucao","elaboracao","integracao",
    "publicacao","comunicacao","atualizacao","avaliacao","decisao",
    "prova de conceito","diretoria de transformacao"
]
encontradas = [w for w in sem_acento if w in full.lower()]
if encontradas:
    print(f"ATENCAO — palavras sem acento: {encontradas}")
else:
    print("Verificacao OK — acentuacao correta")
```

Se encontrar palavras sem acento, corrigir com substituição por contexto
e repetir a geração antes de prosseguir.

### Regra de entrega

Nunca entregar documento sem as 3 etapas concluídas.
A conversão para PDF só ocorre após Etapa C confirmar zero ocorrências.
