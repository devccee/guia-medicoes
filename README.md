# Envio e consulta de medições através da Plataforma de Integração
Ao realizar a integração entre sua aplicação e a CCEE através da Plataforma de Integração, o agente pode:

- Enviar dados de medição
- Consultar as medições
- Obter informações de um ponto de medição. 

## O que fazer para enviar dados de medições?

![Guia Medições - visão geral](./img/passos-informar-coleta.png)
 
### Implemente o endpoint para receber notificações

![Guia Medições - passo 1](./img/passo1.png)

Implemente uma interface RestAPI que irá receber o retorno da situação da coleta assim que a mesma for admitida ou recusada pela CCEE.

Os detalhes da API e exemplos de implementação, estão disponiveis no manual [Retornar Situação Coleta Medição](https://www.ccee.org.br/documents/80415/919484/Manual%20do%20Usu%C3%A1rio%20-%20Retornar%20Situacao%20Coleta%20Medicao.pdf/e0f36c42-4e4f-1d51-f283-85344ee40e5c).
 
--- 
 
### Envie os dados de medição

![Guia Medições - passo 2](./img/passo2.png)

Utilize o serviço *InformarColetaMedicao* para envio das coletas de medições através da Plataforma de Integração da CCEE.

[Clique aqui](https://documenter.getpostman.com/view/12351215/UzJJucpF#4f88fa78-50e2-4b53-993d-949b33476e8c) para ver exemplos de consulta utilizando a ferramenta Postman em seu  navegador.
    
Os campos de entrada e saída do serviço podem ser consultados no [manual de utilização](https://www.ccee.org.br/documents/80415/919484/Manual%20do%20Usu%C3%A1rio%20-%20Informar%20Coleta%20Medicao.pdf/e1239897-7981-b1ad-ca68-671645fbebf1) desse serviço. 

> Clique no botão abaixo e abra a configuração direto no Postman instalado em seu computador com os serviços da Plataforma de Integração, incluindo o Informar Coleta Medição
>
> [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/12351215-f6611483-5030-426a-9c05-c33102fa218c?action=collection%2Ffork&collection-url=entityId%3D12351215-f6611483-5030-426a-9c05-c33102fa218c%26entityType%3Dcollection%26workspaceId%3D0ed6d2fd-f92a-462d-8fbe-a353f67f0e6c)

---

### Receba as notificações enviadas pela CCEE

![Guia Medições - passo 3](./img/passo3.png)

A Plataforma de Integração da CCEE realizará apenas uma tentativa de requisição ao serviço exposto, no passo 1, e disponibilizado para receber a situação da coleta de medição enviada via Plataforma de Integração. 

Os detalhes da API e exemplos de implementação, estão disponiveis no manual [Retornar Situação Coleta Medição](https://www.ccee.org.br/documents/80415/919484/Manual%20do%20Usu%C3%A1rio%20-%20Retornar%20Situacao%20Coleta%20Medicao.pdf/e0f36c42-4e4f-1d51-f283-85344ee40e5c).

---

### Consulte o status do registro enviado

![Guia Medições - passo 4](./img/passo4.png)

Se desejado, é possível consultar o status de notificações enviadas. Á consulta está disponível através do serviço *Obter Situação Coleta Medição*.

[Clique aqui](https://documenter.getpostman.com/view/12351215/UzJJucpF#9c19abb5-6114-4ccf-9a50-0f834a6d17ea) para ver exemplos de consulta utilizando a ferramenta Postman em seu  navegador.

Os campos de entrada e saída do serviço podem ser consultados no [manual de utilização](https://www.ccee.org.br/documents/80415/919484/Manual%20do%20Usu%C3%A1rio%20-%20Obter%20Situacao%20Coleta%20Medicao.pdf/7736ea26-c9a6-a944-88f3-642a67c6cbd2) desse serviço. 

> Clique no botão abaixo e abra a configuração direto no Postman instalado em seu computador com os serviços da Plataforma de Integração, incluindo o Situação Coleta Medição
>
> [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/12351215-f6611483-5030-426a-9c05-c33102fa218c?action=collection%2Ffork&collection-url=entityId%3D12351215-f6611483-5030-426a-9c05-c33102fa218c%26entityType%3Dcollection%26workspaceId%3D0ed6d2fd-f92a-462d-8fbe-a353f67f0e6c)

## Como consultar os dados de medições ? 
Existem quatro formas de consultar as medidas registradas na CCEE através da Plataforma de Integração, são elas: 

- **Medida de 5 em 5 minutos** - permite a consulta de medidas consistidas em intervalos de 5 minutos.
    
    [Clique aqui](https://documenter.getpostman.com/view/12351215/UzJJucpF#2b083490-da52-4e77-a1d0-64251ab71bc2) para ver exemplos de consulta utilizando a ferramenta Postman em seu  navegador.
    
    Os campos de entrada e saída do serviço podem ser consultados no [manual de utilização](https://www.ccee.org.br/documents/80415/919484/ListarMedidaCincoMinutosBSv2.pdf/ef5c3678-4fe7-7216-eb34-af41a453d28b) desse serviço. 
    
    > Clique no botão abaixo e abra a configuração direto no Postman instalado em seu computador com os serviços da Plataforma de Integração, incluindo o Listar Medidas - 5 minutos
    >
    > [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/12351215-f6611483-5030-426a-9c05-c33102fa218c?action=collection%2Ffork&collection-url=entityId%3D12351215-f6611483-5030-426a-9c05-c33102fa218c%26entityType%3Dcollection%26workspaceId%3D0ed6d2fd-f92a-462d-8fbe-a353f67f0e6c)
    
- **Medida consolidada** - permite a consulta de medidas consolidadas. Esse serviço retorna através da Plataforma de Integração os mesmos dados do *relatorio de medidas consolidadas* no SCDE.

	>>> Você precisará obter o código do perfil do agente principal (do Agente Conectante ou do Agente Medição) para realizar a consulta. E ele deverá ser enviado no Header da requisição xml. O serviço Listar Ponto Medição fornece essa informação no retorno da sua consulta.

    [Clique aqui](https://documenter.getpostman.com/view/12351215/UzJJucpF#71673640-0991-4393-b998-9a4ca7451df2) para ver exemplos de consulta utilizando a ferramenta Postman em seu  navegador.
    
    Os campos de entrada e saída do serviço podem ser consultados no [manual de utilização](https://www.ccee.org.br/documents/80415/919484/ListarMedida.pdf/962fa85d-520c-adfa-09ae-b24ed6dfabbc) desse serviço. 
    
    > Clique no botão abaixo e abra a configuração direto no Postman instalado em seu computador com os serviços da Plataforma de Integração, incluindo o Listar Medidas consolidadas
    >
    > [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/12351215-f6611483-5030-426a-9c05-c33102fa218c?action=collection%2Ffork&collection-url=entityId%3D12351215-f6611483-5030-426a-9c05-c33102fa218c%26entityType%3Dcollection%26workspaceId%3D0ed6d2fd-f92a-462d-8fbe-a353f67f0e6c)
        
- **Medida faltante** - permite a consulta de períodos contendo dados faltantes.

	>>> Você precisará obter o código do perfil do agente principal (do Agente Conectante ou do Agente Medição) para realizar a consulta. E ele deverá ser enviado no Header da requisição xml. O serviço Listar Ponto Medição fornece essa informação no retorno da sua consulta.

    [Clique aqui](https://documenter.getpostman.com/view/12351215/UzJJucpF#3681fa17-a90c-4973-81f3-55379dee015c) para ver exemplos de consulta utilizando a ferramenta Postman em seu  navegador.
    
    Os campos de entrada e saída do serviço podem ser consultados no [manual de utilização](https://www.ccee.org.br/documents/80415/919484/ListarMedida.pdf/962fa85d-520c-adfa-09ae-b24ed6dfabbc) desse serviço. 
    
    > Clique no botão abaixo e abra a configuração direto no Postman instalado em seu computador com os serviços da Plataforma de Integração, incluindo o Listar Medidas faltantes
    >
    > [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/12351215-f6611483-5030-426a-9c05-c33102fa218c?action=collection%2Ffork&collection-url=entityId%3D12351215-f6611483-5030-426a-9c05-c33102fa218c%26entityType%3Dcollection%26workspaceId%3D0ed6d2fd-f92a-462d-8fbe-a353f67f0e6c)
        
- **Medida final** - permite a consulta de medidas finais. Esse serviço retorna através da Plataforma de Integração os mesmos dados do *relatorio origem de dados da coleta* no SCDE.

	>>> Você precisará obter o código do perfil do agente principal (do Agente Conectante ou do Agente Medição) para realizar a consulta. E ele deverá ser enviado no Header da requisição xml. O serviço Listar Ponto Medição fornece essa informação no retorno da sua consulta.

    [Clique aqui](https://documenter.getpostman.com/view/12351215/UzJJucpF#7e10d923-1451-47d5-b548-c7fd8336b8df) para ver exemplos de consulta utilizando a ferramenta Postman em seu  navegador.
    
    Os campos de entrada e saída do serviço podem ser consultados no [manual de utilização](https://www.ccee.org.br/documents/80415/919484/ListarMedida.pdf/962fa85d-520c-adfa-09ae-b24ed6dfabbc) desse serviço. 
    
    > Clique no botão abaixo e abra a configuração direto no Postman instalado em seu computador com os serviços da Plataforma de Integração, incluindo o Listar Medidas finais
    >
    > [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/12351215-f6611483-5030-426a-9c05-c33102fa218c?action=collection%2Ffork&collection-url=entityId%3D12351215-f6611483-5030-426a-9c05-c33102fa218c%26entityType%3Dcollection%26workspaceId%3D0ed6d2fd-f92a-462d-8fbe-a353f67f0e6c)
        
## Como consultar as informações do ponto de medição ? 
Você pode consultar as informações dos pontos de medição através dos serviços abaixo:

- **Listar pontos de medição por Agente** - esse serviço irá retornar a lista de pontos de medição associados ao código do perfil do agente informado.

    [Clique aqui](https://documenter.getpostman.com/view/12351215/UzJJucpF#750252ba-97c2-4d2c-9e91-10e934fd7950) para ver exemplos de consulta utilizando a ferramenta Postman em seu  navegador.
    
    Os campos de entrada e saída do serviço podem ser consultados no [manual de utilização](https://www.ccee.org.br/documents/80415/919484/ListarPontoMedicaoBSv2.pdf/eeeababc-8d3b-4a20-b484-4927d7e32450) desse serviço. 
    
    > Clique no botão abaixo e abra a configuração direto no Postman instalado em seu computador com os serviços da Plataforma de Integração, incluindo o Listar Ponto Medicao
    >
    > [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/12351215-f6611483-5030-426a-9c05-c33102fa218c?action=collection%2Ffork&collection-url=entityId%3D12351215-f6611483-5030-426a-9c05-c33102fa218c%26entityType%3Dcollection%26workspaceId%3D0ed6d2fd-f92a-462d-8fbe-a353f67f0e6c)
    
- **Obter Dados do Ponto de Medição** - caso queira saber mais informações de um ponto de medição especifico, esse serviço irá retornar todos os dados cadastrais do ponto de medição informado.

    [Clique aqui](https://documenter.getpostman.com/view/12351215/UzJJucpF#d711f15f-a4d3-44ca-9463-58b55d2a2f41) para ver exemplos de consulta utilizando a ferramenta Postman em seu  navegador.
    
	Os campos de entrada e saída do serviço podem ser consultados no [manual de utilização](https://www.ccee.org.br/documents/80415/919484/ObterPontoMedicaoBSv2.pdf/54818657-9bf7-b15f-c98d-ebca9fb2f9dd) desse serviço.
	
	> Clique no botão abaixo e abra a configuração direto no Postman instalado em seu computador com os serviços da Plataforma de Integração, incluindo o Obter Ponto Medicao
    >
    > [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/12351215-f6611483-5030-426a-9c05-c33102fa218c?action=collection%2Ffork&collection-url=entityId%3D12351215-f6611483-5030-426a-9c05-c33102fa218c%26entityType%3Dcollection%26workspaceId%3D0ed6d2fd-f92a-462d-8fbe-a353f67f0e6c)
    
- **Obter Dados do Ponto Mapeado** - caso queira saber mais informações de um ponto de medição especifico, esse serviço irá retornar todos os dados cadastrais do ponto mapeado no cadastro do SIGA, retornando informações complementares do serviço acima.

    [Clique aqui](https://documenter.getpostman.com/view/12351215/TVCdzTxD#874a60d9-aa95-453f-998a-e56cbccc2b08) para ver exemplos de consulta utilizando a ferramenta Postman em seu  navegador.
    
	Os campos de entrada e saída do serviço podem ser consultados no [manual de utilização](https://www.ccee.org.br/documents/80415/919484/ObterPontoMedicaoBSv2.pdf/54818657-9bf7-b15f-c98d-ebca9fb2f9dd) desse serviço.
	
	> Clique no botão abaixo e abra a configuração direto no Postman instalado em seu computador com os serviços da Plataforma de Integração, incluindo o Obter Ponto Mapeado
    >
    > [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/12351215-f6611483-5030-426a-9c05-c33102fa218c?action=collection%2Ffork&collection-url=entityId%3D12351215-f6611483-5030-426a-9c05-c33102fa218c%26entityType%3Dcollection%26workspaceId%3D0ed6d2fd-f92a-462d-8fbe-a353f67f0e6c)
	
