---
title: Criando manualmente um proxy de serviço para um serviço WCF
description: A maneira mais fácil de criar um proxy de serviço de cliente para um serviço de Windows Communication Foundation (WCF) é na camada de modelo de serviço com a ferramenta WsUtil, conforme descrito no tópico Criando um cliente.
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e061fda95298986ee6336dee0662d80c89a0a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813420"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a>Criando manualmente um proxy de serviço para um serviço WCF

A maneira mais fácil de criar um proxy de serviço de cliente para um serviço de Windows Communication Foundation (WCF) é na camada de [modelo de serviço](service-model-layer-overview.md) com a ferramenta WsUtil, conforme descrito no tópico [criando um cliente](creating-a-client.md) . No entanto, se necessário, você também pode criar um proxy de serviço manualmente. Essa API inclui uma função [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) para criar o proxy de serviço, bem como estruturas, enumerações e assim por diante para definir as propriedades necessárias para interoperar com o WCF.

O WCF fornece várias associações padrão, cada uma direcionada a um cenário de uso específico. A associação do serviço que você está tentando se conectar a usa, por sua vez, determina quais propriedades de canal você precisa personalizar para que o proxy de serviço se comunique com o serviço.

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a>Criando um proxy de serviço para o WSHttpBinding do WCF

WSHttpBinding é para o cenário de serviços Web da Internet principal. Ele usa a versão mais recente do SOAP 1,2 e a versão 1,0 do WS-Addressing e habilita uma ampla gama de configurações de segurança nos transportes HTTP e HTTPS públicos. O WWSAPI não tem um equivalente de WSHttpBinding (ou qualquer uma das associações padrão do WCF, para esse assunto), mas como sua versão padrão de SOAP, WS-Addressing versão e formato de codificação correspondem aos da WSHttpBinding, a criação de um proxy de serviço para um serviço que usa o WSHttpBinding é simples. Por exemplo, para criar um proxy de serviço para se comunicar com um ponto de extremidade WSHttpBinding sem segurança, você pode simplesmente usar código como o seguinte trecho (declaração de variável, heap e criação de erro são omitidas). Observe que nenhuma propriedade de canal ou descrição de segurança é especificada na chamada para a função [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) .


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



A função cria o proxy de serviço e retorna um ponteiro para ele no parâmetro de Service- *proxy* (&proxy na chamada de função acima).

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a>Criando um proxy de serviço para BasicHttpBinding do WCF

No entanto, quando você cria manualmente um proxy de serviço para um serviço WCF que usa uma associação BasicHttpBinding, é necessário definir a versão SOAP e as propriedades WS-Addressing do canal. Isso ocorre porque WWSAPI assume a versão de SOAP 1,2 e WS-Addressing 1,0. A BasicHttpBinding do WCF, por outro lado, usa SOAP versão 1,1 e nenhum WS-Addressing.

Para definir a versão SOAP e WS-Addrssing Propriedades do canal, declare uma matriz de estruturas [**de \_ \_ Propriedade do WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) para manter as propriedades do canal e informações relacionadas.


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



Em seguida, passe a matriz de propriedades de canal (channelproperties) e a contagem de Propriedades (channelPropertyCount) para [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (ou [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) se você estiver trabalhando na camada de canal).


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



A matriz que você declarou para conter as propriedades é copiada em **WsCreateServiceProxy** e, como resultado, você pode liberar a memória para a matriz de propriedades imediatamente após chamar a função. Além disso, se você alocar a memória da pilha (como o trecho de código acima), também poderá retornar da função imediatamente após a chamada.

## <a name="other-bindings"></a>Outras associações

Além disso, o WWSAPI fornece mecanismos para criar proxies de serviço para se comunicar com os serviços WCF usando outras associações, como NetTcpbinding e WSFederationHttpBinding. Muitas dessas associações exigem a definição de propriedades de canal adicionais, como descritores de segurança. Para obter exemplos que ilustram o uso de outras associações, consulte a seção [exemplos de serviços Web do Windows](windows-web-services-examples.md), em particular os [exemplos de camada de canal TCP](tcp-channel-layer-examples.md), [exemplos de camada de canal http](http-channel-layer-examples.md)e subseções [exemplos de camada de canal de segurança](security-channel-layer-examples.md) .

 

 




