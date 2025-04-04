//Comando para executar o protoc
protoc --go_out=. --go-grpc_out=. internal/infra/grpc/protofiles/order.proto

//para iniciar o servidor grpc para rodar as queries use o seguinte comando:

evans -r repl

//Para executar os endpoints do grpc

- Selecione o package: `package pb`

- Selecione o service: `service {nome-do-service}`

- Faça a chamada: `call {nome-do-endpoints}`

//Para executar o endpoint de graphql

- Acesse: `localhost:8080`

Utilize a seguinte estrutura;

`mutation createOrder {
  createOrder(input: {
    id: "ccc",
    Price: 100,
    Tax: 0.2
  }){
    id
    Price
    Tax
    FinalPrice
  }
}`