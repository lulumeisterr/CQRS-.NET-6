# Command :
  Reponsavel por expressar uma intenção de responsabilidade unica, como Inserir , Remover e atualizar.
  - Validação (Utilização Fluent Validator): Responsavel por Receber um comando(entidade de tipo generico) e validar seus atributos de requisição.

# CommandHandler :
   Responsavel por manipular tipos de comando que alteram o estado da entidade.
   - Para cada command a ser implementado nos precisamos ter um Handler
   - Verificamos se o comando é valido caso contrario devemos lançar uma notificação
   - Apos validar o comando devemos receber ele em uma entidade
   - Chamar o repositorio
   - Realizar o commit, adicionar regras de validacao para que so seja commitado caso não tenha nenhum erro/notifications do fluent validator
   - Retornar o status da gravação no banco caso contrario lancamos uma notificacao de erro.

# Referencias
   https://www.youtube.com/watch?v=noda1ox6NeA
   https://medium.com/codigorefinado/bolovo-voc%C3%AA-conhece-esse-modelo-de-arquitetura-de-software-1590c778f394
   https://www.learmoreseekmore.com/2021/03/dotnet5-sample-cqrs-mediatr-pattern.html
