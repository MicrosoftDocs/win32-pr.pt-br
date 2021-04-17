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
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a><span data-ttu-id="01dfd-103">Criando manualmente um proxy de serviço para um serviço WCF</span><span class="sxs-lookup"><span data-stu-id="01dfd-103">Manually Creating a Service Proxy for a WCF Service</span></span>

<span data-ttu-id="01dfd-104">A maneira mais fácil de criar um proxy de serviço de cliente para um serviço de Windows Communication Foundation (WCF) é na camada de [modelo de serviço](service-model-layer-overview.md) com a ferramenta WsUtil, conforme descrito no tópico [criando um cliente](creating-a-client.md) .</span><span class="sxs-lookup"><span data-stu-id="01dfd-104">The easiest way to create a client service proxy for a Windows Communication Foundation (WCF) service is at the [Service Model](service-model-layer-overview.md) layer with the WsUtil tool, as described in the [Creating a Client](creating-a-client.md) topic.</span></span> <span data-ttu-id="01dfd-105">No entanto, se necessário, você também pode criar um proxy de serviço manualmente.</span><span class="sxs-lookup"><span data-stu-id="01dfd-105">However, if necessary, you can also create a service proxy manually.</span></span> <span data-ttu-id="01dfd-106">Essa API inclui uma função [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) para criar o proxy de serviço, bem como estruturas, enumerações e assim por diante para definir as propriedades necessárias para interoperar com o WCF.</span><span class="sxs-lookup"><span data-stu-id="01dfd-106">This API includes a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function for creating the service proxy as well as structures, enumerations, and so on for setting the properties necessary to interoperate with WCF.</span></span>

<span data-ttu-id="01dfd-107">O WCF fornece várias associações padrão, cada uma direcionada a um cenário de uso específico.</span><span class="sxs-lookup"><span data-stu-id="01dfd-107">WCF provides a number of standard bindings, each targeting a specific usage scenario.</span></span> <span data-ttu-id="01dfd-108">A associação do serviço que você está tentando se conectar a usa, por sua vez, determina quais propriedades de canal você precisa personalizar para que o proxy de serviço se comunique com o serviço.</span><span class="sxs-lookup"><span data-stu-id="01dfd-108">Which binding the service you are trying to connect to uses, in turn, determines which channel properties you need to customize for your service proxy to communicate with the service.</span></span>

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a><span data-ttu-id="01dfd-109">Criando um proxy de serviço para o WSHttpBinding do WCF</span><span class="sxs-lookup"><span data-stu-id="01dfd-109">Creating a Service Proxy for WCF's WSHttpBinding</span></span>

