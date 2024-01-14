# ChatPHP

Essa aplicação e um Chat que vários clientes podem enviar mensagem através desse chat e receberem essa mensagem.

Ela é divida em 2 arquivos principais, service e o index.

O service, é responsável por criar uma conexão com todos clientes permitindo com que eles recebam e envie mensagem através do chat

O index é responsável por criar uma interface visual, onde eles poderam ler as mensagem enviadas, e inputar novas mensagem para enviar para todos os outros clientes.

## Service 
- O service é responsável realizar algumas coisas princiapis
-   Criar um main socket que irá ouvir todo novo clientes que se conectar a ele
-   Para cada novo client que se conecta, criamos um WebSocket I\O, e adicionamos na lista de clients
-   Enviamos a todos os clients a mensagem que uma nova conexão foi criada
-   Dentor do main loop, também lopamos por todas socket conectados e verificamos se eles receberam data, se sim, retornamos para o cliente
-   
