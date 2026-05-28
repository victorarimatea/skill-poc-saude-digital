# Referência Completa — Padrão de PoC em Saúde Digital SES-DF

## Índice
1. Estrutura obrigatória do documento
2. Padrão de conteúdo por seção
3. Textos-padrão reutilizáveis
4. Diretrizes de formatação DOCX
5. Script base de geração

---

## 1. Estrutura obrigatória do documento

Todo documento de PoC no padrão SES-DF deve conter as seguintes seções,
nesta ordem:

| # | Seção | Obrigatória |
|---|-------|-------------|
| — | Capa com tabela de identificação | Sim |
| — | Sumário | Sim |
| 1 | Contexto e Justificativa | Sim |
| 1.1 | A Solução Avaliada | Sim |
| 2 | Objetivos da PoC | Sim |
| 3 | Escopo e Delimitações | Sim |
| 4 | Cenário Operacional e Fluxo | Sim |
| 5 | Governança e Partes Interessadas | Sim |
| 5.1 | Coordenador da PoC e Ponto Focal SES-DF | Sim |
| 6 | Cronograma Preliminar | Sim |
| 6.1 | Declaração Formal de Encerramento | Sim |
| 7 | Métricas e Critérios de Sucesso | Sim |
| 8 | Gestão de Riscos | Sim |
| 9 | Aspectos Éticos e Regulatórios | Sim |
| 9.1 | Conformidade com Exercício Profissional de Enfermagem | Se aplicável* |
| 10 | Deliberações Pendentes | Sim |
| 11 | Resultado Esperado | Sim |
| 11.1 | Responsáveis pelos Entregáveis e Prazos | Sim |
| 11.2 | Instrumentos Jurídicos Necessários à Execução | Se aplicável** |
| Anexo I | Documentação técnica do fornecedor | Se disponível |

*Incluir sempre que o fluxo envolver técnico de enfermagem operando sistema de apoio clínico.
**Incluir sempre que houver equipamentos de propriedade do fornecedor em uso pela equipe SES-DF.

---

## 2. Padrão de conteúdo por seção

### CAPA

Campos obrigatórios na tabela de identificação:
- Área responsável
- Área assistencial parceira
- Classificação da solução (ex.: SaMD — RDC 657/2022)
- Versão do documento
- Status
- Data de elaboração
- Coordenador da PoC / Ponto focal SES-DF → [a indicar formalmente]
- Ponto focal [Nome do Fornecedor] → [a indicar formalmente]

---

### SEÇÃO 1 — CONTEXTO E JUSTIFICATIVA

Estrutura:
1. Parágrafo de contextualização da área de saúde envolvida
2. Lista de problemas operacionais/assistenciais identificados (mínimo 4 bullets)
3. Parágrafo de posicionamento da tecnologia como potencial resposta
4. Caixa amarela dupla com:
   - **Limitações conhecidas** da solução (ex.: ausência de integração com PEC/RNDS)
   - **Premissa de uso**: a solução atua como apoio, não substitui decisão clínica

Regra de tom: problemas devem ser descritos de forma estrutural/sistêmica,
nunca atribuídos a falhas individuais de profissionais.

---

### SEÇÃO 1.1 — A SOLUÇÃO AVALIADA

Estrutura obrigatória:
1. Parágrafo de identificação: nome, empresa, classificação regulatória
2. Tabela de componentes de hardware (se houver kit/equipamentos)
3. Tabela de exames/funcionalidades apoiadas pelo hardware (se aplicável)
4. Parágrafo de funcionamento do software
5. Caixa azul com princípio de não-obrigatoriedade do hardware (se aplicável)
6. Imagens do produto (se disponíveis — usar as fornecidas pelo usuário)
7. Caixa laranja: premissa inviolável de que a IA/sistema é apoio informacional
8. Remissão ao Anexo I para documentação técnica completa

Regra crítica: A Nonagon (ou qualquer fabricante de hardware integrado pelo
fornecedor) NÃO aparece como parte na PoC. O relacionamento é exclusivamente
com o fornecedor da solução integrada.

---

### SEÇÃO 2 — OBJETIVOS DA PoC

**2.1 Objetivo Geral**
Avaliar viabilidade técnica e operacional mínima em ambiente real, verificando
aderência ao fluxo proposto e potencial de entregar resultados compatíveis com
a proposta funcional declarada.