<span data-ttu-id="01dfd-110">WSHttpBinding é para o cenário de serviços Web da Internet principal.</span><span class="sxs-lookup"><span data-stu-id="01dfd-110">WSHttpBinding is for the mainline Internet web services scenario.</span></span> <span data-ttu-id="01dfd-111">Ele usa a versão mais recente do SOAP 1,2 e a versão 1,0 do WS-Addressing e habilita uma ampla gama de configurações de segurança nos transportes HTTP e HTTPS públicos.</span><span class="sxs-lookup"><span data-stu-id="01dfd-111">It uses the newer SOAP version 1.2 and WS-Addressing version 1.0 and enables a wide range of security settings over the public HTTP and HTTPS transports.</span></span> <span data-ttu-id="01dfd-112">O WWSAPI não tem um equivalente de WSHttpBinding (ou qualquer uma das associações padrão do WCF, para esse assunto), mas como sua versão padrão de SOAP, WS-Addressing versão e formato de codificação correspondem aos da WSHttpBinding, a criação de um proxy de serviço para um serviço que usa o WSHttpBinding é simples.</span><span class="sxs-lookup"><span data-stu-id="01dfd-112">WWSAPI does not have an equivalent of the WSHttpBinding (or any of the WCF standard bindings, for that matter), but since its default SOAP version, WS-Addressing version, and encoding format match those in WSHttpBinding, creating a service proxy for a service that uses the WSHttpBinding is straightforward.</span></span> <span data-ttu-id="01dfd-113">Por exemplo, para criar um proxy de serviço para se comunicar com um ponto de extremidade WSHttpBinding sem segurança, você pode simplesmente usar código como o seguinte trecho (declaração de variável, heap e criação de erro são omitidas).</span><span class="sxs-lookup"><span data-stu-id="01dfd-113">For example, to create a service proxy to talk to a WSHttpBinding endpoint without security, you can simply use code like following snippet (variable declaration, and heap and error creation are omitted).</span></span> <span data-ttu-id="01dfd-114">Observe que nenhuma propriedade de canal ou descrição de segurança é especificada na chamada para a função [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="01dfd-114">Notice that no channel properties or security description is specified in the call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span>


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



<span data-ttu-id="01dfd-115">A função cria o proxy de serviço e retorna um ponteiro para ele no parâmetro de Service- *proxy* (&proxy na chamada de função acima).</span><span class="sxs-lookup"><span data-stu-id="01dfd-115">The function creates the service proxy and returns a pointer to it in the *serviceProxy* parameter (&proxy in the function call above).</span></span>

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a><span data-ttu-id="01dfd-116">Criando um proxy de serviço para BasicHttpBinding do WCF</span><span class="sxs-lookup"><span data-stu-id="01dfd-116">Creating a Service Proxy for WCF's BasicHttpBinding</span></span>

<span data-ttu-id="01dfd-117">No entanto, quando você cria manualmente um proxy de serviço para um serviço WCF que usa uma associação BasicHttpBinding, é necessário definir a versão SOAP e as propriedades WS-Addressing do canal.</span><span class="sxs-lookup"><span data-stu-id="01dfd-117">When you manually create a service proxy for a WCF service that uses a BasicHttpBinding binding, however, it is necessary to set the SOAP version and WS-Addressing properties of the channel.</span></span> <span data-ttu-id="01dfd-118">Isso ocorre porque WWSAPI assume a versão de SOAP 1,2 e WS-Addressing 1,0.</span><span class="sxs-lookup"><span data-stu-id="01dfd-118">This is because WWSAPI defaults to SOAP version 1.2 and WS-Addressing 1.0.</span></span> <span data-ttu-id="01dfd-119">A BasicHttpBinding do WCF, por outro lado, usa SOAP versão 1,1 e nenhum WS-Addressing.</span><span class="sxs-lookup"><span data-stu-id="01dfd-119">WCF's BasicHttpBinding, on the other hand, uses SOAP version 1.1 and no WS-Addressing.</span></span>

<span data-ttu-id="01dfd-120">Para definir a versão SOAP e WS-Addrssing Propriedades do canal, declare uma matriz de estruturas [**de \_ \_ Propriedade do WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) para manter as propriedades do canal e informações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="01dfd-120">To set the SOAP version and WS-Addrssing properties of the channel, declare an array of [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) structures to hold the channel properties and related information.</span></span>


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



<span data-ttu-id="01dfd-121">Em seguida, passe a matriz de propriedades de canal (channelproperties) e a contagem de Propriedades (channelPropertyCount) para [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (ou [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) se você estiver trabalhando na camada de canal).</span><span class="sxs-lookup"><span data-stu-id="01dfd-121">Then pass the array of channel properties (channelProperties) and the count of properties (channelPropertyCount) to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (or [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) if you are working at channel layer).</span></span>


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



<span data-ttu-id="01dfd-122">A matriz que você declarou para conter as propriedades é copiada em **WsCreateServiceProxy** e, como resultado, você pode liberar a memória para a matriz de propriedades imediatamente após chamar a função.</span><span class="sxs-lookup"><span data-stu-id="01dfd-122">The array you declared to hold the properties is copied in **WsCreateServiceProxy**, and as a result, you can free the memory for the property array immediately after calling the function.</span></span> <span data-ttu-id="01dfd-123">Além disso, se você alocar a memória da pilha (como o trecho de código acima), também poderá retornar da função imediatamente após a chamada.</span><span class="sxs-lookup"><span data-stu-id="01dfd-123">Also, if you allocate the memory from the stack (like the code snippet above), you can also return from the function immediately after the call.</span></span>

## <a name="other-bindings"></a><span data-ttu-id="01dfd-124">Outras associações</span><span class="sxs-lookup"><span data-stu-id="01dfd-124">Other Bindings</span></span>

<span data-ttu-id="01dfd-125">Além disso, o WWSAPI fornece mecanismos para criar proxies de serviço para se comunicar com os serviços WCF usando outras associações, como NetTcpbinding e WSFederationHttpBinding.</span><span class="sxs-lookup"><span data-stu-id="01dfd-125">In addition, WWSAPI provides mechanisms for creating service proxies to communicate with WCF services using other bindings, such as NetTcpBinding and WSFederationHttpBinding.</span></span> <span data-ttu-id="01dfd-126">Muitas dessas associações exigem a definição de propriedades de canal adicionais, como descritores de segurança.</span><span class="sxs-lookup"><span data-stu-id="01dfd-126">Many of these binding require setting additional channel properties, such as security descriptors.</span></span> <span data-ttu-id="01dfd-127">Para obter exemplos que ilustram o uso de outras associações, consulte a seção [exemplos de serviços Web do Windows](windows-web-services-examples.md), em particular os [exemplos de camada de canal TCP](tcp-channel-layer-examples.md), [exemplos de camada de canal http](http-channel-layer-examples.md)e subseções [exemplos de camada de canal de segurança](security-channel-layer-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="01dfd-127">For examples that illustrate using other bindings, see the [Windows Web Services Examples](windows-web-services-examples.md), section, in particular the [TCP Channel Layer Examples](tcp-channel-layer-examples.md), [HTTP Channel Layer Examples](http-channel-layer-examples.md), and [Security Channel Layer Examples](security-channel-layer-examples.md) subsections.</span></span>

 

 




