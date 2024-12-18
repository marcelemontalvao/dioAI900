# Laboratório _Trabalhando com Machine Learning na Prática no Azure ML_

Este laboratório explora a criação de um espaço de trabalho no Azure, o uso do Machine Learning Studio para automação, e a análise de dados para previsão de aluguel de bicicletas.

## Pré-requisitos

*   **Conta no Azure:** É necessário ter uma conta ativa no Azure. Se você não tem uma, você pode criar uma conta gratuita no site do Azure.
    *   Ao criar sua conta, você receberá **200 dólares de crédito** para usar em 30 dias, além de acesso a serviços gratuitos por 12 meses e alguns serviços que são sempre gratuitos.
    *   É importante lembrar de **excluir todos os recursos** após a conclusão dos laboratórios para evitar cobranças.
*   **Acesso ao Portal do Azure:** Você precisará acessar o portal do Azure para criar os recursos.

## Passos para Criar o Laboratório

1.  **Acessar o Portal do Azure:** Vá para o site do Azure e faça login na sua conta.
2.  **Personalizar a Interface:** Você pode personalizar a interface do Azure, como idioma, região e aparência.
3.  **Criar um Recurso:**
    *   Clique em "**criar um recurso**" e procure por "**machine learning**".
    *   Selecione "**Machine Learning**" no marketplace e clique em "**create**".
4.  **Configurar o Workspace:**
    *   **Assinatura:** Selecione sua assinatura do Azure.
    *   **Grupo de Recursos:** Crie um novo grupo de recursos ou selecione um existente. Pense no grupo de recursos como uma "**gaveta**" ou "**baú**" para organizar seus recursos.
    *   **Detalhes do Workspace:**
        *   Nomeie seu workspace (deve ser um nome único). Por exemplo, "**laboratorioAI900**".
        *   Escolha uma região (a região dos EUA é sugerida para reduzir custos).
        *   Mantenha as configurações padrão para "**Storage account**," "**Key vault**" e "**Application insights**".
    *   Clique em "**Review + Create**" e depois em "**Create**".
    *   Aguarde a criação do recurso, acompanhando o status do deploy na tela.
5.  **Acessar o Machine Learning Studio:**
    *   Após a conclusão do deploy, clique em "**Go to resource**".
    *   Clique em "**ir para o estúdio**" para acessar o Machine Learning Studio.
    *   Se for seu primeiro acesso, pode ser necessário preencher informações para criar um workspace no Machine Learning Studio.
6.  **Criar um Trabalho de ML Automatizado:**
    *   Na barra lateral esquerda, clique em "**ML automatizado**".
    *   Clique em "**novo trabalho de ML automatizado**".
    *   **Nome do Trabalho:** Use "**bike**" como nome do trabalho e do experimento.
    *   **Descrição:** Adicione uma descrição como "**aprendizado de máquina automatizado para previsão de aluguel de bicicletas**".
    *   **Tipo de Tarefa:** Selecione "**regressão**".
    *   **Conjunto de Dados:**
        *   Clique em "**criar o nome de ativos de dados**" e insira um nome como "**aluguel de bicicletas**".
         *   Adicione uma descrição como "**Dados históricos de aluguel de bicicletas**".
        *   Selecione "**tabular**" como tipo de dados e "**arquivo da web**" como fonte de dados.
        *   Insira a URL fornecida na documentação (essa URL contém os dados que serão usados no modelo).
        *   Aguarde a visualização dos dados ser carregada e clique em "**avançar**".
        *  Clique em "**Criar**" para criar os dados.
        *   Clique em "**Aluguel de Bicicletas**" e "**avançar**".
    *   **Configuração de Tarefas:**
        *   Verifique se o tipo de tarefa é "**regressão**" e o conjunto de dados é "**aluguel de bicicletas**".
        *   A coluna de destino é "**rental**".
         *   Em configurações adicionais, a métrica primária é "**raiz do erro quadrático médio normalizado**".
        *   Modelos permitidos: Reno e light.
    *   **Limites:**
        *   Preencha os campos de limites (3, 3, 0.085, 15, 15).
        *   Habilite o "**encerramento antecipado**".
        *   Em "**tipo de validação**" selecione "**divisão de validação**".
    *   Selecione "**sem servidor**" e clique em "**avançar**".
    *   Clique em "**enviar trabalho de treinamento**".
7.  **Acompanhar o Trabalho:**
    *   Aguarde a execução do trabalho de treinamento. O status deve mudar para "**completed**".
    *   Você pode acompanhar o progresso na guia "**jobs**".
8.  **Analisar Resultados:**
    *   Clique no nome do job para ver o histórico e detalhes do modelo.
    *   Valide as métricas para garantir a integridade do modelo.
    *   Explore os gráficos residuais e preditos.
9.  **Testar o Modelo:**
    *   Vá para a parte de modelos, selecione o modelo gerado e clique em "**pontos de extremidade**".
    *   Clique em "**testar**" e insira os dados de teste para verificar a previsão do modelo.

## Observações Importantes

*   **Tempo de Processamento:** O tempo para o modelo ser executado pode variar. Alguns passos podem levar alguns minutos para concluir.
*   **Documentação:** Siga a documentação do Microsoft Learning para garantir que todos os passos sejam seguidos corretamente.
*   **Exploração:** Explore o Machine Learning Studio e os recursos de inteligência artificial do Azure.

## Recursos Adicionais

- [Documentação do Azure Machine Learning](https://learn.microsoft.com/azure/machine-learning/)
- [Tutoriais e exemplos de código](https://learn.microsoft.com/azure/machine-learning/tutorials/)
- [Suporte da Comunidade Azure](https://learn.microsoft.com/azure/)
