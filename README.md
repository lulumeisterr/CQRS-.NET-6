# Implementando CQRS

# Sobre Padr�o CQRS (	Command Query Responsibility Segregation )

	A ideia do CQRS � segregar comandos e querys com responsabilidade. ou seja
	separar formas de gravar e escrever no banco, onde n�o � necess�rio 
	passar por N camadas apenas para ler um dado.

   - Comando : Tudo o que altera o estado de uma entidade ou seja (INSERT / UPDATE e Delete)
   - Query : � basicamente um select

   Vantagens :
    - Trabalhar com bases diferentes onde voc� pode ter um banco  que apenas grava e outro banco que apenas l�.
	- Evita DeadLocks, timeouts e lentid�o a partir do momento em que vc tem N servidores balanceados realizando I/O ao mesmo tempo.
	- Resolve problema de performace.
	- Dependendo do contexto n�o � necess�rio ter 2 bancos de dados, pois vc ainda tem o principio de responsabilidade e segrega��o onde o comando
	  sera passado por um handler para ser gravado no banco.
	- S� de passar por caminhos diferentes vc ja esta implementando um CQRS.
	- Facilita o trabalho com mensagerias. (Se vc estiver trabalhando sincrono n�o � necess�rio)
	- Possibilita trabalhar com o padr�o Event sourcing, onde vc detalha por logs do inicio ao fim da sua aplica��o

# Projeto












   https://www.youtube.com/watch?v=AQcsfIXQj18
   https://www.youtube.com/results?search_query=CQRS+.net+
