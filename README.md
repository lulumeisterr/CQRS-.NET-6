# Implementando CQRS

# Sobre Padrão CQRS (	Command Query Responsibility Segregation )

	A ideia do CQRS é segregar comandos e querys com responsabilidade. ou seja
	separar formas de gravar e escrever no banco, onde não é necessário 
	passar por N camadas apenas para ler um dado.

   - Comando : Tudo o que altera o estado de uma entidade ou seja (INSERT / UPDATE e Delete)
   - Query : é basicamente um select

   Vantagens :
    - Trabalhar com bases diferentes onde você pode ter um banco  que apenas grava e outro banco que apenas lê.
	- Evita DeadLocks, timeouts e lentidão a partir do momento em que vc tem N servidores balanceados realizando I/O ao mesmo tempo.
	- Resolve problema de performace.
	- Dependendo do contexto não é necessário ter 2 bancos de dados, pois vc ainda tem o principio de responsabilidade e segregação onde o comando
	  sera passado por um handler para ser gravado no banco.
	- Só de passar por caminhos diferentes vc ja esta implementando um CQRS.
	- Facilita o trabalho com mensagerias. (Se vc estiver trabalhando sincrono não é necessário)
	- Possibilita trabalhar com o padrão Event sourcing, onde vc detalha por logs do inicio ao fim da sua aplicação

# Projeto












   https://www.youtube.com/watch?v=AQcsfIXQj18
   https://www.youtube.com/results?search_query=CQRS+.net+
