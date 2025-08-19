IC - Modelos de Otimização com Restrições Ambientais
Este repositório contém os códigos e dados utilizados na Iniciação Científica sobre restrições ambientais, com análises implementadas na linguagem Julia. O objetivo deste documento é guiar a execução e reprodução dos resultados.

Estrutura do Repositório
O projeto está organizado da seguinte forma:

/Códigos sem restrições ambientais: Primeiros modelos inspirados no modelo matemático desenvolvido.
/Códigos com restrições ambientais: Modelo que considera a utilização das restrições ambientais.
/Modelo Simples Programação Dinâmica: Modelo automatizado para n meses e n cenários com o custo futuro. Pode ser usado de base para adicionar a programação dinâmica no arquivo com restrições ambientais.
/Dados Kenny: Contém os conjuntos de dados brutos fornecidos pelo Kenny (ex: .csv).
README.md: Este arquivo de instruções.
Como Executar o Projeto
Siga os passos abaixo para executar as análises em sua máquina local.

1. Pré-requisitos
É necessário ter o Julia instalado na sua máquina.

Além disso, o projeto utiliza alguns pacotes. Para instalá-los, abra o terminal do Julia (REPL) e execute os seguintes comandos:

using Pkg
Pkg.add("DataFrames")
Pkg.add("CSV")
Pkg.add("JuMP")
Pkg.add("Gurobi") #Se for usar esse solver. O Highs já vem com o JuMP
2. Baixar
Baixe todos os arquivos ou o próprio projeto na máquina, para que os códigos possam ser utilizados.

3. Modificar a leitura dos arquivos
Durante códigos maiores, haverá uma leitura de arquivos. Para que ela possa ser usada é preciso que:

Os dados estejam organizados em uma pasta para fins de uma melhor visualização
Uma vez na pasta, pegue o arquivo, aperte o botão direito e utilize a opção "Copiar como caminho"
Cole o caminho copiado no lugar de leitura e substitua a barra invertida () pela barra (/)
Troque o "Gurobi" por "HiGHS" se não for usar o Gurobi
O arquivo está pronto para ser executado
