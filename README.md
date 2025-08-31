# Projeto de Business Intelligence para Comissionamento de Vendas 3P


## Autores
Naomi Arakaki 10438010

Melissa Zanelato 10436651

# Cenário de Negócio e Concepção da Solução

Um marketplace generalista, que opera com um vasto leque de categorias de produtos, busca otimizar sua tomada de decisão de forma que sejam orientadas a dados. Neste modelo, os vendedores parceiros (*sellers*) são responsáveis por anunciar seus produtos, gerenciar a logística de entrega, definir a precificação e executar as estratégias de marketing.


Problema Central: A ausência de uma ferramenta analítica centralizada dificulta a tomada de decisão, que pode ser baseada mais em intuição do que em dados concretos, gerando potenciais perdas de receita e oportunidades de crescimento.

> Assim, o sistema que vamos construir busca transformar o marketplace em uma organização **data-driven**, construindo um **Data Warehouse (DW)** centralizado como única fonte da verdade. A arquitetura será otimizada com **Data Marts** departamentais para garantir alta performance. Integrado a uma plataforma de **Business Intelligence (BI)**, o projeto visa democratizar o acesso a dados consistentes e acionáveis, fomentando uma cultura de decisões estratégicas baseadas em evidências.

### Clientes (Sponsors do Projeto)

Este grupo representa a liderança da empresa, responsável por aprovar, financiar e definir a direção estratégica do projeto.

-   **C-Level (CEO, COO, CFO, CMO):** Utilizarão os dashboards executivos para monitorar a saúde geral do negócio, tomar decisões estratégicas de alto impacto e reportar resultados ao conselho.
-   **Diretores e Chefes de Departamento (Vendas, Marketing, Operações, Produto):** São os principais clientes dos Data Marts departamentais. Eles patrocinam o projeto para obter autonomia e inteligência de dados para suas equipes, visando o cumprimento de metas e a otimização de suas áreas.

### Usuários Finais (Consumidores da Informação)

São os profissionais que irão interagir diretamente com a plataforma de BI no dia a dia para executar suas funções.

-   **Analistas de Dados e de BI:** Usuários avançados que irão construir dashboards, realizar análises complexas (ad-hoc) e disseminar insights pela organização.
-   **Analistas de Marketing:** Utilizarão a plataforma para segmentar clientes, medir o ROI de campanhas, analisar o funil de conversão e otimizar o orçamento de marketing.
-   **Gerentes de Categoria e Vendas:** Monitorarão o desempenho de vendedores (sellers), a performance de produtos, a competitividade de preços e a saúde de suas categorias.
-   **Analistas de Operações e Logística:** Acompanharão a eficiência das entregas, os custos de frete, os níveis de serviço do atendimento ao cliente e os indicadores de fraude.
-   **Gerentes de Produto (Product Managers):** Analisarão o comportamento do usuário na plataforma, o engajamento com novas funcionalidades e o desempenho da busca interna para guiar o roadmap do produto.

### Equipe do Projeto (Construtores e Mantenedores)

Este grupo é responsável pelo desenvolvimento técnico, manutenção e evolução da infraestrutura de dados.

-   **Engenheiros de Dados:** Responsáveis por construir e manter os pipelines de ETL/ELT, o Data Warehouse e os Data Marts, garantindo a qualidade e a disponibilidade dos dados.
-   **Desenvolvedores de BI:** Especialistas na ferramenta de BI escolhida, responsáveis por criar os modelos de dados semânticos, dashboards complexos e treinar os usuários finais.
-   **Administradores de Sistemas / DevOps:** Garantirão a infraestrutura, segurança e performance da solução em nuvem.

### Impactados Indiretos (Beneficiários do Ecossistema)

Embora não acessem a plataforma diretamente, estes grupos serão positivamente impactados pelas melhorias e otimizações que ela proporciona.

