# Projeto de Business Intelligence para Comissionamento de Vendas 3P


## Autores
Naomi Arakaki 10438010

Melissa Zanelato 10436651

## Cenário de Negócio e Concepção da Solução

Um e-commerce generalista, que opera com um vasto leque de categorias de produtos, busca otimizar sua estratégia de comissionamento para as operações de marketplace (3P). Neste modelo, os vendedores parceiros (*sellers*) são responsáveis por anunciar seus produtos, gerenciar a logística de entrega, definir a precificação e executar as estratégias de marketing.

Problema Central: A necessidade de um sistema robusto que forneça insights claros e acionáveis para a definição das taxas de comissão de vendas. A ausência de uma ferramenta analítica centralizada dificulta a tomada de decisão, que pode ser baseada mais em intuição do que em dados concretos, gerando potenciais perdas de receita e oportunidades de crescimento.

Para endereçar este desafio, propõe-se a criação de um **Sistema de Business Intelligence (BI)** focado em monitorar e analisar as métricas essenciais que influenciam e são influenciadas pelas comissões de vendas.

O objetivo é transformar dados brutos em inteligência de negócio, permitindo que a liderança e as equipes táticas tomem decisões mais rápidas, estratégicas e baseadas em evidências.

### 🎯 Objetivos do Sistema

* **Centralizar e Integrar Dados:** Unificar diferentes fontes de dados (vendas, cadastro de produtos, *sellers*, etc.) em um único ambiente analítico.
* **Análise de Métricas Chave:** Fornecer cálculos precisos e visualizações claras das seguintes métricas:
    * ROI (Retorno sobre o Investimento)
    * Elasticidade de Preço vs. Comissão e Lucro
* **Segmentação e Agrupamento:** Permitir a análise das métricas com diferentes níveis de granularidade:
    * Por **Categoria**
    * Por **Vendedor** (*Seller*)
    * Por **SKU** (Unidade de Manutenção de Estoque)
* **Empoderar Usuários:** Capacitar as equipes a realizarem suas próprias análises sem depender do time de tecnologia.

### 👥 Público-Alvo

O sistema atenderá a um amplo espectro de profissionais, desde a liderança estratégica até os analistas táticos:

* **Liderança Executiva:** Comercial e Financeiro.
* **Diretoria e Gerência:** Setores Financeiro, de Vendas e de Categorias.
* **Analistas e Especialistas:** Profissionais que influenciam a tomada de decisão.

### ✨ Fatores Críticos de Qualidade

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
  
# 📌 Modelo de Casos de Uso

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

### Administrador do Sistema
| Caso de Uso                      | Detalhes (`<<include>>`) |
|----------------------------------|--------------------------|
| **Administrar usuários**         |                          |
|                                  | Configurar permissões    |
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

