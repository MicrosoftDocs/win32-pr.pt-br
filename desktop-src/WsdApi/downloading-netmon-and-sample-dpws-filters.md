---
description: O Monitor de Rede da Microsoft 3 (Netmon) é um analisador de pacotes usado para inspecionar o tráfego de rede.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Baixando os filtros de DPWS e de exemplo do Netmon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788951"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a><span data-ttu-id="6bba3-103">Baixando os filtros de DPWS e de exemplo do Netmon</span><span class="sxs-lookup"><span data-stu-id="6bba3-103">Downloading Netmon and Sample DPWS Filters</span></span>

<span data-ttu-id="6bba3-104">O Monitor de Rede da Microsoft 3 (Netmon) é um analisador de pacotes usado para inspecionar o tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="6bba3-104">Microsoft Network Monitor 3 (Netmon) is a packet analyzer used to inspect network traffic.</span></span> <span data-ttu-id="6bba3-105">O Netmon deve ser baixado antes das etapas de solução de problemas fornecidas na [inspeção de rastreamentos de rede para a descoberta de UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) e [inspeção de rastreamentos de rede para que o intercâmbio de metadados http](inspecting-network-traces-for-http-metadata-exchange.md) possa ser seguido.</span><span class="sxs-lookup"><span data-stu-id="6bba3-105">Netmon must be downloaded before the troubleshooting steps given in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) can be followed.</span></span> <span data-ttu-id="6bba3-106">Após o download do Netmon, os filtros DPWS podem ser usados para ajudar a isolar o tráfego de interesse.</span><span class="sxs-lookup"><span data-stu-id="6bba3-106">After Netmon has been downloaded, DPWS filters can be used to help isolate traffic of interest.</span></span>

## <a name="downloading-netmon"></a><span data-ttu-id="6bba3-107">Baixando o Netmon</span><span class="sxs-lookup"><span data-stu-id="6bba3-107">Downloading Netmon</span></span>

