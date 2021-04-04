---
description: Lista os procedimentos de diagnóstico a serem usados ao solucionar problemas de clientes de descoberta de função.
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: Solucionando problemas de clientes de descoberta de função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647691"
---
# <a name="troubleshooting-function-discovery-clients"></a><span data-ttu-id="6f24f-103">Solucionando problemas de clientes de descoberta de função</span><span class="sxs-lookup"><span data-stu-id="6f24f-103">Troubleshooting Function Discovery Clients</span></span>

<span data-ttu-id="6f24f-104">Clientes de descoberta de função:</span><span class="sxs-lookup"><span data-stu-id="6f24f-104">Function Discovery clients:</span></span>

-   <span data-ttu-id="6f24f-105">Sempre usar WS-Discovery UDP para descoberta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="6f24f-105">Always use UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="6f24f-106">Sempre iniciar conexões HTTP ou HTTPS para troca de metadados</span><span class="sxs-lookup"><span data-stu-id="6f24f-106">Always initiate HTTP or HTTPS connections for metadata exchange</span></span>
-   <span data-ttu-id="6f24f-107">Às vezes, use a descoberta direcionada</span><span class="sxs-lookup"><span data-stu-id="6f24f-107">Sometimes use directed discovery</span></span>
-   <span data-ttu-id="6f24f-108">Às vezes, use um canal seguro (HTTPS) para troca de metadados</span><span class="sxs-lookup"><span data-stu-id="6f24f-108">Sometimes use a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="6f24f-109">A lista a seguir mostra a sequência típica de mensagens enviadas e recebidas por clientes de descoberta de função.</span><span class="sxs-lookup"><span data-stu-id="6f24f-109">The following list shows the typical sequence of messages sent and received by Function Discovery clients.</span></span> <span data-ttu-id="6f24f-110">Nem todas as mensagens são obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="6f24f-110">Not all messages are mandatory.</span></span>

1.  <span data-ttu-id="6f24f-111">O cliente envia uma mensagem de [investigação](probe-message.md) para descobrir dispositivos e serviços.</span><span class="sxs-lookup"><span data-stu-id="6f24f-111">The client sends a [Probe](probe-message.md) message to discover devices and services.</span></span> <span data-ttu-id="6f24f-112">Se o cliente estiver usando a descoberta direcionada, essa mensagem será enviada por HTTP ou HTTPS; caso contrário, a mensagem será enviada por multicast UDP para a porta 3702.</span><span class="sxs-lookup"><span data-stu-id="6f24f-112">If the client is using directed discovery then this message is sent over HTTP or HTTPS; otherwise, the message is sent by UDP multicast to port 3702.</span></span>
2.  <span data-ttu-id="6f24f-113">O cliente recebe mensagens [ProbeMatches](probematches-message.md) de dispositivos ou serviços correspondentes.</span><span class="sxs-lookup"><span data-stu-id="6f24f-113">The client receives [ProbeMatches](probematches-message.md) messages from matching devices or services.</span></span> <span data-ttu-id="6f24f-114">As mensagens de descoberta direcionadas são enviadas por HTTP ou HTTPS; caso contrário, essas mensagens são enviadas por UDP unicast e originadas da porta 3702.</span><span class="sxs-lookup"><span data-stu-id="6f24f-114">Directed discovery messages are sent over HTTP or HTTPS; otherwise, these messages are sent by UDP unicast and originate from port 3702.</span></span>
3.  <span data-ttu-id="6f24f-115">Se nenhum XAddrs tiver sido incluído na mensagem ProbeMatches, o cliente enviará uma mensagem de [resolução](resolve-message.md) por multicast UDP para a porta 3702.</span><span class="sxs-lookup"><span data-stu-id="6f24f-115">If no XAddrs were included in the ProbeMatches message, then the client will send a [Resolve](resolve-message.md) message by UDP multicast to port 3702.</span></span>
4.  <span data-ttu-id="6f24f-116">Se uma mensagem de [resolução](resolve-message.md) for enviada, o cliente receberá uma mensagem [ResolveMatches](resolvematches-message.md) de serviços correspondentes.</span><span class="sxs-lookup"><span data-stu-id="6f24f-116">If a [Resolve](resolve-message.md) message was sent, then the client receives a [ResolveMatches](resolvematches-message.md) message from matching services.</span></span> <span data-ttu-id="6f24f-117">Essa mensagem é enviada por UDP unicast da porta 3702 para a porta na qual a mensagem de resolução foi originada.</span><span class="sxs-lookup"><span data-stu-id="6f24f-117">This message is sent by UDP unicast from port 3702 to the port where the Resolve message originated.</span></span>
5.  <span data-ttu-id="6f24f-118">O cliente envia uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) para solicitar metadados do dispositivo ou serviço.</span><span class="sxs-lookup"><span data-stu-id="6f24f-118">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to request metadata from the device or service.</span></span> <span data-ttu-id="6f24f-119">Essa mensagem é enviada por HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6f24f-119">This message is sent by HTTP or HTTPS.</span></span>
6.  <span data-ttu-id="6f24f-120">O cliente recebe uma mensagem [GetResponse](getresponse--metadata-exchange--message.md) com os metadados do dispositivo ou do serviço.</span><span class="sxs-lookup"><span data-stu-id="6f24f-120">The client receives a [GetResponse](getresponse--metadata-exchange--message.md) message with the device or service metadata.</span></span> <span data-ttu-id="6f24f-121">Essa mensagem é enviada por HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6f24f-121">This message is sent by HTTP or HTTPS.</span></span>

<span data-ttu-id="6f24f-122">Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com um cliente de descoberta de função.</span><span class="sxs-lookup"><span data-stu-id="6f24f-122">The following diagnostic procedures should be used (in order) to help identify problems with a Function Discovery client.</span></span>

<span data-ttu-id="6f24f-123">**Para solucionar problemas de um cliente de descoberta de função**</span><span class="sxs-lookup"><span data-stu-id="6f24f-123">**To troubleshoot a Function Discovery client**</span></span>

1.  <span data-ttu-id="6f24f-124">Se a descoberta direcionada for usada, [solucione o problema de descoberta direcionada](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="6f24f-124">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="6f24f-125">[Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="6f24f-125">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="6f24f-126">[Use um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="6f24f-126">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="6f24f-127">[Use o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="6f24f-127">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="6f24f-128">[Inspecione os rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="6f24f-128">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="6f24f-129">[Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="6f24f-129">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="6f24f-130">[Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="6f24f-130">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="6f24f-131">[Inspecione os rastreamentos de rede para a troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="6f24f-131">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="6f24f-132">Se a origem do problema não puder ser identificada usando os procedimentos de diagnóstico acima, siga as instruções em [habilitando o rastreamento de WSDAPI](enabling-wsdapi-tracing.md) e entre em contato com o suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6f24f-132">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f24f-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f24f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f24f-134">Introdução com a solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="6f24f-134">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



