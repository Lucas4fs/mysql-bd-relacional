<p align="center">
    <img src="imagensedocumentos\bda.png">
    <br>
    <h1 align="center">
    🗃️ BANCO DE DADOS RELACIONAL 🗃️
    </h1>
</p>
<br>
<h2>
    :mag: ACESSE O CÓDIGO DO PROJETO NO LINK ABAIXO
</h2>

```
https://github.com/Lucas4fs/mysql-bd-relacional/blob/main/ScriptIdentado.sql
``` 
<h3>
    :pushpin: Intuito do Projeto
</h3>

<p>
    Criar um banco de dados relacional do zero.<br>
</p>

<h3>
    :pushpin: Como Funciona esse Banco de Dados?
</h3>

<p>
    O banco de dados contém três tabelas.
    Tabela dos CLIENTES que armazena os dados dos clientes, tabela dos PRODUTOS que armazena os dados dos produtos e a tabela VENDAS que armazena os dados das vendas que foram feitas. 
</p>

<p>
    A tabela VENDAS se relaciona com as outras duas tabelas, trazendo dados dos PRODUTOS vendidos e dos CLIENTES que compraram os PRODUTOS.
</p>

<p>
    Mais abaixo existe um modelo relacional, para que a relação das tabelas seja entendida de forma mais didática:
</p>

<img src = "imagensedocumentos\MODELORELACIONAL.png">

<h3>
    :pushpin: Tipos de Linguagens de Banco de Dados que Serão Utilizadas
</h3>

<li>
    DQL(Linguagem de Consulta de Dados) - Permite recuperar informações específicas de um banco de dados relacional usando comandos SQL. Basicamente é o uso do SELECT(SELECIONAR).
</li>

<li>
    DDL(Linguagem de Definição de Dados) - Utilizada para definir a estrutura, organização e outras características dos dados armazenados em um banco de dados relacional. Os comandos DDL são responsáveis pela criação, modificação e exclusão dos objetos de banco de dados, tais como tabelas, colunas, índices, chaves estrangeiras, visões, entre outros. Eles não manipulam os dados propriamente ditos, apenas definem a forma como eles serão armazenados e organizados. Basicamente é o uso do CREATE(CRIAR), ALTER(ALTERAR) e DROP(DERRUBAR/APAGAR).
</li>

<li>
    DML (Linguagem de Manipulação de Dados) -  São utilizados para manipular os dados em um banco de dados ou seja, para inserir, atualizar ou excluir dados em uma tabela. Basicamente é o uso do INSERT(INSERIR), UPDATE(ATUALIZAR) e DELETE(DELETAR).
</li>

<h3>
    :pushpin: Observações Importantes
</h3>

<p>
    A cláusula * só será usada nesse projeto para economizar tempo na criação das consultas(seleções), mas vale lembrar que em um banco de dados empresarial não é aconselhável usar a cláusula *, isso pode interferir no desempenho do banco de dados, pois ao mencionar as colunas que queremos dentro da consulta o seletor já identifica as mesmas no primeiro momento, ao usar a cláusula * o seletor primeiro procura todas as colunas para depois trazer uma por uma, isso pode levar a uma sobrecarga de dados desnecessários, tornando a consulta mais lenta e consumindo mais recursos do sistema, aumentando a carga do processador e da memória. Em um banco de dados empresarial é aconselhável fazer a consulta mencionando as colunas desejadas para que essa consulta consuma menos processamento e menos memória.
</p>

<p>
    Vale lembrar também que caso algum código não funcione, basta remover os comentários e tentar rodar novamente que irá funcionar normalmente. A intenção de usar comentários nesse projeto é explicar oque cada linha de código está fazendo, mas os comentários podem acabar interferindo na sintaxe da instrução SQL, pois em alguns casos o MySQL interpreta o comentário como parte da string.
</p>

<h3>
    📌Início do Projeto Dentro do SGBD(Sistema de Gerenciamento de Banco de Dados) MySQL
</h3>

<p>
Abaixo serão apresentados os códigos usados para o desenvolvimento do projeto, mostrando do início ao fim como o banco foi criado e explicando qual a função de cada código.
</p>

<h3>
    ⛏️Criação do Banco de Dados
</h3>

<p>
    <img src = "imagensedocumentos\1-createdatabasempresa.png">
    <br>
    <img src = "imagensedocumentos\2-bdcriado.png">
</p>

<h3>
    ⛏️Criação da tabela CLIENTES dentro do banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\3-createtableempresaclientes.png"> 
</p>

<h3>
    ⛏️Criação da tabela PRODUTOS dentro do banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\4-createtableempresaprodutos.png"> 
</p>

<h3>
    ⛏️Criação da Tabela VENDAS Dentro do Banco EMPRESA
</h3>
<p>
    <img src = "imagensedocumentos\5-createtableempresavendas.png">
</p>

<h3>
    ⛏️Verificando se as Tabelas Foram Criadas
</h3>

<p>
    <img src = "imagensedocumentos\6-verificandotabelas.png">
</p>

<h3>
    📌Para que Serve uma CONSTRAINT(RESTRIÇÃO) ?
</h3>

<p>
Uma CONSTRAINT(RESTRIÇÃO) em um banco de dados é uma regra definida para impor limitações e restrições sobre os dados armazenados em uma tabela. As CONSTRAINTS(RESTRIÇÕES) ajudam a garantir que os dados inseridos em uma tabela estejam corretos e consistentes, protegendo a integridade dos dados e evitando erros e inconsistências.
</p>

<h3>
    📌Principais funções das CONSTRAINTS(RESTRIÇÕES):
</h3>


<li>
Garantir a integridade referencial: uma CONSTRAINT(RESTRIÇÃO) de chave estrangeira pode ser usada para garantir que os dados em uma tabela relacionada a outra tabela sejam consistentes e precisos.
</li>

<li>
Limitar valores aceitáveis: uma CONSTRAINT(RESTRIÇÃO) de verificação pode ser usada para restringir os valores que podem ser inseridos em uma coluna, garantindo que apenas valores aceitáveis sejam armazenados na tabela.
</li>