<span data-ttu-id="6bba3-108">Para baixar o Netmon, vá para [Monitor de rede da Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) e siga as instruções.</span><span class="sxs-lookup"><span data-stu-id="6bba3-108">To download Netmon, go to [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) and follow the instructions.</span></span> <span data-ttu-id="6bba3-109">Para obter mais informações sobre o Netmon, consulte "informações sobre o Monitor de Rede 3,0" na base de dados de conhecimento de ajuda e suporte em [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="6bba3-109">For more information about Netmon, see "Information about Network Monitor 3.0" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

## <a name="sample-dpws-filters"></a><span data-ttu-id="6bba3-110">Filtros de DPWS de exemplo</span><span class="sxs-lookup"><span data-stu-id="6bba3-110">Sample DPWS Filters</span></span>

<span data-ttu-id="6bba3-111">Às vezes, a solução de problemas de WS-Discovery e troca de metadados deve ocorrer em uma rede ocupada.</span><span class="sxs-lookup"><span data-stu-id="6bba3-111">Sometimes, WS-Discovery and metadata exchange troubleshooting must take place on a busy network.</span></span> <span data-ttu-id="6bba3-112">Os filtros de exemplo podem ser usados para ajudar a limitar a saída do Netmon ao tráfego de interesse.</span><span class="sxs-lookup"><span data-stu-id="6bba3-112">The sample filters can be used to help limit the Netmon output to traffic of interest.</span></span> <span data-ttu-id="6bba3-113">Para obter mais informações sobre como usar filtros do Netmon, consulte [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="6bba3-113">For more information about using Netmon filters, see [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

<span data-ttu-id="6bba3-114">O exemplo a seguir mostra um filtro que limita a saída a todos os WS-Discovery tráfego de difusão.</span><span class="sxs-lookup"><span data-stu-id="6bba3-114">The following example shows a filter that limits output to all broadcast WS-Discovery traffic.</span></span>

> [!Note]  
> <span data-ttu-id="6bba3-115">Esse filtro não captura o tráfego de pilhas que não respondem a mensagens WS-Discovery multicast que se originam na porta 3702.</span><span class="sxs-lookup"><span data-stu-id="6bba3-115">This filter does not capture traffic from stacks that do not respond to multicast WS-Discovery messages that originate at port 3702.</span></span> <span data-ttu-id="6bba3-116">Se tal pilha estiver sendo usada, esse filtro de exemplo deverá ser modificado antes do uso.</span><span class="sxs-lookup"><span data-stu-id="6bba3-116">If such a stack is being used, then this sample filter must be modified before use.</span></span>

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

<span data-ttu-id="6bba3-117">O exemplo a seguir mostra um filtro que limita a saída para mensagens HTTP enviadas a pilhas WSDAPI na porta padrão.</span><span class="sxs-lookup"><span data-stu-id="6bba3-117">The following example shows a filter that limits output to HTTP messages sent to WSDAPI stacks on the default port.</span></span>

> [!Note]  
> <span data-ttu-id="6bba3-118">Os serviços podem enviar mensagens HTTP relevantes de portas diferentes de 5357.</span><span class="sxs-lookup"><span data-stu-id="6bba3-118">Services may send relevant HTTP messages from ports other than 5357.</span></span> <span data-ttu-id="6bba3-119">Se o tráfego de outras portas for interessante, esse filtro de exemplo deverá ser modificado antes do uso.</span><span class="sxs-lookup"><span data-stu-id="6bba3-119">If traffic from other ports is of interest, then this sample filter must be modified before use.</span></span>

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

<span data-ttu-id="6bba3-120">O exemplo a seguir mostra um filtro que limita a saída ao tráfego de multicast IPv4.</span><span class="sxs-lookup"><span data-stu-id="6bba3-120">The following example shows a filter that limits output to IPv4 multicast traffic.</span></span>

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

<span data-ttu-id="6bba3-121">O exemplo a seguir mostra um filtro que limita a saída para o tráfego de multicast IPv6.</span><span class="sxs-lookup"><span data-stu-id="6bba3-121">The following example shows a filter that limits output to IPv6 multicast traffic.</span></span>

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

<span data-ttu-id="6bba3-122">Alguns filtros podem ser combinados para limitar os resultados.</span><span class="sxs-lookup"><span data-stu-id="6bba3-122">Some filters can be combined to further limit results.</span></span> <span data-ttu-id="6bba3-123">O exemplo a seguir mostra um filtro que limita a saída para o tráfego de WS-Discovery multicast IPv4.</span><span class="sxs-lookup"><span data-stu-id="6bba3-123">The following example shows a filter that limits output to IPv4 multicast WS-Discovery traffic.</span></span>

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

<span data-ttu-id="6bba3-124">Quando esses filtros são usados, o tráfego relevante pode ser excluído dos resultados do Netmon.</span><span class="sxs-lookup"><span data-stu-id="6bba3-124">When these filters are used, relevant traffic may be excluded from the Netmon results.</span></span> <span data-ttu-id="6bba3-125">A exclusão pode ocorrer quando os serviços residem em portas diferentes das portas padrão (5357/5358) e quando uma pilha DPWS não responde às mensagens que usam a porta padrão.</span><span class="sxs-lookup"><span data-stu-id="6bba3-125">Exclusion can occur when services reside at ports other than the default ports (5357/5358) and when a DPWS stack does not respond to messages using the default port.</span></span> <span data-ttu-id="6bba3-126">Nesses casos, os filtros devem ser modificados antes do uso.</span><span class="sxs-lookup"><span data-stu-id="6bba3-126">In these cases, the filters must be modified before use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bba3-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6bba3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bba3-128">Procedimentos de diagnóstico do WSDAPI</span><span class="sxs-lookup"><span data-stu-id="6bba3-128">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="6bba3-129">Introdução com a solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="6bba3-129">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



