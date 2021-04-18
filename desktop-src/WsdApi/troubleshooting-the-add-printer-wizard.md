---
description: Lista os procedimentos de diagnóstico a serem usados ao solucionar problemas do assistente para adicionar impressora.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Solução de problemas do assistente para adicionar impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760508"
---
# <a name="troubleshooting-the-add-printer-wizard"></a><span data-ttu-id="b9f94-103">Solução de problemas do assistente para adicionar impressora</span><span class="sxs-lookup"><span data-stu-id="b9f94-103">Troubleshooting the Add Printer Wizard</span></span>

<span data-ttu-id="b9f94-104">O assistente para adicionar impressora:</span><span class="sxs-lookup"><span data-stu-id="b9f94-104">The Add Printer Wizard:</span></span>

-   <span data-ttu-id="b9f94-105">Sempre usa WS-Discovery UDP para descoberta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b9f94-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="b9f94-106">Sempre inicia uma conexão HTTP ou HTTPS para a troca de metadados</span><span class="sxs-lookup"><span data-stu-id="b9f94-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="b9f94-107">Às vezes usa a descoberta direcionada</span><span class="sxs-lookup"><span data-stu-id="b9f94-107">Sometimes uses directed discovery</span></span>
-   <span data-ttu-id="b9f94-108">Às vezes usa um canal seguro (HTTPS) para troca de metadados</span><span class="sxs-lookup"><span data-stu-id="b9f94-108">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="b9f94-109">Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com o assistente para adicionar impressora.</span><span class="sxs-lookup"><span data-stu-id="b9f94-109">The following diagnostic procedures should be used (in order) to help identify problems with the Add Printer Wizard.</span></span>

<span data-ttu-id="b9f94-110">**Para solucionar problemas do assistente para adicionar impressora**</span><span class="sxs-lookup"><span data-stu-id="b9f94-110">**To troubleshoot the Add Printer Wizard**</span></span>

1.  <span data-ttu-id="b9f94-111">Se a descoberta direcionada for usada, [solucione o problema de descoberta direcionada](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="b9f94-111">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="b9f94-112">[Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="b9f94-112">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="b9f94-113">[Use um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="b9f94-113">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="b9f94-114">[Use o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="b9f94-114">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="b9f94-115">[Inspecione os rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="b9f94-115">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="b9f94-116">[Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="b9f94-116">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="b9f94-117">[Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="b9f94-117">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="b9f94-118">[Inspecione os rastreamentos de rede para a troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="b9f94-118">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="b9f94-119">Se a origem do problema não puder ser identificada usando os procedimentos de diagnóstico acima, siga as instruções em [habilitando o rastreamento de WSDAPI](enabling-wsdapi-tracing.md) e entre em contato com o suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b9f94-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9f94-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9f94-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9f94-121">Introdução com a solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="b9f94-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="b9f94-122">Solucionando problemas de aplicativos usando a descoberta direcionada</span><span class="sxs-lookup"><span data-stu-id="b9f94-122">Troubleshooting Applications Using Directed Discovery</span></span>](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