<li>
Impedir duplicatas: uma CONSTRAINT(RESTRIÇÃO) de chave única pode ser usada para garantir que não haja valores duplicados em uma coluna específica de uma tabela.
</li>

<li>
Impor restrições de integridade: uma CONSTRAINT(RESTRIÇÃO) de chave primária pode ser usada para garantir que cada registro em uma tabela seja exclusivo e que haja uma chave primária definida para cada registro.
</li>

<li>
Em resumo, as CONSTRAINTS(RESTRIÇÕES) são importantes para garantir a integridade dos dados em um banco de dados, evitando erros e inconsistências que podem comprometer a qualidade dos dados e a confiabilidade das informações armazenadas.
</li>

<h3>
    ⛏️Criando CONSTRAINTS(RESTRIÇÕES) de PRIMARY KEYS(CHAVES PRIMÁRIAS)
</h3>

<p>
    <img src = "imagensedocumentos\7-constraintpk.png">
</p>

<h3>
    ⛏️Alterando as Colunas das Tabelas Fazendo com que as PRIMARY KEYS(CHAVES PRIMÁRIAS) sejam Incrementadas Automaticamente
</h3>

<p>
    <img src = "imagensedocumentos\8-altertableidautoincrement.png"> 
</p>

<h3>
    ⛏️Fazendo Relação de Tabelas Tornando as Colunas Chaves Primárias
</h3>

<p>
    <img src = "imagensedocumentos\9-constraintfk.png"> 
</p>

<h3>
    📌Importância de Nomear as CONSTRAINTS(RESTRIÇÕES) que Tornam os ID's Chaves Estrangeiras
</h3>

<p>
    As CONSTRAINTS(RESTRIÇÕES) que tornam os ID's chaves entrangeiras ficam armazenadas dentro da tabela TABLE_CONSTRAINTS que fica dentro do banco INFORMATION_SCHEMA, este é um dos bancos criados automaticamente pelo MySQL para manter o funcionamento adequado do banco de dados. Nomear uma CONSTRAINT(RESTRIÇÃO) que cria uma chave estrangeira facilita o trabalho de procurar a  CONSTRAINT(RESTRIÇÃO) dentro da tabela TABLE_CONSTRAINTS, pois essa tabela armazena CONSTRAINTS(RESTRIÇÕES)s que também são criadas automaticamente pelo MySQL. Podemos inclusive fazer uma consulta dentro dessa tabela para encontrar a CONSTRAINT(RESTRIÇÃO).
</p>

<p>
    <img src = "imagensedocumentos\10-consultandotabelaconstraintsfk.png"> 
</p>

<h3>
    ⛏️Resultado
</h3>

<p>
    <img src = "imagensedocumentos\11-resultadodaconsulta.png"> 
</p>

<h3>
    ⛏️Criando Banco de Backup para Armazenar Dados que vem das TRIGGERS(GATILHOS)
</h3>

<p>
    <img src = "imagensedocumentos\12-createdatabaseempresabk.png">
    <br>
    <img src = "imagensedocumentos\13-bdempresabkpcriado.png">
</p>

<h3>
    ⛏️Criando Tabela que vai Armazenar Dados Inseridos Pela TRIGGER(GATILHO)
</h3>

<p>
    <img src = "imagensedocumentos\14-createtabledadosinseridosclientes.png"> 
</p>

<h3>
    ⛏️Para que Serve uma TRIGGER(GATILHO) ?
</h3>

<p>
Uma TRIGGER(GATILHO) é um objeto do banco de dados que é usado para executar automaticamente uma ação em resposta a determinados eventos que ocorrem no banco de dados. As TRIGGERS(GATILHOS) são usadas para automatizar processos de negócios, aplicar regras de negócios e manter a integridade dos dados.
</p>

<p>
As TRIGGERS(GATILHOS) podem ser definidas para executar em resposta a diferentes eventos, como a inserção, atualização ou exclusão de dados em uma tabela. As TRIGGERS(GATILHOS) podem ser usadas para realizar várias tarefas, como:
</p>

<li>
Validar dados: as TRIGGERS(GATILHOS) podem ser usadas para validar dados antes que eles sejam inseridos ou atualizados em uma tabela, garantindo que os dados sejam precisos e completos.
</li>

<li>
Atualizar dados: as TRIGGERS(GATILHOS) podem ser usadas para atualizar automaticamente os dados em uma tabela quando ocorre um evento, como a inserção ou atualização de dados em outra tabela.
</li>

<li>
Manter a integridade dos dados: as TRIGGERS(GATILHOS) podem ser usadas para garantir que os dados em uma tabela estejam sempre consistentes e corretos, evitando que valores inválidos ou duplicados sejam inseridos.
</li>

<li>
Realizar auditorias: as TRIGGERS(GATILHOS) podem ser usadas para registrar automaticamente eventos e alterações no banco de dados para fins de auditoria e rastreabilidade.
</li>

<p>
Em resumo, as TRIGGERS(GATILHOS) são usadas para automatizar processos de negócios e manter a integridade dos dados em um banco de dados. As TRIGGERS(GATILHOS) são úteis para reduzir a necessidade de intervenção manual em processos de negócios e para garantir que os dados armazenados no banco de dados sejam precisos e confiáveis.
</p>

<h3>
    ⛏️Criando TRIGGER(GATILHO) que faz Backup para a Tabela DADOS_INSERIDOS_CLIENTES do Banco EMPRESA_BKP depois de Inserir Dados na Tabela CLIENTES Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\15-createtriggerbkpclentesinseridos.png"> 
</p>

<h3>
    ⛏️Criando Tabela que Vai Armazenar Dados Depois do INSERT(INSERÇÃO) na Tabela PRODUTOS do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\16-createtableempresabkpdadosinseridosprodutos.png"> 
</p>

<h3>
    ⛏️Criando TRIGGER(GATILHO) que Faz Bakcup Para a Tabela DADOS_INSERIDOS_PRODUTOS Dentro do Banco de Dados EMPRESA_BKP Depois do INSERT(INSERÇÃO) na Tabela PRODUTOS do Banco de Dados EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\17-createtriggerempresabkpprodutosinseridos.png"> 
