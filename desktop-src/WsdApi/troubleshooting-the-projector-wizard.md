---
description: Lista os procedimentos de diagnóstico a serem usados ao solucionar problemas do assistente de projetor.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Solução de problemas do assistente do projetor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761217"
---
# <a name="troubleshooting-the-projector-wizard"></a><span data-ttu-id="68ac3-103">Solução de problemas do assistente do projetor</span><span class="sxs-lookup"><span data-stu-id="68ac3-103">Troubleshooting the Projector Wizard</span></span>

<span data-ttu-id="68ac3-104">O assistente do projetor:</span><span class="sxs-lookup"><span data-stu-id="68ac3-104">The Projector Wizard:</span></span>

-   <span data-ttu-id="68ac3-105">Sempre usa WS-Discovery UDP para descoberta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="68ac3-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="68ac3-106">Sempre usa HTTP para troca de metadados</span><span class="sxs-lookup"><span data-stu-id="68ac3-106">Always uses HTTP for metadata exchange</span></span>
-   <span data-ttu-id="68ac3-107">Às vezes usa a descoberta direcionada</span><span class="sxs-lookup"><span data-stu-id="68ac3-107">Sometimes uses directed discovery</span></span>

<span data-ttu-id="68ac3-108">Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com o assistente do projetor.</span><span class="sxs-lookup"><span data-stu-id="68ac3-108">The following diagnostic procedures should be used (in order) to help identify problems with the Projector Wizard.</span></span>

<span data-ttu-id="68ac3-109">**Para solucionar problemas do assistente de projetor**</span><span class="sxs-lookup"><span data-stu-id="68ac3-109">**To troubleshoot the Projector Wizard**</span></span>

1.  <span data-ttu-id="68ac3-110">Se a descoberta direcionada for usada, [solucione o problema de descoberta direcionada](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="68ac3-110">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="68ac3-111">[Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="68ac3-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="68ac3-112">[Use um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="68ac3-112">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="68ac3-113">[Use o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="68ac3-113">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="68ac3-114">[Inspecione os rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="68ac3-114">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="68ac3-115">[Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="68ac3-115">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="68ac3-116">[Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="68ac3-116">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="68ac3-117">[Inspecione os rastreamentos de rede para a troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="68ac3-117">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="68ac3-118">Se a origem do problema não puder ser identificada usando os procedimentos de diagnóstico acima, siga as instruções em [habilitando o rastreamento de WSDAPI](enabling-wsdapi-tracing.md) e entre em contato com o suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="68ac3-118">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68ac3-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68ac3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68ac3-120">Introdução com a solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="68ac3-120">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



