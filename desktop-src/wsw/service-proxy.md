---
title: Proxy de Serviço
description: Um proxy de serviço é o proxy do lado do cliente para um serviço.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Serviços Web de Proxy de Serviço para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff23349545c47dde2a54ea0b0911d3f792f21778f5053628929d3a98c69b0f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026175"
---
# <a name="service-proxy"></a>Proxy de Serviço

Um proxy de serviço é o proxy do lado do cliente para um serviço. O proxy de serviço permite que os aplicativos enviem e [recebam mensagens](message.md) por um [canal como](channel.md) chamadas de método.

Os proxies de serviço são criados conforme necessário, abertos, usados para chamar um serviço e fechados quando não são mais necessários. Como alternativa, um aplicativo pode reutilizar um proxy de serviço para se conectar repetidamente ao mesmo serviço sem as despesas de tempo e recursos necessários para inicializar um proxy de serviço mais de uma vez. O diagrama a seguir ilustra o fluxo dos possíveis estados do proxy de serviço e as chamadas de função ou eventos que levam de um estado para outro.

![Diagrama mostrando os estados de proxy de serviço e as chamadas de função ou eventos que levam de um estado para outro.](images/serviceproxystates.png)

Esses estados de proxy de serviço são enumerados na [**enumeração WS \_ SERVICE PROXY \_ \_ STATE.**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state)

Como ilustra o diagrama anterior e o código a seguir, um proxy de serviço é criado por uma chamada para a [**função WsCreateServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) Como parâmetros para essa chamada, o WWSAPI fornece as seguintes enumerações:

-   [**TIPO DE \_ CANAL WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [**ASSOCIAÇÃO DE \_ CANAL \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

Ele também aceita parâmetros opcionais usando os seguintes tipos de dados:

-   [**ID DA \_ \_ PROPRIEDADE PROXY \_ DO WS**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [**DESCRIÇÃO DE SEGURANÇA DO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

Quando o proxy de serviço tiver sido criado, a **função WsCreateServiceProxy** retornará uma referência ao proxy de serviço, [ \_ \_ PROXY DE SERVIÇO WS,](ws-service-proxy.md)por meio de um parâmetro out.

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

Quando o proxy de serviço tiver sido criado, o aplicativo poderá abrir o proxy de serviço para [](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) comunicação com um serviço chamando a [**função WsOpenServiceProxy,**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) passando uma estrutura de endereços que contém o endereço de rede do ponto de extremidade de serviço ao que se conectar.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

Quando o proxy de serviço tiver sido aberto, o aplicativo poderá usá-lo para fazer chamadas ao serviço.

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

Quando o aplicativo não precisa mais do proxy de serviço, ele fecha o proxy de serviço chamando a [**função WsCloseServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) Ele também libera a memória associada chamando [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).

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

Como alternativa, depois de [**chamar WsCloseServiceProxy,**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) um aplicativo pode reutilizar o proxy de serviço chamando a [**função WsResetServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

Para obter mais informações sobre como os proxies de serviço são usados em contextos diferentes, consulte os seguintes tópicos:

-   [Proxy de serviço e sessões](service-proxy-and-sessions.md)
-   [Operação de serviço](service-operation.md)
-   [Operações de serviço do lado do cliente](client-side-service-operations.md)
-   [HttpCalculatorClientExample](httpcalculatorclientexample.md)

### <a name="security"></a>Segurança

As seguintes considerações de design de aplicativo devem ser cuidadosamente notadas quando você usa a API de proxy de serviço WWSAPI:

-   O proxy de serviço não executará nenhuma validação dos dados além da validação do Perfil Básico 2.0 e da serialização XML. É responsabilidade do aplicativo validar os dados contidos nos parâmetros que ele recebe de volta como parte da chamada.
-   Configurar o número máximo de chamadas pendentes no proxy de serviço, usando o valor de enumeração [**\_ de \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) DA PROPRIEDADE PROXY **WS WS \_ MAX \_ \_ \_ PENDING \_ CALLS**, fornece proteção contra um servidor em execução lenta. O máximo padrão é 100. Os aplicativos devem ter cuidado ao modificar os padrões.
-   O proxy de serviço não fornece nenhuma garantia de segurança além daquelas especificadas na estrutura [**WS \_ SECURITY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) usada para se comunicar com o servidor.
-   Tome cuidado ao modificar os padrões [de](message.md) mensagem [e](channel.md) canal no proxy de serviço. Leia as considerações de segurança associadas a mensagens e canais antes de modificar qualquer uma das propriedades relacionadas.
-   O proxy de serviço criptografa todas as credenciais que ele mantém na memória.

Os elementos de API a seguir estão relacionados a proxies de serviço.

| Callback                                                          | Descrição                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**RETORNO DE \_ CHAMADA DE MENSAGEM PROXY \_ \_ DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | Invocado quando os headers da mensagem de entrada estão prestes a ser enviados por meio de ou quando os headers de uma mensagem de saída são recebidos. |



 



| Enumeração                                                 | Descrição                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**ID DA \_ \_ PROPRIEDADE CALL \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | Enumera parâmetros opcionais para configurar uma chamada em uma operação de serviço do lado do cliente. |
| [**ID DA \_ \_ PROPRIEDADE PROXY \_ DO WS**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | Enumera parâmetros opcionais para configurar o proxy de serviço.                         |
| [**ESTADO DO \_ PROXY DO \_ SERVIÇO \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | O estado do proxy de serviço.                                                           |



 



| Função                                                       | Descrição                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | Abandonar uma chamada especificada em um proxy de serviço especificado.                           |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | Cancela todas as entradas e saídas pendentes em um proxy de serviço especificado.                |
| [**WsCall**](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | Somente interno. Serializa argumentos em uma mensagem e os envia pelo canal. |
| [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | Fecha um proxy de serviço para comunicação.                                         |
| [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | Cria um proxy de serviço.                                                          |
| [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | Libera a memória associada a um proxy de serviço.                              |
| [**WsGetServiceProxyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | Recupera uma propriedade de proxy de serviço especificada.                                     |
| [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | Abre um proxy de serviço para um ponto de extremidade de serviço.                                      |
| [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | Redefine o proxy de serviço.                                                             |



 



| Handle                                     | Descrição                                       |
|--------------------------------------------|---------------------------------------------------|
| [PROXY DE \_ SERVIÇO \_ WS](ws-service-proxy.md) | Um tipo opaco usado para referenciar um proxy de serviço. |



 



| Estrutura                                         | Descrição                 |
|---------------------------------------------------|-----------------------------|
| [**PROPRIEDADE \_ CALL \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | Especifica uma propriedade de chamada.  |
| [**WS \_ PROPRIEDADE \_ PROXY**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property). | Especifica uma propriedade de proxy. |



 

 

 




