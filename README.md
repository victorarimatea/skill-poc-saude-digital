# skill-poc-saude-digital

**Tipo:** Skill (S)
**Versão atual:** v1.0 — 2026-05-28
**Mantenedor:** victorarimatea
**Visibilidade:** Público
**Status:** Ativo

> Skill responsável por elaborar documentos completos de Prova de Conceito (PoC)
> para soluções de saúde digital no padrão institucional da SES-DF/DTD.
> Baseada no caso zero do Marco Regulatório Interno de PoCs em Saúde Digital
> da Secretaria de Estado de Saúde do Distrito Federal.

---

## Arquivos deste repositório

| Arquivo | Função |
|---|---|
| `SKILL.md` | Instrução técnica lida pelo Claude para executar a skill |
| `backlog-versoes.md` | Histórico auditável de todas as versões desta skill |
| `references/poc-saude-digital-referencia.md` | Padrão completo das 11 seções obrigatórias, textos-padrão, diretrizes DOCX e script base |

---

## O que esta skill faz

Quando acionada, conduz o processo completo de elaboração de um documento de PoC:

1. Lê o repositório âncora do ecossistema (`ecossistema-sumario`)
2. Coleta informações sobre a solução (via documento anexado ou entrevista estruturada)
3. Gera o documento DOCX no padrão SES-DF com todas as seções obrigatórias
4. Aplica o protocolo de correção de acentuação antes da entrega
5. Entrega DOCX + PDF com indicação de campos em aberto e deliberações pendentes

---

## Estrutura do documento gerado

Todo documento de PoC produzido por esta skill contém:

- Capa com tabela de identificação institucional
- 11 seções obrigatórias (Contexto, Objetivos, Escopo, Fluxo Operacional,
  Governança, Cronograma, Métricas, Gestão de Riscos, Aspectos Regulatórios,
  Deliberações Pendentes, Resultado Esperado)
- Seções condicionais: análise de exercício profissional de enfermagem (9.1)
  e instrumentos jurídicos (11.2)
- Formatação institucional: cabeçalho/rodapé, caixas de alerta, tabelas de governança

---

## Como acionar esta skill

Em uma conversa com o Claude que tenha esta skill carregada:

> *"Elabore uma PoC para a solução [nome] da empresa [fornecedor]"*
> *"Preciso criar um documento de PoC para avaliar [solução]"*
> *"Monte a PoC de saúde digital para [contexto]"*

O Claude vai conduzir a coleta de informações e gerar o documento completo.

---

## Contexto institucional

Esta skill faz parte do ecossistema de automação e governança documental
da **Diretoria de Transformação Digital (DTD)** da SETIS/SES-DF,
desenvolvido e mantido por Victor Leonardo Arimatea Queiroz.

Repositório âncora do ecossistema: [ecossistema-sumario](https://github.com/victorarimatea/ecossistema-sumario)

---

## Histórico resumido de versões

| Versão | Data | Descrição |
|---|---|---|
| v1.0 | 2026-05-28 | Criação inicial da skill — baseada na PoC MedNear (caso zero) |