</p>

<h3>
    ⛏️Criando Tabela que Vai Armazenar Dados Depois do INSERT(INSERÇÃO) na Tabela VENDAS do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\18-createtableempresabkpdadosinseridosvendas.png"> 
</p>

<h3>
    ⛏️Criando TRIGGER(GATILHO) que Faz Bakcup Para a Tabela DADOS_INSERIDOS_VENDAS Dentro do Banco de Dados EMPRESA_BKP Depois do INSERT(INSERÇÃO) na Tabela VENDAS do Banco de Dados EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\19-createtriggerempresabkpvendasinseridos.png"> 
</p>

<h3>
    ⛏️Criando Tabela que Vai Armazenar Dados Antes do DELETE(DELETAR) na Tabela CLIENTES do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\20-createtableempresabkpdadosdeletadosclientes.png"> 
</p>

<h3>
    ⛏️Criando TRIGGER(GATILHO) que Faz Bakcup Para a Tabela DADOS_DELETADOS_CLIENTES Dentro do Banco de Dados EMPRESA_BKP Antes do DELETE(DELETAR) na Tabela CLIENTES do Banco de Dados EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\21-createtriggerempresabkpclientesdeletados.png"> 
</p>

<h3>
   ⛏️Criando Tabela que Vai Armazenar Dados Antes do DELETE(DELETAR) na Tabela PRODUTOS do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\22-createtableempresabkpdadosdeletadosprodutos.png"> 
</p>

<h3>
    ⛏️Criando TRIGGER(GATILHO) que Faz Bakcup Para a Tabela DADOS_DELETADOS_PRODUTOS Dentro do Banco de Dados EMPRESA_BKP Antes do DELETE(DELETAR) na Tabela PRODUTOS do Banco de Dados EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\23-createtriggerempresabkpprodutosdeletados.png"> 
</p>

<h3>
   ⛏️Criando Tabela que Vai Armazenar Dados Antes do DELETE(DELETAR) na Tabela VENDAS do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\24-createtableempresabkpdadosdeletadosvendas.png"> 
</p>

<h3>
   ⛏️Criando TRIGGER(GATILHO) que Faz Bakcup Para a Tabela DADOS_DELETADOS_VENDAS Dentro do Banco de Dados EMPRESA_BKP Antes do DELETE(DELETAR) na Tabela VENDAS do Banco de Dados EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\25-createtriggerempresabkpvendasdeletados.png"> 
</p>

<h3>
   ⛏️Criando Tabela que Vai Armazenar Dados Depois do UPDATE(ATUALIZAÇÃO) na Tabela CLIENTES do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\26-createtableempresabkpdadosatualizadosclientes.png"> 
</p>

<h3>
   ⛏️Criando TRIGGER(GATILHO) que Faz Bakcup Para a Tabela DADOS_ATUALIZADOS_CLIENTES Dentro do Banco de Dados EMPRESA_BKP Depois do UPDATE(ATUALIZAÇÃO) na Tabela CLIENTES do Banco de Dados EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\27-createtriggerempresabkpclientesatualizados.png"> 
</p>

<h3>
   ⛏️Criando Tabela que Vai Armazenar Dados Depois do UPDATE(ATUALIZAÇÃO) na Tabela PRODUTOS do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\28-createtableempresabkpdadosatualizadosprodutos.png"> 
</p>

<h3>
   ⛏️Criando TRIGGER(GATILHO) que Faz Bakcup Para a Tabela DADOS_ATUALIZADOS_PRODUTOS Dentro do Banco de Dados EMPRESA_BKP Depois do UPDATE(ATUALIZAÇÃO) na Tabela PRODUTOS do Banco de Dados EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\29-createtriggerempresabkpprodutosatualizados.png"> 
</p>

<h3>
   ⛏️Criando Tabela que Vai Armazenar Dados Depois do UPDATE(ATUALIZAÇÃO) na Tabela VENDAS do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\30-createtableempresabkpdadosatualizadosvendas.png"> 
</p>

<h3>
   ⛏️Criando TRIGGER(GATILHO) que Faz Bakcup Para a Tabela DADOS_ATUALIZADOS_VENDAS Dentro do Banco de Dados EMPRESA_BKP Depois do UPDATE(ATUALIZAÇÃO) na Tabela VENDAS do Banco de Dados EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\31-createtriggerempresabkpvendasatualizadas.png"> 
</p>

<h3>
   ⛏️Para que Serve uma PROCEDURE(PROCEDIMENTO) ?
</h3>

<p>
Uma PROCEDURE(PROCEDIMENTO) (também conhecida como PROC ou procedimento armazenado) é um objeto de banco de dados que contém um conjunto de instruções SQL que são agrupadas em uma única unidade lógica de trabalho. Ela é uma função que pode ser invocada por um programa ou script para realizar uma série de tarefas predefinidas no banco de dados.
</p>

<p>
As PROCEDURES(PROCEDIMENTOS) são úteis para uma variedade de tarefas, como:
</p>

<li>
Reutilização de código: Ao escrever as instruções SQL em uma PROCEDURE(PROCEDIMENTO), essas instruções podem ser reutilizadas em vários pontos do sistema de banco de dados, reduzindo a necessidade de duplicar o código.
</li>

<li>
Controle de acesso: As PROCEDURES(PROCEDIMENTOS) permitem que um administrador de banco de dados conceda e revogue privilégios de acesso a uma determinada PROCEDURE(PROCEDIMENTO), em vez de conceder privilégios de acesso às tabelas individuais do banco de dados.
</li>

<li>
Melhor desempenho: Ao invocar uma PROCEDURE(PROCEDIMENTO), o banco de dados pode armazenar a PROCEDURE(PROCEDIMENTO) em cache, permitindo que ela seja executada mais rapidamente em comparação com a execução de um conjunto de instruções SQL individuais.
</li>

<li>
Implementação de regras de negócios: As PROCEDURES(PROCEDIMENTOS) permitem que as regras de negócios sejam implementadas diretamente no banco de dados, garantindo que os dados estejam sempre de acordo com as políticas e regras da empresa.
</li>

