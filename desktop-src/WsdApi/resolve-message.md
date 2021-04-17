---
description: Uma WS-Discovery mensagem usada por um cliente para procurar serviços na rede por nome.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Resolver mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3390d97aad972f001b98587c6b5e7cd7ac708b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780278"
---
# <a name="resolve-message"></a><span data-ttu-id="317a2-103">Resolver mensagem</span><span class="sxs-lookup"><span data-stu-id="317a2-103">Resolve Message</span></span>

<span data-ttu-id="317a2-104">Uma mensagem de resolução é uma WS-Discovery mensagem usada por um cliente para procurar serviços na rede por nome.</span><span class="sxs-lookup"><span data-stu-id="317a2-104">A Resolve message is a WS-Discovery message used by a client to search for services on the network by name.</span></span> <span data-ttu-id="317a2-105">Um cliente só enviará uma mensagem de resolução quando uma mensagem HTTP (como uma solicitação de troca de metadados [Get](get--metadata-exchange--http-request-and-message.md) ou uma mensagem de serviço) for enviada.</span><span class="sxs-lookup"><span data-stu-id="317a2-105">A client will only send a Resolve message when an HTTP message (such as a [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange request or a service message) will be sent.</span></span> <span data-ttu-id="317a2-106">Para obter mais informações sobre como resolver mensagens, consulte a seção 6,1 da [especificação do WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).</span><span class="sxs-lookup"><span data-stu-id="317a2-106">For more information about Resolve messages, see section 6.1 of the [WS-Discovery Specification](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).</span></span>

<span data-ttu-id="317a2-107">Uma mensagem de resolução é enviada pelo multicast UDP para a porta 3702.</span><span class="sxs-lookup"><span data-stu-id="317a2-107">A Resolve message is sent by UDP multicast to port 3702.</span></span> <span data-ttu-id="317a2-108">Não há suporte para mensagens de resolução de unicast.</span><span class="sxs-lookup"><span data-stu-id="317a2-108">Unicast Resolve messages are not supported.</span></span>

<span data-ttu-id="317a2-109">Os clientes do DPWS enviam mensagens de resolução.</span><span class="sxs-lookup"><span data-stu-id="317a2-109">DPWS clients send Resolve messages.</span></span> <span data-ttu-id="317a2-110">A lista a seguir mostra cenários em que o WSDAPI enviará uma mensagem de resolução.</span><span class="sxs-lookup"><span data-stu-id="317a2-110">The following list shows scenarios in which WSDAPI will send a Resolve message.</span></span>

-   <span data-ttu-id="317a2-111">Um cliente de descoberta de função envia uma mensagem de resolução se nenhum XAddrs estiver incluído em uma mensagem [ProbeMatches](probematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="317a2-111">A Function Discovery client sends a Resolve message if no XAddrs are included in a [ProbeMatches](probematches-message.md) message.</span></span>
-   <span data-ttu-id="317a2-112">Um cliente que chama os métodos [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) enviará uma mensagem de resolução.</span><span class="sxs-lookup"><span data-stu-id="317a2-112">A client calling the [**IWSDiscoveryProvider::SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) methods will send a Resolve message.</span></span>
-   <span data-ttu-id="317a2-113">Um cliente que chama [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) pode enviar uma mensagem de resolução se um endereço de dispositivo lógico for passado para *pszDeviceId*.</span><span class="sxs-lookup"><span data-stu-id="317a2-113">A client calling [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) may send a Resolve message if a logical device address is passed to *pszDeviceId*.</span></span>
-   <span data-ttu-id="317a2-114">Um cliente que chama [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) enviará uma mensagem de resolução se a função for chamada com o parâmetro pDeviceAddress definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="317a2-114">A client calling [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) will send a Resolve message if the function is called with the pDeviceAddress parameter set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="317a2-115">Este tópico mostra uma mensagem DPWS de exemplo gerada por clientes e hosts WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="317a2-115">This topic shows a sample DPWS message generated by WSDAPI clients and hosts.</span></span> <span data-ttu-id="317a2-116">O WSDAPI analisará e aceitará outras mensagens em conformidade com o DPWS que não estão em conformidade com este exemplo.</span><span class="sxs-lookup"><span data-stu-id="317a2-116">WSDAPI will parse and accept other DPWS-compliant messages that do not conform to this sample.</span></span> <span data-ttu-id="317a2-117">Não use este exemplo para verificar a interoperabilidade do DPWS; em vez disso, use a [ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .</span><span class="sxs-lookup"><span data-stu-id="317a2-117">Do not use this sample to verify DPWS interoperability; use the [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) instead.</span></span>

 

<span data-ttu-id="317a2-118">A mensagem SOAP a seguir mostra uma mensagem de resolução de exemplo.</span><span class="sxs-lookup"><span data-stu-id="317a2-118">The following SOAP message shows a sample Resolve message.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery">
<soap:Header>
    <wsa:To>
urn:schemas-xmlsoap-org:ws:2005:04:discovery
</wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Resolve>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Resolve>
</soap:Body>
</soap:Envelope>
```

<span data-ttu-id="317a2-119">Uma mensagem de resolução tem os seguintes pontos de foco.</span><span class="sxs-lookup"><span data-stu-id="317a2-119">A Resolve message has the following focus points.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="317a2-120">Ponto de foco</span><span class="sxs-lookup"><span data-stu-id="317a2-120">Focus point</span></span></th>
<th><span data-ttu-id="317a2-121">XML</span><span class="sxs-lookup"><span data-stu-id="317a2-121">XML</span></span></th>
<th><span data-ttu-id="317a2-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="317a2-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="317a2-123">Resolver</span><span class="sxs-lookup"><span data-stu-id="317a2-123">Resolve</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td><span data-ttu-id="317a2-124">A ação resolver SOAP identifica a mensagem como uma mensagem de resolução.</span><span class="sxs-lookup"><span data-stu-id="317a2-124">The Resolve SOAP action identifies the message as a Resolve message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="317a2-125">MessageID</span><span class="sxs-lookup"><span data-stu-id="317a2-125">MessageID</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td><span data-ttu-id="317a2-126">Contém o identificador da mensagem, que é referenciado em uma mensagem <a href="resolvematches-message.md">ResolveMatches</a> .</span><span class="sxs-lookup"><span data-stu-id="317a2-126">Contains the message identifier, which is referenced in a <a href="resolvematches-message.md">ResolveMatches</a> message.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="317a2-127">Endereço</span><span class="sxs-lookup"><span data-stu-id="317a2-127">Address</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td><span data-ttu-id="317a2-128">Contém o endereço do ponto de extremidade que está sendo resolvido.</span><span class="sxs-lookup"><span data-stu-id="317a2-128">Contains the address of the endpoint being resolved.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="317a2-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="317a2-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="317a2-130">Descoberta e mensagens de troca de metadados</span><span class="sxs-lookup"><span data-stu-id="317a2-130">Discovery and Metadata Exchange Messages</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[<span data-ttu-id="317a2-131">Mensagem ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="317a2-131">ResolveMatches Message</span></span>](resolvematches-message.md)
</dt> </dl>

 

 



