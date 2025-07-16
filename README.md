Este projeto foi desenvolvido como parte do *Desafio Jovem Tech (Grupo Mateus)*. O objetivo é criar uma ferramenta para otimizar a gestão de estoque de frango, utilizando um modelo de previsão de vendas para automatizar a decisão de retirada do produto do congelador, visando minimizar perdas e maximizar a disponibilidade.

## 📊 O Dashboard

O coração do projeto é um dashboard interativo onde o gerente pode visualizar dados históricos, acompanhar as previsões e simular as operações diárias.

## ✨ Funcionalidades Principais

* *Previsão de Vendas*: Utiliza o modelo Prophet para prever a demanda futura de vendas com base em dados históricos.
* *Simulação de Estoque*: Simula o ciclo de vida do produto: retirada do congelador, descongelamento, disponibilidade para venda, venda real e perdas por validade.
* *Dashboard Interativo*: Uma interface amigável construída com Streamlit para visualizar KPIs (Indicadores Chave de Desempenho), gráficos de perdas, custos e tendências de vendas.
* *Tomada de Decisão Automatizada*: O sistema recomenda a quantidade exata de frango a ser descongelada para os próximos dias, com base nas previsões e no estoque atual.

## 📂 Estrutura do Repositório
* README.md:
    * Este arquivo contém a documentação e o guia do projeto.
* dashboard_simulacao.py:
    * Este é o arquivo principal do projeto. Ele contém o código do dashboard interativo. Para rodar a aplicação, execute este script.
* simulador.py:
    * Contém toda a lógica de negócio da simulação. É responsável por calcular as perdas, as sobras e a necessidade de descongelamento com base na venda informada no dashboard.
* dados.csv:
    * A planilha com os *dados históricos de vendas*. É a fonte de informação essencial para treinar o modelo de previsão.
* estado_estoque.csv:
    * Arquivo gerado e atualizado pela simulação. Ele salva o "estado" do estoque a cada dia (o que está pronto para venda, o que está descongelando, etc.). É o "histórico" da simulação.
* relatorio_previsoes.csv:
    * Arquivo gerado pela simulação que contém as previsões de venda e as necessidades de estoque para os dias futuros. É a fonte de dados principal para os gráficos do dashboard.
* requirements.txt:
    * Lista todas as bibliotecas Python necessárias para que o projeto funcione corretamente.

## 🚀 Executando o Projeto

Siga os passos abaixo para rodar o dashboard na sua máquina.

*1. Clone o Repositório:*
bash
git clone https://github.com/luizcarlos001/DashboardFinal-JT.git
cd DashboardFinal-JT

*2. Instale as Dependências:*
bash
# Instale todas as bibliotecas listadas em 'requirements.txt'
pip install -r requirements.txt


*3. Execute o Dashboard:*
bash
streamlit run dashboard_simulacao.py


*4. Acesse o Dashboard:*
Após executar o comando, o seu navegador abrirá automaticamente no endereço da dashboard.

*Credenciais para acesso:*
* Usuário: gerente
* Senha: 1234

Na barra lateral, você poderá inserir a venda real de um dia e clicar em "Executar Próximo Dia" para avançar na simulação e ver os resultados atualizados.