<p>
Em resumo, uma PROCEDURE(PROCEDIMENTO) é uma maneira de agrupar um conjunto de instruções SQL em uma unidade lógica de trabalho que pode ser invocada por um programa ou script. As PROCEDURES(PROCEDIMENTOS) são úteis para melhorar o desempenho do banco de dados, implementar regras de negócios e controlar o acesso aos dados.
</p>

<h3>
    ⛏️Criando PROCEDURE(PROCEDIMENTO) que Insere Parâmetros com Dados Dentro da Tabela CLIENTES
</h3>

<p>
    <img src = "imagensedocumentos\32-createprocedureempresainsertabclientes.png"> 
</p>

<h3>
    ⛏️Chamando PROCEDURE(PROCEDIMENTO) e Inserindo Dados Dentro dos Parâmetros que Serão Inseridos na Tabela CLIENTES
</h3>

<p>
    <img src = "imagensedocumentos\33-callinserttabclientes.png"> 
</p>

<h3>
    ⛏️Fazendo SELECT(SELEÇÃO) para Visualizar os Dados Inseridos Dentro da Tabela CLIENTES
</h3>

<p>
    <img src = "imagensedocumentos\34-selectfromempresaclientes.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\35-resultadoselectfromempresaclientes.png"> 
</p>

<h3>
    ⛏️Criando PROCEDURE(PROCEDIMENTO) que Insere Parâmetros com Dados Dentro da Tabela PRODUTOS
</h3>

<p>
    <img src = "imagensedocumentos\36-createprocedureempresainserttabprodutos.png"> 
</p>

<h3>
   ⛏️Chamando PROCEDURE(PROCEDIMENTO) e Inserindo Dados Dentro dos Parâmetros que Serão Inseridos na Tabela PRODUTOS
</h3>

<p>
    <img src = "imagensedocumentos\37-callinserttabprodutos.png"> 
</p>

<h3>
    ⛏️Fazendo SELECT(SELEÇÃO) para Visualizar os Dados Inseridos Dentro da Tabela PRODUTOS
</h3>

<p>
    <img src = "imagensedocumentos\38-selectfromempresaprodutos.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\39-resultadoselectfromempresaprodutos.png"> 
</p>

<h3>
   ⛏️Criando PROCEDURE(PROCEDIMENTO) que Insere Parâmetros com Dados Dentro da Tabela VENDAS
</h3>

<p>
    <img src = "imagensedocumentos\40-createprocedureempresainserttabvendas.png"> 
</p>

<h3>
   ⛏️Chamando PROCEDURE(PROCEDIMENTO) e Inserindo Dados Dentro dos Parâmetros que Serão Inseridos na Tabela VENDAS
</h3>

<p>
    <img src = "imagensedocumentos\40.1-callinserttabvendas.png"> 
</p>

<h3>
   ⛏️Fazendo SELECT(SELEÇÃO) para Visualizar os Dados Inseridos Dentro da Tabela VENDAS
</h3>

<p>
    <img src = "imagensedocumentos\41-selectfromempresavendas.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\42-resultadoselectfromempresavendas.png"> 
</p>

<h3>
    ⛏️Fazendo SELECT(SELEÇÃO) para Ver se Houve Backup dos Dados Inseridos e se a TRIGGER(GATILHO) BKP_CLIENTES_INSERIDOS Funcionou
</h3>

<p>
    <img src = "imagensedocumentos\43-selectfromempresabkpdadosinseridosclientes.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\44-resultadoselecfromempresabkpdadosinseridosclientes.png"> 
</p>

<h3>
   ⛏️Fazendo SELECT(SELEÇÃO) para Ver se Houve Backup dos Dados Inseridos e se a TRIGGER(GATILHO) BKP_PRODUTOS_INSERIDOS Funcionou
</h3>

<p>
    <img src = "imagensedocumentos\45-selectfromempresabkpdadosinseridosprodutos.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\46-resultadoselectfromempresabkpdaddosinseridosprodutos.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\48-resultadoselectfromempresabkpdadosinseridosvendas.png"> 
</p>

<h3>
	⛏️Observações Importantes Antes de Iniciar os Comandos de DELETE(DELETAR).
</h3>

<p>
	Se for deletar um cliente e o mesmo estiver coligado a alguma venda na tabela VENDAS, primeiro é necessário deletar esse cliente da tabela VENDAS para depois deletar esse cliente da tabela CLIENTES.
</p>

<p>
	Se for deletar um produto e o mesmo estiver coligado a alguma venda na tabela VENDAS, primeiro é necessário deletar esse produto da tabela VENDAS para depois deletar esse produto da tabela PRODUTOS.
</p>

<h3>
    ⛏️Fazendo DELETE(DELETANDO) Dentro da Tabela VENDAS que Fica Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\49-deletefromempresavendaswhereidvendasbetween1and6.png"> 
</p>

<h3>
   ⛏️Fazendo DELETE(DELETANDO) Dentro da Tabela PRODUTOS que Fica Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\50-deletefromempresaprodutoswhereidprod3.png"> 
</p>

<h3>
   ⛏️Fazendo DELETE(DELETANDO) Dentro da Tabela CLIENTES que Fica Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\51-deletefromempresaclienteswhereidcliente1.png"> 
</p>

<h3>
    ⛏️Fazendo SELECT(SELEÇÃO) Dentro da Tabela CLIENTES Para Verificar se os Dados Foram Deletados
</h3>

<p>
    <img src = "imagensedocumentos\52-selectfromempresaclientes.png"> 
</p>

<h3>
    ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\53-resultadoselectfromempresaclientesdepoisdodelete.png"> 
</p>

<h3>
   ⛏️Fazendo SELECT(SELEÇÃO) Dentro da Tabela PRODUTOS Para Verificar se os Dados Foram Deletados
</h3>

<p>
    <img src = "imagensedocumentos\54-selectfromempresaprodutos.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\55-selecfromempresaprodutosresultado.png"> 
</p>

<h3>
   ⛏️Fazendo SELECT(SELEÇÃO) Dentro da Tabela VENDAS Para Verificar se os Dados Foram Deletados
</h3>

