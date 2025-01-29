Documentação da API RobotsController

Introdução

Esta documentação descreve os endpoints disponíveis no controlador RobotsController, que faz parte da API do projeto Megaman. Este controlador gerencia operações relacionadas a robôs.

Endpoints

1. Listar todos os robôs

Rota: GET /api/v1/robots

Descrição:
Retorna uma lista de todos os robôs cadastrados.

Resposta de Sucesso:

Status: 200 OK

Corpo: Lista de objetos RobotReadDTO

2. Buscar robô por ID

Rota: GET /api/v1/robots/{id}

Parâmetros:

id (int): Identificador do robô a ser buscado.

Descrição:
Retorna um robô específico baseado no ID fornecido.

Resposta de Sucesso:

Status: 200 OK

Corpo: Objeto RobotReadDTO

Resposta de Erro:

Status: 404 Not Found

Corpo: { "message": "Nenhum robo encontrado" }

3. Criar um novo robô

Rota: POST /api/v1/robots

Descrição:
Endpoint responsável por criar um novo robô. No momento, este método apenas retorna um status 200 OK sem processar nenhum dado.

Resposta de Sucesso:

Status: 200 OK

Dependências

O RobotsController depende do serviço IRobotServices para manipular os dados dos robôs. Ele utiliza os seguintes métodos:

SearchAll(): Retorna todos os robôs cadastrados.

SearchById(int id): Retorna um robô pelo seu ID.

Observação

Este controlador está em fase inicial de desenvolvimento, e a criação de robôs ainda não está implementada completamente. Futuras melhorias podem incluir validação de entrada, atualização e remoção de robôs.