**2.2 Objetivos Específicos** (mínimo 6, numerados):
- Verificar estabilidade técnica em uso contínuo em ambiente real
- Avaliar capacidade de executar o fluxo completo
- Mensurar tempo médio por atendimento
- Avaliar esforço operacional exigido das equipes
- Analisar consistência e utilidade clínica das saídas
- Identificar limitações técnicas e operacionais
- Avaliar percepção das equipes sobre usabilidade

**2.3 Perguntas Avaliativas** (mínimo 8, em bullets):
Cobrir: estabilidade, completude do fluxo, tempo, esforço operacional,
sobrecarga, compreensibilidade das saídas, integração ao processo de trabalho,
uso contínuo sem comprometer o fluxo, potencial de contribuição.

---

### SEÇÃO 3 — ESCOPO E DELIMITAÇÕES

**3.1 Dentro do Escopo**: lista de o que será testado
**3.2 Fora do Escopo**: incluir sempre:
- Integração com sistemas institucionais (PEC e-SUS APS, RNDS, prontuário)
- Avaliação de impacto clínico definitivo ou desfechos em saúde
- Análise de custo-efetividade
- Pesquisa clínica formal com submissão a CEP (salvo se escopo mudar)

**3.3 Natureza da PoC**: tabela com tipo, característica, volume estimado,
duração estimada, caráter, caráter CEP.

Caixa laranja de atenção ao final: a ausência de integração sistêmica não
configura falha da PoC, mas será registrada como limitação estrutural.

---

### SEÇÃO 4 — CENÁRIO OPERACIONAL E FLUXO

**4.1 Local de Implementação**: UBS ou unidade a definir, com critérios de seleção

**4.2 Perfil dos Profissionais**: tabela com colunas
[Perfil Profissional | Atribuições na PoC]
Incluir sempre: técnico de enfermagem, enfermeiro, médico, gestão local (GSAP),
gestão regional (DIRAPS)

**4.3 Fluxo Operacional**: mínimo 2 cenários alternativos sem hierarquia.
Padrão mínimo:
- Cenário A: conduzido pelo técnico de enfermagem (coleta + encaminhamento ao enfermeiro)
- Cenário B: conduzido pelo enfermeiro
- Cenário C (se aplicável): expandido com participação médica

Cada cenário: lista numerada de passos.
Ao final: caixa laranja com premissa de que as saídas do sistema são apoio
informacional, não substituem avaliação clínica.

**4.4 Critérios de Elegibilidade**: incluídos / excluídos
**4.5 Infraestrutura Necessária**: lista de requisitos

---

### SEÇÃO 5 — GOVERNANÇA E PARTES INTERESSADAS

Tabela com colunas [Ator / Instância | Papel na PoC].

Atores obrigatórios (adaptar conforme contexto):
- DTD — coordenação geral
- DESF/COAPS (ou área assistencial equivalente) — coordenação assistencial
- DIRAPS (ou gestão regional equivalente) — apoio à implementação
- **DIENF/COASIS/SAIS** — apreciação e manifestação formal sobre conformidade
  normativa de enfermagem (SEMPRE incluir quando técnico de enfermagem estiver
  nos fluxos)
- GSAP/unidade de saúde — execução operacional
- Profissionais de saúde — operação e percepção avaliativa
- Fornecedor da solução — suporte técnico, sem interferência assistencial

---

### SEÇÃO 5.1 — COORDENADOR DA PoC E PONTO FOCAL SES-DF

Conteúdo obrigatório:
1. Parágrafo de definição: indicado pelo Diretor da área, podendo ser o próprio
2. Lista de atribuições (mínimo 6):
   - Conduzir tratativas com Ponto Focal do fornecedor
   - Declarar início e encerramento formal
   - Autorizar ajustes operacionais (sem alterar escopo)
   - Acionar mecanismo de interrupção (Seção 8)
   - Justificar prorrogações de prazo (Seção 11.1)
   - Supervisionar instrumentos jurídicos (Seção 11.2)
3. Regra de substituição: membro da Comissão Avaliadora designado pelo Diretor,
   com comunicação formal ao Ponto Focal do fornecedor
4. Definição do Ponto Focal do Fornecedor e suas responsabilidades

---

### SEÇÃO 6 — CRONOGRAMA PRELIMINAR

Tabela com fases [Fase | Atividades Principais]:
- Planejamento
- Preparação
- Execução da PoC
- Avaliação e Consolidação

---

### SEÇÃO 6.1 — DECLARAÇÃO FORMAL DE ENCERRAMENTO