<p>
    <img src = "imagensedocumentos\56-selectfromempresavendas.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\57-selectfromempresavendasresultado.png"> 
</p>

<h3>
    ⛏️Fazendo SELECT(SELEÇÃO) Para Ver se Houve Backup dos Dados Deletados e se a TRIGGER(GATILHO) BKP_CLIENTES_DELETADOS Funcionou
</h3>

<p>
    <img src = "imagensedocumentos\58-selectfromempresabkpdadosdeletadosclientes.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\59-resultadoselectfromempresabkpdadosdeletadosclientes.png"> 
</p>

<h3>
   ⛏️Fazendo SELECT(SELEÇÃO) Para Ver se Houve Backup dos Dados Deletados e se a TRIGGER(GATILHO) BKP_PRODUTOS_DELETADOS Funcionou
</h3>

<p>
    <img src = "imagensedocumentos\60-selectfromempresabkpdadosdeletadosprodutos.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\61-resultadoselectfromempresabkpdadosdeletadosprodutos.png"> 
</p>

<h3>
   ⛏️Fazendo SELECT(SELEÇÃO) Para Ver se Houve Backup dos Dados Deletados e se a TRIGGER(GATILHO) BKP_VENDAS_DELETADOS Funcionou
</h3>

<p>
    <img src = "imagensedocumentos\61.1-selectfromempresabkpdadosdeletadosvendas.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\61.2-resultadoselectfromempresabkpdadosdeletadosvendas.png"> 
</p>

<h3>
    ⛏️Fazendo UPDATE(ATUALIZAÇÃO) Dentro da Tabela CLIENTES que Fica Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\62-updateempresaclientesset.png"> 
</p>

<h3>
    ⛏️Fazendo SELECT(SELEÇÃO) na Tabela DADOS_ATUALIZADOS_CLIENTES Dentro do Banco EMPRESA_BKP Para Visualizar se a TRIGGER(GATILHO) BKP_CLIENTES_ATUALIZADOS Funcionou
</h3>

<p>
    <img src = "imagensedocumentos\63-selectfromempresabkpdadosatualizadosclientes.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
+--+--+<br>
| ID | 1 |<br>
+--+--+
</p>
<p>
+----------------+<br>
| ID_CLIENTE     | 2 |<br>
+----------------+
</p>
<p>
+---------------------------+--------------------------+<br>
| ANTIGO_NOME_CLIENTE        | LUCAS ALFREDO MELO |<br>
+---------------------------+--------------------------+
</p>
<p>
+-------------------------+----------------+<br>
| NOVO_NOME_CLIENTE    | JULIA BONITA |<br>
+-------------------------+----------------+
</p>
<p>
+--------------+-----------------+<br>
| ANTIGO_CPF     | 456.965.445-42   |<br>
+--------------+-----------------+
</p>
<p>
+------------+-----------------+<br>
| NOVO_CPF       | 741.963.852-87   |<br>
+------------+-----------------+
</p>
<p>
+----------------+--+<br>
| ANTIGO_SEXO  | M          |<br>
+----------------+--+
</p>
<p>
+--------------+-+<br>
| NOVO_SEXO  | F        |<br>
+--------------+-+
</p>
<p>
+---------------+--------+<br>
| ANTIGO_PAIS  | BRASIL  |<br>
+---------------+--------+
</p>
<p>
+-------------+-------------+<br>
| NOVO_PAIS  | HONDURAS  |<br>
+-------------+-------------+
</p>
<p>
+-------------+----+<br>
| ANTIGO_UF  | GO |<br>
+-------------+----+
</p>
<p>
+----------+----+<br>
| NOVO_UF  | DF |<br>
+----------+----+
</p>
<p>
+------------------+------------+<br>
| ANTIGO_CIDADE  | ANAPOLIS   |<br>
+------------------+------------+
</p>
<p>
+----------------+---------------+<br>
| NOVO_CIDADE  | TAGUATINGA |<br>
+----------------+---------------+
</p>
<p>
+------------------+-------------+<br>
| ANTIGO_BAIRRO  | ANAPOLIM         |<br>
+------------------+-------------+
</p>
<p>
+----------------+------------------------+<br>
| NOVO_BAIRRO  | TAGUATINGA NORTE |<br>
+----------------+------------------------+
</p>
<p>
+----------------------+---------------------+<br>
| ANTIGO_ENDERECO | RUA 12 QUADRA 3 |<br>
+----------------------+---------------------+
</p>
<p>
+--------------------+-----------+<br>
| NOVO_ENDERECO  | QD 2 LT 5 |<br>
+--------------------+-----------+
</p>
<p>
+-------------------+--------------------+<br>
| ANTIGO_TEL_RES    | +55(62)3697-4477  |<br>
+-------------------+--------------------+
</p>
<p>
+-----------------+--------------------+<br>
| NOVO_TEL_RES     | +55(62)3369-4417 |<br>
+-----------------+--------------------+
</p>
<p>
+-------------------+----------------------+<br>
| ANTIGO_TEL_CEL    | +55(62)99999-4574 |<br>
+-------------------+----------------------+
</p>
<p>
+-----------------+----------------------+<br>
| NOVO_TEL_CEL | +55(61)99798-7847  |<br>
+-----------------+----------------------+<br>  
</p>  
<p>
+------------------------------+-----------------------+<br>
| DATA_HORA_ATUALIZACAO   | 2023-04-24 13:54:57 |<br>
+------------------------------+-----------------------+
</p>
<p>
+---------------------+-----------------+<br>
| QUEM_ATUALIZOU          | root@localhost     |<br>
+---------------------+-----------------+
</p>


<h3>
   ⛏️Fazendo UPDATE(ATUALIZAÇÃO) Dentro da Tabela PRODUTOS que Fica Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\65-updateempresaprodutos.png"> 
</p>

<h3>
   ⛏️Fazendo SELECT(SELEÇÃO) na Tabela DADOS_ATUALIZADOS_PRODUTOS Dentro do Banco EMPRESA_BKP Para Visualizar se a TRIGGER(GATILHO) BKP_PRODUTOS_ATUALIZADOS Funcionou
</h3>

