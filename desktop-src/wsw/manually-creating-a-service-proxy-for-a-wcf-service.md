---
title: Criando manualmente um proxy de serviço para um serviço WCF
description: A maneira mais fácil de criar um proxy de serviço de cliente para um serviço WCF (Windows Communication Foundation) é na camada modelo de serviço com a ferramenta WsUtil, conforme descrito no tópico Criando um cliente.
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33133ae48dee89e72871712d445453e237116f6f1fa08cf66a76381ea8d3d424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927246"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a>Criando manualmente um proxy de serviço para um serviço WCF

A maneira mais fácil de criar um proxy de serviço de cliente para [](service-model-layer-overview.md) um serviço do WCF (Windows Communication Foundation) é na camada modelo de serviço com a ferramenta WsUtil, conforme descrito no tópico Criando um [cliente.](creating-a-client.md) No entanto, se necessário, você também pode criar um proxy de serviço manualmente. Essa API inclui uma [**função WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) para criar o proxy de serviço, bem como estruturas, enumerações e assim por diante para definir as propriedades necessárias para interoperar com o WCF.

O WCF fornece várias vinculações padrão, cada uma visando um cenário de uso específico. A associação do serviço ao qual você está tentando se conectar usa, por sua vez, determina quais propriedades de canal você precisa personalizar para que o proxy de serviço se comunique com o serviço.

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a>Criando um proxy de serviço para WSHttpBinding do WCF

WSHttpBinding é para o cenário principal de serviços Web da Internet. Ele usa as versões SOAP 1.2 e WS-Addressing versão 1.0 mais recente e permite uma ampla variedade de configurações de segurança nos transportes HTTP e HTTPS públicos. O WWSAPI não tem um equivalente do WSHttpBinding (ou qualquer uma das vinculações padrão do WCF, para esse assunto), mas como sua versão soap padrão, a versão do WS-Addressing e o formato de codificação são correspondentes àqueles em WSHttpBinding, a criação de um proxy de serviço para um serviço que usa o WSHttpBinding é simples. Por exemplo, para criar um proxy de serviço para se falar com um ponto de extremidade WSHttpBinding sem segurança, você pode simplesmente usar código como o snippet a seguir (declaração de variável e criação de heap e erro são omitidos). Observe que nenhuma propriedade de canal ou descrição de segurança é especificada na chamada para a [**função WsCreateServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)


```C++
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        NULL, // channel properties
        0, // channel property count
        &proxy, 
        error);
```



A função cria o proxy de serviço e retorna um ponteiro para ele no parâmetro *serviceProxy* (&proxy na chamada de função acima).

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a>Criando um proxy de serviço para BasicHttpBinding do WCF

No entanto, quando você cria manualmente um proxy de serviço para um serviço WCF que usa uma associação BasicHttpBinding, é necessário definir a versão SOAP e WS-Addressing propriedades do canal. Isso porque o WWSAPI assume como padrão SOAP versão 1.2 e WS-Addressing 1.0. O BasicHttpBinding do WCF, por outro lado, usa SOAP versão 1.1 e nenhum WS-Addressing.

Para definir a versão SOAP e WS-Addrssing propriedades do canal, declare uma matriz de estruturas DE PROPRIEDADE CANAL [**\_ \_ do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) para manter as propriedades do canal e as informações relacionadas.


```
WS_CHANNEL_PROPERTY channelProperties[4]; // Array to hold up to 4 channel properties

ULONG channelPropertyCount = 0; // Count of properties set
 
WS_ENVELOPE_VERSION soapVersion = WS_ENVELOPE_VERSION_SOAP_1_1; // Set required SOAP version
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ENVELOPE_VERSION; // Type of first channel property
channelProperties[channelPropertyCount].value = &soapVersion; // Address of the SOAP version value
channelProperties[channelPropertyCount].valueSize = sizeof(soapVersion); // Size of the value
channelPropertyCount++; // Increment property count
 
WS_ADDRESSING_VERSION addressingVersion = WS_ADDRESSING_VERSION_TRANSPORT; // Set required WS-Addressing value
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ADDRESSING_VERSION; // Type of second channel property
channelProperties[channelPropertyCount].value = &addressingVersion ; // Address of the WS-Addressing value
channelProperties[channelPropertyCount].valueSize = sizeof(addressingVersion ); // Size of the value
channelPropertyCount++; // Increment property count
 
// add more channel properties here

```



Em seguida, passe a matriz de propriedades de canal (channelProperties) e a contagem de propriedades (channelPropertyCount) para [**o WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) [**(ou WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) se você estiver trabalhando na camada de canal).


```
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        channelProperties, // channel properties
        channelPropertyCount, // channel property count
        &proxy, 
        error);
```



A matriz que você declarou para manter as propriedades é copiada em **WsCreateServiceProxy** e, como resultado, você pode liberar a memória para a matriz de propriedades imediatamente após chamar a função. Além disso, se você alocar a memória da pilha (como o snippet de código acima), também poderá retornar da função imediatamente após a chamada.

## <a name="other-bindings"></a>Outras vinculações

Além disso, o WWSAPI fornece mecanismos para criar proxies de serviço para se comunicar com serviços WCF usando outras vinculações, como NetTcpBinding e WSFederationHttpBinding. Muitas dessas vinculações exigem a configuração de propriedades de canal adicionais, como descritores de segurança. Para exemplos que ilustram o uso de outras vinculações, consulte a seção [exemplos](windows-web-services-examples.md)de serviços Web Windows , em particular as subseções Exemplos de camada de canal [TCP](tcp-channel-layer-examples.md), [Exemplos](http-channel-layer-examples.md)de camada de canal HTTP e [Exemplos](security-channel-layer-examples.md) de camada de canal de segurança.

 

 