Conteúdo obrigatório:
1. Três hipóteses de encerramento:
   a) Atingimento dos critérios de volume e prazo
   b) Encerramento antecipado pelo mecanismo de interrupção (Seção 8)
   c) Decisão estratégica justificada da área responsável
2. Encerramento como marco de início da contagem dos prazos dos entregáveis
3. Registro obrigatório no processo SEI, com ciência do Ponto Focal do fornecedor

---

### SEÇÃO 7 — MÉTRICAS E CRITÉRIOS DE SUCESSO

**7.1 Indicadores Técnicos**: tabela [Indicador | Meta/Referência]
Incluir sempre:
- Taxa de falhas críticas do sistema (meta: < 5%)
- Disponibilidade do sistema (meta: ≥ 90%)
- Taxa de conclusão do fluxo completo (meta: ≥ 80%)
- Tempo médio por atendimento (a registrar comparativamente)

**7.2 Indicadores Operacionais**: tabela [Indicador | Forma de Aferição]
Incluir sempre:
- Impacto no tempo de atendimento
- Esforço operacional percebido (escala Likert)
- Facilidade de uso (escala Likert)
- Ocorrência de dupla digitação
- Aderência ao fluxo de acolhimento
- Adequação dos perfis de acesso por CBO

**7.3 Critério Global de Sucesso**: lista de condições simultâneas necessárias
para considerar a PoC tecnicamente bem-sucedida.

Caixa laranja ao final: ausência de integração sistêmica não configura falha.

---

### SEÇÃO 8 — GESTÃO DE RISCOS

Tabela com 5 colunas:
[Risco Identificado | Descrição | Probabilidade | Impacto | Mitigação]

Riscos obrigatórios (adaptar conforme solução):
1. Sobrecarga operacional
2. Dupla digitação (ausência de integração)
3. Falhas técnicas do sistema
4. Resistência das equipes
5. Ausência de integração sistêmica
6. Registro incompleto no prontuário oficial
7. Baixa aderência ao fluxo assistencial
8. Inadequação do espaço físico
9. Inadequação de perfis de acesso por CBO (risco alto — sempre incluir)

Caixa laranja ao final: mecanismo de interrupção temporária com gatilhos
(impacto negativo relevante no tempo de atendimento; sobrecarga documentada;
comprometimento do fluxo assistencial regular).

---

### SEÇÃO 9 — ASPECTOS ÉTICOS E REGULATÓRIOS

Lista de bullets cobrindo:
- Caráter de apoio da solução (não substitui decisão clínica)
- Observância à RDC 657/2022 (SaMD) — status a confirmar com fornecedor
- Conformidade com LGPD (Lei 13.709/2018)
- Obrigatoriedade do registro no prontuário oficial
- Modelo de consentimento informado (a definir com orientação jurídica)
- Dispensa ou não de CEP (justificativa)

---

### SEÇÃO 9.1 — CONFORMIDADE COM EXERCÍCIO PROFISSIONAL DE ENFERMAGEM
*(incluir sempre que técnico de enfermagem estiver nos fluxos)*

Estrutura:
1. Parágrafo de abertura: análise normativa preliminar conduzida pela coordenação
   da PoC, caráter preliminar, pendente de validação pela DIENF/COASIS/SAIS
2. Tabela dos normativos aplicáveis (5 normativos padrão):
   - Lei nº 7.498/1986
   - Decreto nº 94.406/1987
   - Resolução COFEN nº 564/2017
   - Resolução COFEN nº 423/2012
   - Resolução COFEN nº 696/2022
3. Análise numerada (mínimo 4 fundamentos) demonstrando conformidade do fluxo
   com os normativos
4. Caixa verde: "Visão técnica preliminar" (não "Conclusão") — caráter preliminar,
   pendente de DIENF
5. Caixa laranja: recomendação de configuração de perfis por CBO antes da execução

REGRA CRÍTICA DE TOM: A análise NÃO deve atribuir questionamentos ou preocupações
a equipes específicas (ex.: "suscitou questionamento pela equipe da UBS"). Usar
sempre: "a coordenação da PoC conduziu análise normativa preliminar sobre possíveis
inconformidades".

---

### SEÇÃO 10 — DELIBERAÇÕES PENDENTES

Lista numerada. Itens obrigatórios (adicionar específicos conforme contexto):

