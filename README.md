
Este repositório contém os códigos e dados utilizados no projeto de Iniciação Científica sobre a aplicação de restrições ambientais em modelos de otimização. Todas as análises foram implementadas na linguagem de programação Julia.

O objetivo deste documento é servir como um guia para a execução dos códigos e a reprodução dos resultados obtidos.

📂 Estrutura do Repositório
O projeto está organizado da seguinte forma:

Códigos sem restrições ambientais/: Contém o modelo iniciai que foi desenvolvido com base no modelo matemático original, sem a inclusão de restrições ambientais.

Códigos com restrições ambientais/: Apresenta o modelo final que incorpora as restrições ambientais.

Modelo Simples Programação Dinâmica/: Inclui um modelo automatizado que utiliza programação dinâmica para múltiplos meses e cenários, considerando o custo futuro. Este código pode servir de base para integrar a programação dinâmica ao modelo com restrições ambientais.

Dados Kenny/: Armazena os conjuntos de dados brutos (ex: arquivos .csv).


🚀 Como Executar o Projeto
Siga os passos abaixo para configurar e executar as análises em sua máquina local.

1. Pré-requisitos
É essencial ter o Julia instalado em seu sistema.

2. Instalação de Pacotes
O projeto depende de alguns pacotes do Julia. Para instalá-los, abra o terminal do Julia (REPL) e execute os seguintes comandos:

Julia

using Pkg

Pkg.add("DataFrames")
Pkg.add("CSV")
Pkg.add("JuMP")
Pkg.add("Gurobi") # Necessário apenas se for usar o solver Gurobi. O Highs já vem com o JuMP.
3. Configuração do Ambiente
Baixar o Projeto:
Clone ou baixe o repositório para a sua máquina local.

Modificar a Leitura dos Arquivos:
Nos scripts, a leitura de arquivos de dados precisa ser configurada corretamente. Siga estas instruções:

Mantenha os arquivos de dados em uma pasta dedicada para melhor organização.

Nos códigos, localize a linha onde os arquivos são lidos.

Copie o caminho absoluto do arquivo de dados em sua máquina (clique com o botão direito sobre o arquivo e selecione "Copiar como caminho").

Cole o caminho no local indicado no código e substitua todas as barras invertidas (\) por barras normais (/).

Exemplo:

Julia

// Antes
dados = CSV.read("C:\\Users\\SeuUsuario\\Projeto\\dados.csv", DataFrame)

// Depois
dados = CSV.read("C:/Users/SeuUsuario/Projeto/dados.csv", DataFrame)
4. Executando o Código
Após a configuração, basta executar o arquivo Julia desejado.

Observação sobre o Solver: Se você não possui uma licença do Gurobi, pode utilizar o solver open-source HiGHS, que já vem integrado ao JuMP. Para isso, certifique-se de que o modelo JuMP esteja configurado para usar o HiGHS.

Exemplo de como definir o solver:

Julia

using JuMP, HiGHS

// Ao criar o modelo
model = Model(HiGHS.Optimizer)
Certifique-se de trocar Gurobi.Optimizer por HiGHS.Optimizer nos scripts.
