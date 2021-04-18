---
description: AppSequence informações contidas em mensagens de anúncio e resposta do WS-Discovery (Olá, ProbeMatches e ResolveMatches).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Regras de validação do AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505707"
---
# <a name="appsequence-validation-rules"></a><span data-ttu-id="1254d-103">Regras de validação do AppSequence</span><span class="sxs-lookup"><span data-stu-id="1254d-103">AppSequence Validation Rules</span></span>

<span data-ttu-id="1254d-104">AppSequence informações contidas em mensagens de anúncio e resposta do WS-Discovery ([Olá](hello-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md)).</span><span class="sxs-lookup"><span data-stu-id="1254d-104">AppSequence information contained in WS-Discovery announcement and response messages ([Hello](hello-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md)).</span></span> <span data-ttu-id="1254d-105">Essas informações são processadas e validadas pelo WSDAPI antes que essas mensagens sejam passadas para os componentes acima da pilha (como o Gerenciador de rede ou um aplicativo chamando o WSDAPI).</span><span class="sxs-lookup"><span data-stu-id="1254d-105">This information is processed and validated by WSDAPI before these messages are passed on to components above the stack (such as Network Explorer or an application calling into WSDAPI).</span></span>

<span data-ttu-id="1254d-106">O XML a seguir mostra um exemplo de elemento AppSequence.</span><span class="sxs-lookup"><span data-stu-id="1254d-106">The following XML shows a sample AppSequence element.</span></span> <span data-ttu-id="1254d-107">O prefixo WSD refere-se ao namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="1254d-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

<span data-ttu-id="1254d-108">O WSDAPI ignora mensagens obsoletas.</span><span class="sxs-lookup"><span data-stu-id="1254d-108">WSDAPI ignores stale messages.</span></span> <span data-ttu-id="1254d-109">Para cada dispositivo (identificado exclusivamente pelo endereço do ponto de extremidade no corpo SOAP), o WSDAPI ignora todas as mensagens com um AppSequence MessageNumber inferior à última mensagem vista.</span><span class="sxs-lookup"><span data-stu-id="1254d-109">For each device (uniquely identified by the Endpoint Address in the SOAP Body), WSDAPI ignores any messages with an AppSequence MessageNumber lower than the last message seen.</span></span>

<span data-ttu-id="1254d-110">O WSDAPI ignora os anúncios de XAddr obsoletos.</span><span class="sxs-lookup"><span data-stu-id="1254d-110">WSDAPI ignores stale XAddr announcements.</span></span> <span data-ttu-id="1254d-111">Se a InstanceId AppSequence for menor do que a última InstanceId vista, o WSDAPI ignorará o XAddrs anunciado no corpo SOAP.</span><span class="sxs-lookup"><span data-stu-id="1254d-111">If the AppSequence InstanceId is lower than the last InstanceId seen, WSDAPI ignores the XAddrs advertised in the SOAP body.</span></span> <span data-ttu-id="1254d-112">Além disso, se a InstanceId for a mesma que a anterior, mas a MetadataVersion for menor do que a última MetadataVersion, o WSDAPI ignorará o XAddrs.</span><span class="sxs-lookup"><span data-stu-id="1254d-112">Also, if the InstanceId is the same as previous but the MetadataVersion is lower than the last MetadataVersion, WSDAPI ignores the XAddrs.</span></span>

<span data-ttu-id="1254d-113">O WSDAPI ignora mensagens de WS-Discovery duplicadas.</span><span class="sxs-lookup"><span data-stu-id="1254d-113">WSDAPI ignores duplicate WS-Discovery messages.</span></span> <span data-ttu-id="1254d-114">Se duas mensagens de WS-Discovery idênticas forem enviadas para WSDAPI, somente o primeiro recebimento será processado.</span><span class="sxs-lookup"><span data-stu-id="1254d-114">If two identical WS-Discovery messages are sent to WSDAPI, only the first received will be processed.</span></span> <span data-ttu-id="1254d-115">Isso geralmente é relevante apenas para aplicativos que chamam diretamente para as interfaces [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) ou [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) .</span><span class="sxs-lookup"><span data-stu-id="1254d-115">This is typically only relevant for applications that call directly into the [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) or [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1254d-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1254d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1254d-117">Padrões de mensagem de troca de metadados e descoberta</span><span class="sxs-lookup"><span data-stu-id="1254d-117">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



