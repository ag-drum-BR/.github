# drum

Esta raiz concentra a documentação de referência para a organização `ag-drum-BR`, com foco na convenção dominante de nomenclatura dos repositórios de entrega.

## Sobre a Drum

A Drum se posiciona como uma agência orientada a crescimento, capaz de integrar criatividade, mídia, dados, conteúdo, experiência e cultura em uma entrega coordenada. A proposta central da marca é transformar complexidade em sincronia, conectando disciplinas, decisões e execução em torno de um mesmo ritmo de negócio.

No contexto brasileiro, a Drum é apresentada como uma operação full service com forte legado criativo e capacidade de entrega integrada. Mais do que gerar volume ou presença isolada, a marca busca construir impacto memorável, alinhando ideias e execução para acelerar crescimento com consistência.

## Escopo

Este documento define uma convenção genérica para naming de repositórios de entrega.

Ficam fora deste escopo:

- repositórios utilitários
- ferramentas internas
- exceções históricas de naming

## Convenção Dominante

O padrão dominante adotado para repositórios de entrega é:

`<cliente>-<tipo-de-entrega>-<marca-ou-produto>-<tema-ou-recorte>-<diferenciador-opcional>-<ano-opcional>`

Quando aplicável, também pode existir uma variação com menos blocos, desde que a ordem lógica seja preservada:

`<cliente>-<tipo-de-entrega>-<marca-ou-produto>-<tema-ou-recorte>`

## Regras

- Usar sempre `kebab-case`
- Usar apenas letras minúsculas, números e hífens
- Não usar espaços, underscore, camelCase ou acentos
- Começar pelo identificador do cliente
- Declarar o tipo de entrega logo após o cliente
- Declarar a marca ou produto antes do tema específico
- Usar diferenciador apenas quando ele realmente separar uma variação relevante
- Colocar o ano no final quando ele fizer parte da identificação da entrega

## Ordem dos Blocos

### 1. Cliente

Identifica o cliente, conta ou unidade principal dona da entrega.

Exemplo:

- `cliente`

### 2. Tipo de Entrega

Identifica a natureza do material.

Exemplos observados:

- `visual-aid`
- `email-fragment`
- `landing-page`
- `detail-aid`

### 3. Marca ou Produto

Identifica o ativo principal da entrega.

Exemplos observados:

- `marca`
- `produto`
- `solucao`

### 4. Tema ou Recorte

Identifica o assunto principal, campanha, público, contexto clínico ou recorte do material.

Exemplos observados:

- `campanha`
- `segmento`
- `indicacao`
- `tema-especifico`

### 5. Diferenciador Opcional

Usar apenas quando necessário para distinguir variantes reais do mesmo material.

Exemplos observados:

- `versao-a`
- `regional`
- `publico-especifico`
- `id-interno`
- `faixa-etaria`

### 6. Ano Opcional

Quando presente, deve ficar no final.

Exemplos:

- `2023`
- `2024`
- `2025`
- `2026`

## Exemplos Válidos

- `cliente-visual-aid-marca-2024`
- `cliente-visual-aid-marca-campanha-2024`
- `cliente-visual-aid-produto-segmento-versao-a-2025`
- `cliente-email-fragment-produto-tema`
- `cliente-detail-aid-solucao-indicacao-id-interno-2026`

## Exemplos a Evitar

- `Cliente-VisualAid-Marca-2024`
- `cliente_visual_aid_marca_2024`
- `cliente-2024-marca-visual-aid`
- `visual-aid-cliente-marca-2024`
- `cliente-visual-aid-2024`

## Critérios de Decisão

Ao criar um novo repositório, validar nesta ordem:

1. Qual é o cliente?
2. Qual é o tipo de entrega?
3. Qual é a marca ou produto principal?
4. Qual é o tema, recorte ou contexto que realmente diferencia este material?
5. Existe necessidade real de um diferenciador adicional?
6. O ano precisa entrar para identificar a entrega?

Se uma parte não ajuda a distinguir o material de forma operacional, ela não deve entrar no nome.

## Recomendação Prática

Antes de criar um novo repositório, reutilize a estrutura mais próxima já existente e altere apenas os blocos necessários. Isso reduz drift de nomenclatura e evita novos padrões paralelos dentro da organização.

## Manutenção

Se a organização passar a adotar novos tipos de entrega além de `visual-aid` e `email-fragment`, este documento deve ser atualizado para refletir o padrão oficial antes da criação recorrente de novos repositórios.