<p>
    <img src = "imagensedocumentos\66-selectfromempresabkpdadosatualizadosprodutos.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\67-resultadoselectfromempresabkpdadosatualizadosprodutos.png"> 
</p>

<h3>
   ⛏️Fazendo UPDATE(ATUALIZAÇÃO) Dentro da Tabela VENDAS que Fica Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\68-updateempresavendas.png"> 
</p>

<h3>
   ⛏️Fazendo SELECT(SELEÇÃO) na Tabela DADOS_ATUALIZADOS_VENDAS Dentro do Banco EMPRESA_BKP Para Visualizar se a TRIGGER(GATILHO) BKP_VENDAS_ATUALIZADOS Funcionou
</h3>

<p>
    <img src = "imagensedocumentos\69-selectfromempresabkpdadosatualizadosvendas.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\70-resultadoselectfromempresabkpdadosatualizadosvendas.png"> 
</p>

<h3>
    ⛏️Para que serve uma VIEW(VISUALIZAÇÃO) ?
</h3>

<p>
Uma VIEW(VISUALIZAÇÃO) (visão ou visão virtual) é uma tabela virtual em um banco de dados relacional que não é armazenada fisicamente. Ela é uma consulta predefinida que retorna um conjunto específico de dados selecionados a partir de uma ou mais tabelas do banco de dados.
</p>

<p>
As VIEWS(VISUALIZAÇÕES)(VISUALIZAÇÕES) têm várias finalidades e benefícios, incluindo:
</p>

<p>
Simplificação das consultas: As VIEWS(VISUALIZAÇÕES) podem ser usadas para agrupar e simplificar as consultas complexas que envolvem várias tabelas do banco de dados. Em vez de escrever consultas longas e complexas, é possível criar VIEWS(VISUALIZAÇÕES) que retornem apenas as informações relevantes.
</p>

<p>
Segurança de dados: As VIEWS(VISUALIZAÇÕES) podem ser usadas para restringir o acesso a dados confidenciais em uma tabela do banco de dados. Por exemplo, uma VIEW(VISUALIZAÇÃO) pode ser criada para mostrar apenas as informações que os usuários têm permissão para acessar, ocultando os dados confidenciais.
</p>

<p>
Facilidade de manutenção: As VIEWS(VISUALIZAÇÕES) podem ser atualizadas facilmente sem afetar as tabelas subjacentes do banco de dados. Por exemplo, se uma tabela é renomeada ou suas colunas são alteradas, a VIEW(VISUALIZAÇÃO) pode ser atualizada para refletir essas alterações sem alterar a consulta original.
</p>

<p>
Desempenho: As VIEWS(VISUALIZAÇÕES) podem melhorar o desempenho do banco de dados, pois os dados são armazenados em cache e a consulta é pré-compilada. Isso significa que a VIEW(VISUALIZAÇÃO) pode ser acessada mais rapidamente do que uma consulta que precisa ser executada cada vez que é solicitada.
</p>

<p>
Em resumo, as VIEWS(VISUALIZAÇÕES) são consultas predefinidas que retornam um conjunto específico de dados selecionados a partir de uma ou mais tabelas do banco de dados. Elas têm várias finalidades, incluindo simplificar as consultas, aumentar a segurança de dados, facilitar a manutenção e melhorar o desempenho do banco de dados.
</p>

<h3>
   ⛏️Criando da VIEW(VISUALIZAÇÃO) REL_VENDAS queque Mostra qual Cliente Comprou qual Produto e qual Foi o Valor da Venda
</h3>

<p>
    <img src = "imagensedocumentos\72-createviewrelvendas.png"> 
</p>

<h3>
   ⛏️Selecionando a VIEW(VISUALIZAÇÃO) REL_VENDAS Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\73-selectfromempresalrelvendas.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\74-resultadoselectfromempresarelvendas.png"> 
</p>

<h3>
    ⛏️Exportando a VIEW(VISUALIZAÇÃO) REL_VENDAS que Está Dentro do Banco EMPRESA Para Dentro de uma Pasta, o Arquivo Fica no Formato .csv
    Dentro do Script Foi Passado Alguns Parâmetros Para que ao Abrir o Arquivo Dentro de Uma Planilha o Mesmo Já Venha Formatado
</h3>

<p>
    <img src = "imagensedocumentos\75-exportandoempresarelvendas.png"> 
</p>

<h3>
   ⛏️Segue o Print do Arquivo .csv Aberto Dentro do Excel
</h3>

<p>
    <img src = "imagensedocumentos\76-printdatabelarelvendasexportada.png"> 
</p>

<h3>
   ⛏️Segue o Link para Download do Arquivo .csv que Foi Gerado
</h3>

<p>
    <a href="imagensedocumentos\77-EMPRESA.REL_VENDAS.csv" download></a>
</p>

<h3>
    ⛏️Criando VIEW(VISUALIZAÇÃO) CALC_REL_VENDAS  que Mostra o Resultado de Alguns Cálculos Feitos na VIEW(VISUALIZAÇÃO) REL_VENDAS
</h3>

<p>
    <img src = "imagensedocumentos\78-createviewempresacalcrelvendas.png"> 
</p>

<h3>
   ⛏️Selecionando a VIEW(VISUALIZAÇÃO) CALC_REL_VENDAS Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\79-selectfromempresacalcrelvendas.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\80-resultadoselectfromempresacalcrelvendas.png"> 
</p>

<h3>
    ⛏️Exportando a VIEW(VISUALIZAÇÃO) CALC_REL_VENDAS que Está Dentro do Banco EMPRESA Para Dentro de uma Pasta, o Arquivo Fica no Formato .csv
    Dentro do Script Foi Passado Alguns Parâmetros Para que ao Abrir o Arquivo Dentro de Uma Planilha o Mesmo Já Venha Formatado
</h3>

<p>
    <img src = "imagensedocumentos\81-exportandoempresacalcrelvendas.png"> 
</p>

<h3>
   ⛏️Segue o Print do Arquivo .csv Aberto Dentro do Excel
</h3>

<p>
    <img src = "imagensedocumentos\82-printdatabelacalcrelvendasexportada.png"> 
