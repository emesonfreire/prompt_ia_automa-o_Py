# Prompt de Engenharia de IA para Automação

Este novo **README** foi estruturado para refletir a robustez técnica da **v3 (Enterprise-Grade)** do seu prompt. Ele posiciona o framework não apenas como um gerador de scripts, mas como uma ferramenta de governança para engenharia de software em automação.

---

# 🚀 Framework de Prompting: Engenheiro de Automação Python (v3)

Este repositório contém um framework de **Prompt Engineering** de alta fidelidade, projetado para transformar requisitos de negócio em sistemas de automação Python robustos, resilientes e prontos para o ambiente corporativo (*Enterprise-Grade*).

## 🎯 O que é este Framework?

Diferente de prompts genéricos de codificação, a **v3** impõe uma governança de engenharia rigorosa. Ele força o modelo de IA a atuar como um **Engenheiro Sênior de Software/RPA** (nível Big4/Accenture), garantindo que a saída não seja apenas funcional, mas auditável e sustentável.

### Pilares Técnicos Incorporados
* **SOLID Completo:** Desacoplamento via `Protocols` (Interface Segregation e Dependency Inversion).
* **Arquitetura em Camadas:** Separação inegociável entre **IO** (`Reader`/`Writer`) e **Lógica de Domínio** (Pura).
* **Resiliência Industrial:** Implementação de *Exponential Backoff* e *Retry* com a biblioteca `tenacity`.
* **Segurança de Dados:** Sanitização de entradas e mascaramento automático de campos sensíveis em logs.
* **Idempotência:** Proteção contra reexecuções e processamentos duplicados via checksum/hash.

---

## 🛠️ Como Utilizar

1.  **Copie o Prompt:** Utilize o conteúdo integral do arquivo `prompt_eng_ia_automacao.md`.
2.  **Preencha os Metadados:** Localize os blocos `[SUBSTITUIR]` e forneça:
    * **AS-IS / TO-BE:** O fluxo manual atual vs. o objetivo automatizado.
    * **Contexto de Processo:** Defina criticidade e volume estimado.
    * **Entrada de Código:** Se for uma refatoração, cole o código legado; se for um projeto novo (*greenfield*), descreva as regras.
3.  **Execução:** Envie para a IA (Gemini 1.5 Pro, GPT-4, etc.) e receba uma solução estruturada para produção.

---

## 🏗️ Estrutura da Resposta Esperada

O prompt obriga a IA a entregar a solução dividida em 5 seções críticas:

1.  **Diagnóstico Técnico:** Análise detalhada de falhas e violações de princípios de software no cenário original.
2.  **Código Completo (Production-Ready):** Solução 100% tipada, modularizada e sem omissões (`...`).
3.  **Testes Unitários:** Suite de testes com `pytest` cobrindo o caminho feliz, falhas de validação e erros de IO.
4.  **Justificativa de Arquitetura:** Explicação técnica da superioridade da abordagem escolhida.
5.  **Dependências:** Lista exata de bibliotecas com versões mínimas recomendadas.

---

## 🧪 Requisitos de Qualidade (Checklist)

Para ser considerada válida pelo framework, a saída deve cumprir:
* **Zero Magic Numbers:** Configurações centralizadas exclusivamente no dicionário `CONFIG`.
* **Logging Profissional:** Proibido o uso de `print()`. Logs com timestamps e níveis hierárquicos.
* **Testabilidade:** A camada de **Domain** deve ser testável sem necessidade de rede ou banco de dados.
* **Segurança:** Uso de `os.environ` para segredos e proibição de valores *hardcoded*.
* **Paralelismo:** Implementação de `ThreadPoolExecutor` para operações de rede/API.

---

## 📓 Fluxo em Google Colab

O prompt é otimizado para a estrutura de notebooks:
* **Modularização por Células:** Organização lógica (Imports -> Config -> Schemas -> Camadas -> Orquestrador).
* **Resumo Executivo:** Ao final da execução, um quadro visual com métricas (Sucessos, Erros, Tempo) deve ser exibido.

---

## 🤝 Contribuição

Este framework é um documento vivo. Sinta-se à vontade para adaptar as regras de `naming conventions` ou adicionar novos `Protocols` baseados na stack tecnológica específica do seu time.

---

> **Aviso:** Este prompt foi desenhado para eliminar o "código descartável" e elevar o padrão de entrega de automações RPA para o nível de Engenharia de Software.