1. Definição e autorização formal da unidade de saúde
2. Aprovação do fluxo operacional pela gestão assistencial
3. Definição dos profissionais participantes
4. Autorização institucional para execução
5. Alinhamento formal com fornecedor (SLA, responsabilidades)
6. Confirmação de perfis de acesso diferenciados por CBO, antes da execução
7. Definição do modelo de consentimento informado
8. Validação da infraestrutura necessária
9. Alinhamento com gestão regional
10. Confirmação do status regulatório (RDC 657/2022) junto ao fornecedor
11. Submissão da análise normativa de enfermagem (Seção 9.1) à DIENF/COASIS/SAIS
    *(se Seção 9.1 estiver presente)*
12. Indicação formal do Coordenador da PoC
13. Indicação formal do Ponto Focal do fornecedor
14. Elaboração, aprovação jurídica e assinatura dos instrumentos da Seção 11.2
    *(se Seção 11.2 estiver presente)*

---

### SEÇÃO 11 — RESULTADO ESPERADO

Lista de entregáveis esperados:
- Relatório técnico de avaliação da solução
- Análise de viabilidade técnica e operacional
- Avaliação de aderência ao processo de trabalho
- Inventário de limitações técnicas e operacionais
- Registro estruturado das percepções das equipes
- Subsídios técnicos para decisão institucional

Parágrafo final obrigatório: "Os resultados da PoC não implicam, por si só,
compromisso de aquisição ou de expansão da solução, constituindo exclusivamente
insumo técnico para o processo decisório da SES-DF."

---

### SEÇÃO 11.1 — RESPONSÁVEIS PELOS ENTREGÁVEIS E PRAZOS

Tabela com 4 colunas:
[Entregável | Responsável (servidor) | Prazo (dias após encerramento) | Ponto focal (fornecedor)]

Prazos padrão:
- Registro de percepções das equipes: **15 dias**
- Relatório técnico de avaliação: **30 dias**
- Análise de viabilidade técnica e operacional: **30 dias**
- Avaliação de aderência ao processo: **30 dias**
- Inventário de limitações: **30 dias**
- Subsídios para decisão institucional: **45 dias**

Caixa amarela obrigatória após a tabela — prorrogação de prazos:
"Os prazos poderão ser prorrogados mediante manifestação e justificativa formal
do Coordenador da PoC, registrada no processo SEI. Considera-se a natureza da
saúde pública e as imprevisibilidades inerentes ao setor [...]"

---

### SEÇÃO 11.2 — INSTRUMENTOS JURÍDICOS NECESSÁRIOS À EXECUÇÃO
*(incluir sempre que houver equipamentos do fornecedor em uso pela equipe SES-DF)*

Três instrumentos obrigatórios, cada um com parágrafo descritivo:

**a) Termo de Empréstimo de Equipamentos**
- Identificação individualizada dos equipamentos (descrição, nº de série, valor)
- Responsável pelo recebimento: Coordenador da PoC
- Condições de uso, guarda, transporte, devolução e prazo
- Responsabilidade institucional (SES-DF), não individual
- Responsabilização individual restrita a dolo ou culpa grave comprovados
- Sujeito à aprovação da assessoria jurídica da SES-DF

**b) Termo de Aceite de Treinamento**
- Assinado individualmente por cada profissional participante
- Confirma treinamento recebido e compreensão dos parâmetros de uso
- Protege o profissional: erros de adaptação em contexto de inovação não
  configuram negligência
- Sujeito à aprovação da assessoria jurídica da SES-DF

**c) Acordo Operacional de Responsabilidades ([Fornecedor] × SES-DF)**
- Execução com representantes presentes: riscos operacionais assumidos pelo fornecedor
- Execução sem representantes: operação sob responsabilidade da SES-DF
- Danos aos equipamentos em uso regular: fornecedor não responsabiliza a SES-DF,
  salvo dolo ou culpa grave comprovados
- Vigência: conforme estipulado no documento formal da PoC
- Encerramento antecipado automático com a PoC
- Sujeito à aprovação da assessoria jurídica da SES-DF

Parágrafo final: todos os instrumentos devem ser aprovados pela assessoria jurídica
e assinados antes do início da execução.

---

### CAIXA INAUGURAL (ao final da Seção 11, quando aplicável)

Usar caixa azul quando for a primeira PoC formal da área:

"★ Nota sobre o caráter inaugural desta PoC: Esta Prova de Conceito constitui
[a primeira / uma das primeiras] iniciativas formais da SES-DF de avaliação
estruturada de solução de saúde digital, sendo conduzida com o propósito adicional
de subsidiar a construção do Marco Regulatório Interno de PoCs em Saúde Digital
da SES-DF. Os aprendizados metodológicos, operacionais e institucionais gerados
ao longo desta PoC [...] serão aproveitados para a padronização do rito técnico,
operacional e legal aplicável a futuras provas de conceito no âmbito da Secretaria."

---

### ANEXO I — DOCUMENTAÇÃO TÉCNICA DO FORNECEDOR

Se o usuário fornecer documentação técnica do fornecedor:
1. Incluir como Anexo I em seção separada do documento (nova section no DOCX)
2. Nota introdutória obrigatória: "As declarações técnicas, funcionais e
   regulatórias contidas neste anexo são de integral responsabilidade da empresa
   [Fornecedor], na qualidade de fornecedora da solução, não representando
   posicionamento institucional da SES-DF, da SETIS ou da DTD."
3. Tabela de catalogação do documento do fornecedor
4. Resumo executivo da solução (parafraseado, não copiado)
5. Tabela da estrutura do documento completo
6. Marco regulatório declarado pelo fornecedor
7. Alerta de verificação pendente do status RDC 657/2022

---

## 3. Textos-padrão reutilizáveis

### Premissa inviolável da solução (caixa laranja)
"[Nome da solução] atua exclusivamente como ferramenta de apoio informacional.
Todas as hipóteses clínicas, sugestões de conduta e classificações geradas possuem
caráter estritamente sugestivo, requerendo avaliação, validação e responsabilização
de profissional habilitado. Para descrição técnico-funcional completa da solução,
consultar o Anexo I deste documento."

### Limitação de integração sistêmica (caixa amarela)
"A solução não possui integração nativa com sistemas institucionais (e-SUS APS PEC,
RNDS), operando de forma independente do ecossistema digital vigente na SES-DF,
com potencial impacto operacional decorrente da necessidade de registro paralelo."

### Mecanismo de interrupção (caixa laranja — Seção 8)
"A PoC poderá ser interrompida temporariamente pela coordenação caso haja: impacto
negativo relevante e mensurável no tempo de atendimento; sobrecarga documentada das
equipes; ou comprometimento do fluxo assistencial regular."

### Prorrogação de prazos (caixa amarela — Seção 11.1)
"Os prazos estabelecidos poderão ser prorrogados mediante manifestação e justificativa
formal do Coordenador da PoC, registrada no processo SEI. Considera-se, em particular,
a natureza da saúde pública e as imprevisibilidades inerentes ao setor, que podem
envolver desdobramentos súbitos — surtos, eventos de saúde coletiva, redirecionamento
de equipes para demandas emergenciais — capazes de impactar a disponibilidade dos
profissionais envolvidos e a conclusão dos entregáveis nos prazos originalmente
previstos."

### Resultado não implica compromisso de aquisição
"Os resultados da PoC não implicam, por si só, compromisso de aquisição ou de
expansão da solução, constituindo exclusivamente insumo técnico para o processo
decisório da SES-DF."

---

## 4. Diretrizes de formatação DOCX

### Identidade visual
- Fonte: Arial em todo o documento
- Cor primária (títulos H1): #1F3864 (azul escuro institucional)
- Cor secundária (títulos H2): #2E75B6 (azul médio)
- Texto corrido: #222222
- Largura útil A4: 9026 DXA (margens de 1 polegada)

### Estilos de parágrafo
- Corpo: tamanho 22 (11pt), espaçamento 276, justificado
- Bullets: numeração docx com LevelFormat.BULLET, indent left 720 hanging 360
- Listas numeradas: LevelFormat.DECIMAL, mesmo indent

### Tabelas
- Sempre dual width: columnWidths + width em cada célula (DXA)
- Cabeçalho: fill #1F3864, texto branco, bold
- Linhas alternadas: #F2F2F2 e #FFFFFF
- Bordas: SINGLE, size 1, color #CCCCCC
- Margins internas: top/bottom 80, left/right 120

### Caixas de destaque
| Tipo | Fill | Cor do texto/label |
|------|------|--------------------|
| Amarela (alerta/atenção) | #FFF3CD | #7B4F00 |
| Azul (informação) | #D6E4F0 | #1F3864 |
| Verde (positivo/confirmação) | #E8F5E9 | #1B5E20 |
| Azul escuro (nota inaugural) | #E3F2FD | #0D47A1 |

