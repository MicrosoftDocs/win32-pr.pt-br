---
title: Proxy de serviço
description: Um proxy de serviço é o proxy do lado do cliente para um serviço.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Serviços Web de proxy de serviço para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "105784042"
---
# <a name="service-proxy"></a>Proxy de serviço

Um proxy de serviço é o proxy do lado do cliente para um serviço. O proxy de serviço permite que os aplicativos enviem e recebam [mensagens](message.md) por um [canal](channel.md) como chamadas de método.

Os proxies de serviço são criados conforme necessário, abertos, usados para chamar um serviço e fechados quando não são mais necessários. Como alternativa, um aplicativo pode reutilizar um proxy de serviço para se conectar repetidamente ao mesmo serviço sem a despesa de tempo e os recursos necessários para initialising um proxy de serviço mais de uma vez. O diagrama a seguir ilustra o fluxo dos possíveis Estados do proxy de serviço e as chamadas de função ou os eventos que levam de um estado para outro.

![Diagrama mostrando os Estados de proxy de serviço e as chamadas de função ou eventos que levam de um estado para outro.](images/serviceproxystates.png)

Esses Estados de proxy de serviço são enumerados na enumeração de [**\_ estado do \_ proxy \_ de serviço WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .

Como o diagrama anterior e o código a seguir ilustram, um proxy de serviço é criado por uma chamada para a função [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) . Como parâmetros para essa chamada, WWSAPI fornece as seguintes enumerações:

-   [**\_tipo de canal do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [**Associação de WS \_ Channel \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

Ele também aceita parâmetros opcionais usando os seguintes tipos de dados:

-   [**\_ID da \_ Propriedade do proxy WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [**\_Descrição da segurança do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

Quando o proxy de serviço é criado, a função **WsCreateServiceProxy** retorna uma referência ao proxy de serviço, [o \_ \_ proxy de serviço WS](ws-service-proxy.md), por meio de um parâmetro out.

``` syntax
WS_SERVICE_PROXY* serviceProxy = NULL;
hr = WsCreateServiceProxy (
    WS_TCP_CHANNEL_BINDING, 
    WS_CHANNEL_TYPE_DUPLEX_SESSION, 
    NULL, 
    NULL, 
    0, 
    NULL,
    0,
    &serviceProxy, 
    error);
```

Quando o proxy de serviço tiver sido criado, o aplicativo poderá abrir o proxy de serviço para comunicação com um serviço chamando a função [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) , passando uma estrutura de [**endereço**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que contém o endereço de rede do ponto de extremidade de serviço ao qual se conectar.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

Quando o proxy de serviço é aberto, o aplicativo pode usá-lo para fazer chamadas para o serviço.

``` syntax
hr = Add(
    serviceProxy, 
    1, 
    2, 
    &result, 
    NULL, 
    0, 
    NULL, 
    error);
```

Quando o aplicativo não precisar mais do proxy de serviço, ele fechará o proxy de serviço chamando a função [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) . Ele também libera a memória associada chamando [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).

``` syntax
hr = WsCloseServiceProxy(
    serviceProxy, 
    NULL, 
    error);
```

``` syntax
hr = WsFreeServiceProxy(
    serviceProxy, 
    error);
```

## <a name="reusing-the-service-proxy"></a>Reutilizando o proxy de serviço

Como alternativa, depois de chamar [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) , um aplicativo pode reutilizar o proxy de serviço chamando a função [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) .

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

Para obter mais informações sobre como os proxies de serviço são usados em diferentes contextos, consulte os seguintes tópicos:

-   [Proxy de serviço e sessões](service-proxy-and-sessions.md)
-   [Operação de serviço](service-operation.md)
-   [Operações de serviço no lado do cliente](client-side-service-operations.md)
-   [HttpCalculatorClientExample](httpcalculatorclientexample.md)

### <a name="security"></a>Segurança

As considerações de design de aplicativo a seguir devem ser cuidadosamente observadas quando você usa a API de proxy do serviço WWSAPI:

-   O proxy de serviço não executará nenhuma validação dos dados além da validação básica do perfil 2,0 e da serialização XML. É responsabilidade do aplicativo validar os dados contidos nos parâmetros que recebe de volta como parte da chamada.
-   Configurando o número máximo de chamadas pendentes no proxy de serviço, usando o valor de enumeração [**WS \_ proxy \_ Property \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) **\_ unproxy WS \_ \_ Max \_ Pending \_**, fornece proteção contra um servidor em execução lenta. O máximo padrão é 100. Os aplicativos devem ter cuidado ao modificar os padrões.
-   O proxy de serviço não fornece nenhuma garantia de segurança além daquelas especificadas na estrutura de [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) usada para se comunicar com o servidor.
-   Tome cuidado ao modificar os padrões de [mensagem](message.md) e [canal](channel.md) no proxy de serviço. Leia as considerações de segurança associadas a mensagens e canais antes de modificar qualquer uma das propriedades relacionadas.
-   O proxy de serviço criptografa todas as credenciais que ele mantém na memória.

Os elementos da API a seguir estão relacionados a proxies de serviço.

| Callback                                                          | Description                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**\_retorno de \_ chamada de mensagem de proxy WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | Chamado quando os cabeçalhos da mensagem de entrada estão prestes a ser enviados por ou quando um cabeçalho de mensagem de saída é apenas recebido. |



 



| Enumeração                                                 | Descrição                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_ID da \_ propriedade da chamada WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | Enumera parâmetros opcionais para configurar uma chamada em uma operação de serviço no lado do cliente. |
| [**\_ID da \_ Propriedade do proxy WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | Enumera parâmetros opcionais para configurar o proxy de serviço.                         |
| [**\_estado do \_ proxy de serviço WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | O estado do proxy de serviço.                                                           |



 



| Função                                                       | Descrição                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | Abandona uma chamada especificada em um proxy de serviço especificado.                           |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | Cancela todas as entradas e saídas pendentes em um proxy de serviço especificado.                |
| [**WsCall**](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | Somente interno. Serializa os argumentos em uma mensagem e os envia pelo canal. |
| [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | Fecha um proxy de serviço para comunicação.                                         |
| [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | Cria um proxy de serviço.                                                          |
| [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | Libera a memória associada a um proxy de serviço.                              |
| [**WsGetServiceProxyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | Recupera uma propriedade de proxy de serviço especificada.                                     |
| [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | Abre um proxy de serviço para um ponto de extremidade de serviço.                                      |
| [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | Redefine o proxy de serviço.                                                             |



 



| Handle                                     | Description                                       |
|--------------------------------------------|---------------------------------------------------|
| [\_proxy de serviço WS \_](ws-service-proxy.md) | Um tipo opaco usado para fazer referência a um proxy de serviço. |



 



| Estrutura                                         | Description                 |
|---------------------------------------------------|-----------------------------|
| [**\_propriedade de chamada WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | Especifica uma propriedade de chamada.  |
| [**WS \_ \_propriedade de proxy**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property). | Especifica uma propriedade de proxy. |



 

 

 




