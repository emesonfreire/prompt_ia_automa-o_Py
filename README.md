# Prompt de Engenharia de IA para Automação

Este repositório contém um prompt de engenharia de IA altamente estruturado para gerar soluções de automação em Python, com foco em projetos corporativos, qualidade de código e execução em Google Colab.

## O que está aqui

- `prompt_eng_ia_automacao.md`: o prompt principal que descreve o papel, requisitos e formato de entrega esperados.
- `README.md`: uma explicação amigável de como usar o prompt corretamente.

## Para que serve este prompt

Este prompt foi criado para orientar um modelo de linguagem a agir como um engenheiro sênior de automação/RPA com foco em:

- código Python limpo e tipado
- modularidade e padrões SOLID
- tratamento robusto de erros
- logging corporativo
- auditoria e métricas de execução
- execução em ambiente Google Colab

## Como usar o prompt

1. Abra `prompt_eng_ia_automacao.md`.
2. Substitua os campos entre colchetes `[ ]` com as informações do seu processo:
   - `AS-IS`: descreva o processo atual manual.
   - `TO-BE`: descreva o resultado automatizado desejado.
   - `Criticidade`: Alta, Média ou Baixa.
   - `Volume estimado`: por exemplo, `~500 registros/execução`.
3. Se for um pedido de refatoração, cole o código original dentro do bloco `Código original para refatoração`.
4. Envie o prompt completo para o modelo de IA ou use-o como base para a solicitação.

## Estrutura esperada do resultado

O prompt orienta o modelo a entregar em quatro partes:

1. Diagnóstico Técnico
2. Código Refatorado
3. Justificativa de Arquitetura
4. Dependências necessárias

Além disso, o código deve seguir os requisitos técnicos obrigatórios:

- usar `dataclasses` ou `TypedDict` para schemas
- aplicar type hints em todas as funções
- centralizar configurações em `CONFIG`
- evitar `print()` para logging
- usar `logging` com formato corporativo
- tratar erros de forma granular
- manter registros rejeitados em `rejected_records`
- apresentar resumo de execução com métricas

## Dicas para usar melhor o prompt

- Sempre forneça o máximo de contexto do processo manual e dos dados de entrada.
- Não envie apenas “faça um script”; descreva o problema, o ambiente e as regras de negócio.
- Se não houver código inicial, o prompt pede explicitamente para solicitá-lo antes de prosseguir.
- Peça ao modelo para manter todo código “production-ready” e compatível com `flake8` e `mypy --strict` conceitualmente.

## Uso em Google Colab

O prompt é pensado para ser usado em notebooks Colab. Algumas orientações específicas:

- instale dependências em uma célula `!pip install ...`
- coloque imports e `CONFIG` em células iniciais
- mantenha funções em células separadas por responsabilidade
- não use `if __name__ == "__main__"`
- use variáveis sensíveis via `os.environ` ou `google.colab` quando necessário

## Como adaptar para outros contextos

Se você quiser usar este prompt fora do Colab, mantenha a mesma disciplina de engenharia:

- preserve o bloco `CONFIG`
- mantenha logging consistente
- use tratamento de dados e validações robustas
- mantenha o formato de entrega dividido em diagnóstico, código, justificativa e dependências

## Conclusão

Use `prompt_eng_ia_automacao.md` como roteiro para solicitar soluções de automação Python de forma confiável. Este README explica o propósito, a forma de uso e as melhores práticas para obter resultados profissionais com o prompt.
