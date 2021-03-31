---
description: Lista os procedimentos de diagnóstico a serem usados ao solucionar problemas do Gerenciador de rede.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Solucionando problemas do Gerenciador de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920900"
---
# <a name="troubleshooting-the-network-explorer"></a><span data-ttu-id="a1ce7-103">Solucionando problemas do Gerenciador de rede</span><span class="sxs-lookup"><span data-stu-id="a1ce7-103">Troubleshooting the Network Explorer</span></span>

<span data-ttu-id="a1ce7-104">O Gerenciador de rede:</span><span class="sxs-lookup"><span data-stu-id="a1ce7-104">The Network Explorer:</span></span>

-   <span data-ttu-id="a1ce7-105">Sempre usa WS-Discovery UDP para descoberta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a1ce7-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="a1ce7-106">Sempre inicia uma conexão HTTP ou HTTPS para a troca de metadados</span><span class="sxs-lookup"><span data-stu-id="a1ce7-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="a1ce7-107">Às vezes usa um canal seguro (HTTPS) para troca de metadados</span><span class="sxs-lookup"><span data-stu-id="a1ce7-107">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="a1ce7-108">Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com o Gerenciador de rede.</span><span class="sxs-lookup"><span data-stu-id="a1ce7-108">The following diagnostic procedures should be used (in order) to help identify problems with the Network Explorer.</span></span>

<span data-ttu-id="a1ce7-109">**Para solucionar problemas do Gerenciador de rede**</span><span class="sxs-lookup"><span data-stu-id="a1ce7-109">**To troubleshoot the Network Explorer**</span></span>

1.  <span data-ttu-id="a1ce7-110">[Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="a1ce7-110">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="a1ce7-111">[Use um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="a1ce7-111">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
3.  <span data-ttu-id="a1ce7-112">[Use o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="a1ce7-112">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
4.  <span data-ttu-id="a1ce7-113">[Inspecione os rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="a1ce7-113">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
5.  <span data-ttu-id="a1ce7-114">[Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="a1ce7-114">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
6.  <span data-ttu-id="a1ce7-115">[Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="a1ce7-115">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
7.  <span data-ttu-id="a1ce7-116">[Inspecione os rastreamentos de rede para a troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="a1ce7-116">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="a1ce7-117">O Gerenciador de rede usa a [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) para enumerar dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="a1ce7-117">The Network Explorer uses [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) to enumerate network devices.</span></span> <span data-ttu-id="a1ce7-118">Para obter mais informações sobre solução de problemas, consulte [Solucionando problemas de clientes de descoberta de função](troubleshooting-function-discovery-clients.md).</span><span class="sxs-lookup"><span data-stu-id="a1ce7-118">For more troubleshooting information, see [Troubleshooting Function Discovery Clients](troubleshooting-function-discovery-clients.md).</span></span>

<span data-ttu-id="a1ce7-119">Se a origem do problema não puder ser identificada usando os procedimentos de diagnóstico acima, siga as instruções em [habilitando o rastreamento de WSDAPI](enabling-wsdapi-tracing.md) e entre em contato com o suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a1ce7-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1ce7-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1ce7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1ce7-121">Introdução com a solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="a1ce7-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="a1ce7-122">Solucionando problemas de clientes de descoberta de função</span><span class="sxs-lookup"><span data-stu-id="a1ce7-122">Troubleshooting Function Discovery Clients</span></span>](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