</p>

<h3>
   ⛏️Segue o Link para Download do Arquivo .csv que Foi Gerado
</h3>

<p>
    https://drive.google.com/file/d/1pcBxkYb1vgfY7vvf3rtQe4ePxB9qNVvm/view?usp=share_link
</p>

<h3>
   ⛏️Criando VIEW(VISUALIZAÇÃO) RANKING_PROD_MAIS_VENDIDO que Mostra o Ranking dos Produtos Mais Vendidos
</h3>

<p>
    <img src = "imagensedocumentos\84-createviewrankingprodmaisvendido.png"> 
</p>

<h3>
   ⛏️Selecionando a VIEW(VISUALIZAÇÃO) RANKING_PROD_MAIS_VENDIDO que Está Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\85-selectfromempresarankingprodmaisvendido.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\86-resultadoselectfromempresarankingprodmaisvendido.png"> 
</p>

<h3>
    ⛏️Exportando a VIEW(VISUALIZAÇÃO) RANKING_PROD_MAIS_VENDIDO que Está Dentro do Banco EMPRESA Para Dentro de uma Pasta, o Arquivo Fica no Formato .csv.
    Dentro do Script Foi Passado Alguns Parâmetros Para que ao Abrir o Arquivo Dentro de Uma Planilha o Mesmo Já Venha Formatado
</h3>

<p>
    <img src = "imagensedocumentos\87-exportandoempresarankingprodmaisvendido.png"> 
</p>

<h3>
   ⛏️Segue o Print do Arquivo .csv Aberto Dentro do Excel
</h3>

<p>
    <img src = "imagensedocumentos\88-printdatabelaempresarankingprodmaisvendido.png"> 
</p>

<h3>
   ⛏️Segue o Link para Download do Arquivo .csv que Foi Gerado
</h3>

<p>
    https://drive.google.com/file/d/1XR-KxxTvzk5z6LISRaQWu7JA1yPzqWZ9/view?usp=share_link
</p>

<h3>
    ⛏️Criando VIEW(VISUALIZAÇÃO) RANKING_CLIENTES_QUE_MAIS_COMPRARAM que Mostra o Ranking dos Clientes que Mais Compraram
</h3>

<p>
    <img src = "imagensedocumentos\90-createviewrankingclientesquemaiscompraram.png"> 
</p>

<h3>
   ⛏️Selecionando a VIEW(VISUALIZAÇÃO) RANKING_CLIENTES_QUE_MAIS_COMPRARAM que Está Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\91-selectfromempresarakingclientesquemaiscompraram.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\92-resultadoselectfromempresarankingclientesquemaiscompraram.png"> 
</p>

<h3>
   ⛏️Segue o Print do Arquivo .csv Aberto Dentro do Excel
</h3>

<p>
    <img src = "imagensedocumentos\94-printdatabelanoexcelempresarankingclientesquemaiscompraram.png"> 
</p>

<h3>
   ⛏️Segue o Link para Download do Arquivo .csv que Foi Gerado
</h3>

<p>
    https://drive.google.com/file/d/1PtlGMjykdjalKukeOphemlz_gBN5B-ZM/view?usp=share_link
</p>

<h3>
   ⛏️Criando VIEW(VISUALIZAÇÃO) QTD_CLIENTE_POR_REGIAO que Mostra a Quantidade de Clientes por Região
</h3>

<p>
    <img src = "imagensedocumentos\96-createviewqtdclienteporregiao.png"> 
</p>

<h3>
    ⛏️Selecionando a VIEW(VISUALIZAÇÃO) QTD_CLIENTE_POR_REGIAO que Está Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\97-selectfromempresaqtdclienteporregiao.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\98-resultadoselectfromempresaqtdclienteporregiao.png"> 
</p>

<h3>
    ⛏️Exportando a VIEW(VISUALIZAÇÃO) QTD_CLIENTE_POR_REGIAO que Está Dentro do Banco EMPRESA Para Dentro de uma Pasta, o Arquivo Fica no Formato .csv
    Dentro do Script Foi Passado Alguns Parâmetros Para que ao Abrir o Arquivo Dentro de Uma Planilha o Mesmo Já Venha Formatado
</h3>

<p>
    <img src = "imagensedocumentos\99-exportandoviewempresaqtdclienteporregiao.png"> 
</p>

<h3>
    ⛏️Segue o Print do Arquivo .csv Aberto Dentro do Excel
</h3>

<p>
    <img src = "imagensedocumentos\100-printdatabelanoexcelempresaqtdclienteporregiao.png"> 
</p>

<h3>
   ⛏️Segue o Link para Download do Arquivo .csv que Foi Gerado
</h3>

<p>
    https://drive.google.com/file/d/1YIy1RBXBJ9ZpaWx4cmeAYR-ILaAYFkl9/view?usp=share_link
</p>

<h3>
    ⛏️Criando VIEW(VISUALIZAÇÃO) PROD_PRECO_ABAIXO_IGUAL_MD que Mostra os Produtos que Tem o Preço Abaixo ou Igual a Média
</h3>

<p>
    <img src = "imagensedocumentos\102-createviewprodprecoabaixoigualamedia.png"> 
</p>

<h3>
    ⛏️Selecionando a VIEW(VISUALIZAÇÃO) PROD_PRECO_ABAIXO_IGUAL_MD que Está Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\103-selectfromempresaprodprecoabaixoigualamedia.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\104-resultadoselectfromempresaprodprecoabaixoigualamedia.png"> 
</p>

<h3>
    ⛏️Exportando a VIEW(VISUALIZAÇÃO) PROD_PRECO_ABAIXO_IGUAL_MD que Está Dentro do Banco EMPRESA Para Dentro de uma Pasta, o Arquivo Fica no Formato .csv
    Dentro do Script Foi Passado Alguns Parâmetros Para que ao Abrir o Arquivo Dentro de Uma Planilha o Mesmo Já Venha Formatado
</h3>

<p>
    <img src = "imagensedocumentos\105-exportandoempresaprodutosprecoabaixoigualamedia.png"> 
</p>

<h3>
    ⛏️Segue o Print do Arquivo .csv Aberto Dentro do Excel