-   **Vendedores do Marketplace (Sellers):** Serão beneficiados por políticas mais justas e transparentes, insights sobre tendências de mercado (compartilhados pelo marketplace) e uma plataforma mais eficiente para vender seus produtos.
-   **Clientes Finais (Compradores):** Terão uma melhor experiência de compra através de uma plataforma mais estável, recomendações de produtos mais relevantes, um sortimento de produtos alinhado com suas buscas e um atendimento ao cliente mais ágil e eficaz.

### Fatores Críticos de Qualidade

O sucesso do produto será medido pela sua capacidade de entregar os seguintes atributos:

* Velocidade e Desempenho para uma tomada de decisão ágil.
* Baixa curva de aprendizado e interface intuitiva para promover a adoção em todos os níveis.
* Precisão e consistência dos dados e dos cálculos apresentados.
* Possibilidade de integração de novas fontes de dados.
* Capacidade de cálculo de novas métricas com os dados disponíveis.
* Permitir que os usuários criem seus próprios relatórios para explorar os dados de acordo com suas necessidades específicas e em poucos cliques, de forma independente.
* Possibilitar compartilhamento de relatórios entre os usuários.
* Controle de acesso para dados confidenciais.
* Abertura de tickets para relatos de problemas no sistema.
  
# Modelo de Casos de Uso

## Casos de Uso por Ator

### Usuário do Sistema
| Caso de Uso                                  |
|----------------------------------------------|
| Integrar de novas tabelas de dados           |
| Acessar relatórios prontos                   |
| Selecionar tabelas para novo relatório       |
| Selecionar métricas por categoria/seller/SKU |
| Selecionar períodos de tempo                 |
| Criar métricas a partir das disponíveis      |
| Editar formas de vizualizações de dados      |
| Exportar relatório                           |
| Abrir ticket                                 |

| Caso de Uso                       | Detalhes (`<<include>>`)   |
|-----------------------------------|----------------------------|
| Integrar de novas tabelas        |                            |
| Acessar relatórios prontos       |                            |
| Criar novo relatório             |                            |
|                                   | Selecionar tabelas       |
|                                   | Selecionar métricas       |
|                                   | Selecionar períodos      |
|                                   | Criar métricas.            |
|                                   | Selecionar formas de vizualizar os dados      |
|                                   | Escolher nome para o relatório          |
|                                   | Salvar relatório          |
| Editar relatório                 |                            |
| Conpartilhar relatório           |                            |
| Abrir ticket                     |                            |
| Vizualizar ticket                |                            |
| Ir para a área de aprendizado    |                            |
 



### Administrador do Sistema
| Caso de Uso                      | Detalhes (`<<include>>`) |
|----------------------------------|--------------------------|
| **Administrar usuários**         |                          |
|                                  | Configurar permissões à bases de dados   |
|                                  | Criar usuário            |
|                                  | Excluir usuário          |


### Sistema de Integração
| Caso de Uso                |
|----------------------------|
| Atualizar base de dados    |


---

## 2. Descrição Resumida dos Casos de Uso

 

---

## 3. Caso de Uso Crítico (Detalhado)

**Caso de Uso:** *Visualizar Simulações de Impacto de Comissão*  

- **Ator Principal:** Usuário do Sistema  
- **Objetivo:** Avaliar cenários de alteração da taxa de comissão e seu impacto no lucro e ROI.  
- **Pré-condições:**  
  - O sistema deve estar integrado às bases de dados de vendas e produtos.  
  - O usuário deve estar autenticado com perfil válido.  
- **Fluxo Principal:**  
  1. O usuário acessa o módulo de simulações.  
  2. Seleciona categoria, seller ou SKU.  
  3. Define um novo percentual de comissão hipotético.  
  4. O sistema recalcula os indicadores (lucro, ROI, elasticidade de preço).  
  5. O sistema exibe os resultados em gráficos comparativos (antes x depois).  
- **Fluxo Alternativo:**  
  - Caso os dados da categoria/seller não estejam disponíveis, o sistema informa indisponibilidade de análise.  
- **Pós-condições:**  
  - O usuário obtém relatórios visuais para tomada de decisão sobre ajustes de comissão.  

---

## 4. Diagrama de Caso de Uso (UML)