### Cabeçalho e rodapé
- Cabeçalho: "SES-DF | DTD — [título abreviado da PoC]"
  com borda inferior azul (#2E75B6)
- Rodapé: "Versão X.X — Uso Interno | Confidencial" + número de página à direita
  com borda superior azul

### Imagens
- Usar sempre que o usuário fornecer imagens do produto/hardware
- Duas imagens no corpo da Seção 1.1: visão geral do kit + kit com acessórios
- Demais imagens de detalhe: reservar para o Anexo I
- Legenda em itálico, tamanho 18, cor #666666, centralizada

---

## 5. Script base de geração

O script Node.js completo para geração do DOCX segue o padrão da PoC MedNear.
Estrutura base a replicar:

```javascript
const {
  Document, Packer, Paragraph, TextRun, Table, TableRow, TableCell,
  AlignmentType, HeadingLevel, BorderStyle, WidthType, ShadingType,
  LevelFormat, Footer, Header, TabStopType, TabStopPosition,
  SimpleField, ImageRun, PageBreak
} = require('docx');
const fs = require('fs');

// Constantes de cor
const BLUE  = "1F3864";
const MID   = "2E75B6";
const GRAY  = "F2F2F2";
const TEXT  = "222222";
const W     = 9026;

// Bordas padrão
const bdr  = { style: BorderStyle.SINGLE, size: 1, color: "CCCCCC" };
const bdrs = { top: bdr, bottom: bdr, left: bdr, right: bdr };

// Helpers obrigatórios:
// space(before), pb(), h1(text), h2(text), h3(text),
// p(text, opts), bullet(text), alertBox(label, text, fill, labelColor),
// infoBox(label, text), greenBox(label, text), twoCol(rows, w1, w2),
// govTable(rows), fiveCol(rows) [riscos], kitTable(rows),
// imageRow(imgData, w, h, caption), assinaturasTable()

// Numerações obrigatórias no Document:
// "bullets", "num-obj", "num-fluxA", "num-fluxB", "num-fluxC", "num-delib"

// Seções: sempre duas — corpo principal + Anexo I (se houver)
// Cada seção com seu próprio header/footer e sectPr
```

Ao gerar o script completo, adaptar:
- Nome da solução e empresa em todos os campos
- Área de saúde no contexto e justificativa
- Fluxos operacionais conforme perfis disponíveis
- Riscos conforme especificidades da solução
- Indicadores técnicos conforme funcionalidades a testar
- Atores de governança conforme área institucional envolvida

### Validação obrigatória após geração
```bash
python3 /mnt/skills/public/docx/scripts/office/validate.py [arquivo.docx]
python3 /mnt/skills/public/docx/scripts/office/soffice.py --headless \
  --convert-to pdf [arquivo.docx] --outdir [dir_saida]/
```

Se validação falhar: desempacotar com `unpack.py`, corrigir XML, reempacotar
com `pack.py --original [original.docx]`. Erros mais comuns:
- `<w:r>` aberto sem `</w:r>` antes do `</w:p>` → adicionar `</w:r>`
- Fragmento órfão `</w:pPr><w:r><w:t/></w:r></w:p>` → remover com Python replace
- `sectPr` fora de parágrafo → envolver em `<w:p><w:pPr>...</w:pPr></w:p>`

---

## 6. Checklist de qualidade antes de entregar

Antes de apresentar o DOCX ao usuário, verificar:

- [ ] Todas as 11 seções obrigatórias presentes
- [ ] Seção 5.1 (Coordenador da PoC) incluída
- [ ] Seção 6.1 (Encerramento Formal) incluída
- [ ] Seção 9.1 incluída se técnico de enfermagem estiver nos fluxos
- [ ] DIENF/COASIS/SAIS na tabela de governança (Seção 5)
- [ ] Seção 11.2 incluída se houver equipamentos do fornecedor
- [ ] Deliberações Pendentes contemplam todos os instrumentos jurídicos
- [ ] Caixa amarela de prorrogação de prazos na Seção 11.1
- [ ] Premissa inviolável de apoio informacional presente (Seção 1.1)
- [ ] Nonagon (ou fabricante de hardware integrado) NÃO aparece como parte
- [ ] Campos [a indicar] e [a definir] marcados corretamente
- [ ] Versão "0.1" na capa e no rodapé
- [ ] Validação DOCX passou sem erros
- [ ] PDF gerado com sucesso