</h3>

<p>
    <img src = "imagensedocumentos\106-printdatabeladentrodoexcelempresaprodutosprecoabaixoigualamedia.png"> 
</p>

<h3>
   ⛏️Segue o Link para Download do Arquivo .csv que Foi Gerado
</h3>

<p>
    https://drive.google.com/file/d/1WdOABSafP0zuWqpTYa1GuD3c7hweAlqB/view?usp=share_link
</p>

<h3>
   ⛏️Criando VIEW(VISUALIZAÇÃO) PROD_PRECO_ACIMA_MD que Mostra os Produtos que Tem o Acima da Média
</h3>

<p>
    <img src = "imagensedocumentos\108-createviewprodprecoacimadamedia.png"> 
</p>

<h3>
   ⛏️Selecionando a VIEW(VISUALIZAÇÃO) PROD_PRECO_ACIMA_MD que Está Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\109-selectfromempresaprodprecoacimadamedia.png"> 
</p>

<h3>
    ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\110-resultadoselectfromempresaprodprecoacimadamedia.png"> 
</p>

<h3>
    ⛏️Exportando a VIEW(VISUALIZAÇÃO) PROD_PRECO_ACIMA_MD que Está Dentro do Banco EMPRESA Para Dentro de uma  Pasta, o Arquivo Fica no Formato .csv
    Dentro do Script Foi Passado Alguns Parâmetros Para que ao Abrir o Arquivo Dentro de Uma Planilha o Mesmo Já Venha Formatado
</h3>

<p>
    <img src = "imagensedocumentos\111-exportandoselectfromempresaprodprecoacimadamedia.png"> 
</p>

<h3>
   ⛏️Segue o Print do Arquivo .csv Aberto Dentro do Excel
</h3>

<p>
    <img src = "imagensedocumentos\112-printdatabelaexportadaempresaprodprecoacimamedia.png"> 
</p>

<h3>
   ⛏️Segue o Link para Download do Arquivo .csv que Foi Gerado
</h3>

<p>
    https://drive.google.com/file/d/1-J55bnvSSpE41LrcpXlfevrqA-t9NJj5/view?usp=share_link
</p>

<h3>
   ⛏️Criando VIEW(VISUALIZAÇÃO) CLIENTES_QUE_COMPRARAM_PROD_PRECO_ABAIXO_MD que Mostra os Clientes que Compraram Produtos com Preço Abaixo ou Igual da Média
</h3>

<p>
    <img src = "imagensedocumentos\114-createviewclientesquecompraramprodprecoabaixomd.png"> 
</p>

<h3>
    ⛏️Selecionando a VIEW(VISUALIZAÇÃO) CLIENTES_QUE_COMPRARAM_PROD_PRECO_ABAIXO_MD que Está Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\115-selectfromEMPRESA.CLIENTES_QUE_COMPRARAM_PROD_PRECO_ABAIXO_IGUAL_MD.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\116-resultadoselectfromclientesquecompraramprodprecoabaixomd.png"> 
</p>

<h3>
    ⛏️Exportando a VIEW(VISUALIZAÇÃO) CLIENTES_QUE_COMPRARAM_PROD_PRECO_ABAIXO_MD que Está Dentro do Banco EMPRESA Para Dentro de uma Pasta, o Arquivo Fica no Formato .csv
    Dentro do Script Foi Passado Alguns Parâmetros Para que ao Abrir o Arquivo Dentro de Uma Planilha o Mesmo Já Venha Formatado
</h3>

<p>
    <img src = "imagensedocumentos\117-exportandoviewEMPRESA.CLIENTES_QUE_COMPRARAM_PROD_PRECO_ABAIXO_IGUAL_MD.png"> 
</p>

<h3>
   ⛏️Segue o Print do Arquivo .csv Aberto Dentro do Excel
</h3>

<p>
    <img src = "imagensedocumentos\118-printdatabelaempresaclientesquecompraramprodprecoabaixoigualmd.png"> 
</p>

<h3>
   ⛏️Criando VIEW(VISUALIZAÇÃO) CLIENTES_QUE_COMPRARAM_PROD_PRECO_ACIMA_MD que Mostra os que Mostra os Clientes que Compraram Produtos com Preço Acima da Média
</h3>

<p>
    <img src = "imagensedocumentos\120-createviewclientesquecompraramprodprecoacimamd.png"> 
</p>

<h3>
    ⛏️Selecionando a VIEW(VISUALIZAÇÃO) CLIENTES_QUE_COMPRARAM_PROD_PRECO_ACIMA_MD que Está Dentro do Banco EMPRESA
</h3>

<p>
    <img src = "imagensedocumentos\121-selectfromempresaclientesquecompraramprodprecoacimamd.png"> 
</p>

<h3>
   ⛏️Resultado do SELECT(SELEÇÃO)
</h3>

<p>
    <img src = "imagensedocumentos\122-resultadoselectfromempresaclientesquecompraramprodprecoacimamd.png"> 
</p>

<h3>
    ⛏️Exportando a VIEW(VISUALIZAÇÃO) CLIENTES_QUE_COMPRARAM_PROD_PRECO_ACIMA_MD que Está Dentro do Banco EMPRESA Para Dentro de uma Pasta, o Arquivo Fica no Formato .csv
    Dentro do Script Foi Passado Alguns Parâmetros Para que ao Abrir o Arquivo Dentro de Uma Planilha o Mesmo Já Venha Formatado
</h3>

<p>
    <img src = "imagensedocumentos\123-exportandoselectfromempresaclientesquecompraramprodprecoacimamd.png"> 
</p>

<h3>
    ⛏️Segue o Print do Arquivo .csv Aberto Dentro do Excel
</h3>

<p>
    <img src = "imagensedocumentos\124-printdatabelaempresaclientesquecompraramprodprecoacimamd.png"> 
</p>

<h3>
   ⛏️Segue o Link para Download do Arquivo .csv que Foi Gerado
</h3>

<p>
    https://drive.google.com/file/d/1dKWR9fXODbyJlkQ53pBwRRjrwAG1BUqZ/view?usp=share_link
</p>