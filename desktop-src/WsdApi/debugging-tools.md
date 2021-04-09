---
description: Um conjunto de ferramentas de depuração criado em serviços da Web na API de dispositivos (WSDAPI) está disponível no SDK do Windows e no WDK (Kit de driver do Windows).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Ferramentas de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091708"
---
# <a name="debugging-tools"></a><span data-ttu-id="181e7-103">Ferramentas de depuração</span><span class="sxs-lookup"><span data-stu-id="181e7-103">Debugging Tools</span></span>

<span data-ttu-id="181e7-104">Um conjunto de ferramentas de depuração criado em serviços da Web na API de dispositivos (WSDAPI) está disponível no SDK do Windows e no WDK (Kit de driver do Windows).</span><span class="sxs-lookup"><span data-stu-id="181e7-104">A debugging toolset built on Web Services on Devices API (WSDAPI) is available in the Windows SDK and the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="181e7-105">Essas ferramentas podem ser usadas para testar a funcionalidade de aplicativos personalizados escritos em WSDAPI, ou dispositivos e clientes gravados usando outro perfil de dispositivo para as pilhas de serviços Web (DPWS).</span><span class="sxs-lookup"><span data-stu-id="181e7-105">These tools can be used to test the functionality of custom applications written on WSDAPI, or devices and clients written using other Device Profile for Web Services (DPWS) stacks.</span></span>

<span data-ttu-id="181e7-106">As ferramentas de host de depuração WSD (wsddebug \_host.exe) e de cliente de depuração WSD (wsddebug \_client.exe) podem ser usadas para inspecionar as características de clientes DPWS ou hosts.</span><span class="sxs-lookup"><span data-stu-id="181e7-106">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools can be used to inspect the characteristics of DPWS clients or hosts.</span></span> <span data-ttu-id="181e7-107">Eles também podem ser usados para solucionar problemas de conectividade ou configuração.</span><span class="sxs-lookup"><span data-stu-id="181e7-107">They can also be used to troubleshoot connectivity or configuration problems.</span></span> <span data-ttu-id="181e7-108">Para obter mais informações, consulte [Guia de solução de problemas de WSDAPI](wsdapi-troubleshooting-guide.md).</span><span class="sxs-lookup"><span data-stu-id="181e7-108">For more information, see [WSDAPI Troubleshooting Guide](wsdapi-troubleshooting-guide.md).</span></span> <span data-ttu-id="181e7-109">Essas ferramentas estão disponíveis apenas no SDK.</span><span class="sxs-lookup"><span data-stu-id="181e7-109">These tools are only available in the SDK.</span></span> <span data-ttu-id="181e7-110">As ferramentas do SDK estão localizadas no seguinte diretório: <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="181e7-110">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="181e7-111">A [ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) pode ser usada para testar a interoperabilidade no nível do protocolo SOAP ou no nível de transporte (ou seja, garantir que as mensagens estejam bem formadas).</span><span class="sxs-lookup"><span data-stu-id="181e7-111">The [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) can be used to test SOAP-level or transport-level interoperability (that is, ensuring messages are well-formed).</span></span> <span data-ttu-id="181e7-112">Essa ferramenta só está disponível no WDK.</span><span class="sxs-lookup"><span data-stu-id="181e7-112">This tool is only available in the WDK.</span></span>

## <a name="the-wsd-debug-client"></a><span data-ttu-id="181e7-113">O cliente de depuração WSD</span><span class="sxs-lookup"><span data-stu-id="181e7-113">The WSD Debug Client</span></span>

<span data-ttu-id="181e7-114">O cliente de depuração WSD (wsddebug \_client.exe) fornece um console interativo que pode ser usado para enviar e receber mensagens de WS-Discovery e para obter metadados.</span><span class="sxs-lookup"><span data-stu-id="181e7-114">The WSD Debug Client (wsddebug\_client.exe) provides an interactive console that can be used to send and receive WS-Discovery messages, and to obtain metadata.</span></span> <span data-ttu-id="181e7-115">Ele também pode ser usado para gerar e consumir mensagens brutas de multicast.</span><span class="sxs-lookup"><span data-stu-id="181e7-115">It can also be used to generate and consume raw multicast messages.</span></span>

<span data-ttu-id="181e7-116">O cliente de depuração WSD opera em um dos três modos: multicast, descoberta e metadados.</span><span class="sxs-lookup"><span data-stu-id="181e7-116">The WSD Debug Client operates in one of three modes: multicast, discovery, and metadata.</span></span>



| <span data-ttu-id="181e7-117">Mode</span><span class="sxs-lookup"><span data-stu-id="181e7-117">Mode</span></span>      | <span data-ttu-id="181e7-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="181e7-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="181e7-119">Multicast</span><span class="sxs-lookup"><span data-stu-id="181e7-119">Multicast</span></span> | <span data-ttu-id="181e7-120">No modo multicast, o cliente de depuração WSD envia e recebe mensagens multicast não formatadas na porta UDP 3702, conforme definido em WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="181e7-120">In Multicast mode, the WSD Debug Client sends and receives unformatted multicast messages on UDP port 3702, as defined in WS-Discovery.</span></span> <span data-ttu-id="181e7-121">O usuário pode salvar essas mensagens SOAP em um arquivo de texto e pode modificar e retransmitir as mensagens com o cliente de depuração WSD.</span><span class="sxs-lookup"><span data-stu-id="181e7-121">The user may save these SOAP messages in a text file, and may modify and rebroadcast the messages with the WSD Debug Client.</span></span>                                                                                                                                 |
| <span data-ttu-id="181e7-122">Descoberta</span><span class="sxs-lookup"><span data-stu-id="181e7-122">Discovery</span></span> | <span data-ttu-id="181e7-123">No modo de descoberta, o cliente de depuração WSD envia e recebe mensagens de WS-Discovery formatadas.</span><span class="sxs-lookup"><span data-stu-id="181e7-123">In Discovery mode, the WSD Debug Client sends and receives formatted WS-Discovery messages.</span></span> <span data-ttu-id="181e7-124">Ele pode exibir [mensagens de](bye-message.md) [saudação](hello-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md) recebidas.</span><span class="sxs-lookup"><span data-stu-id="181e7-124">It can display received [Hello](hello-message.md), [Bye](bye-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md) messages.</span></span> <span data-ttu-id="181e7-125">Ele pode enviar mensagens de [investigação](probe-message.md) por UDP ou http e [resolver](resolve-message.md) mensagens por UDP.</span><span class="sxs-lookup"><span data-stu-id="181e7-125">It can send [Probe](probe-message.md) messages over UDP or HTTP, and [Resolve](resolve-message.md) messages over UDP.</span></span> |
| <span data-ttu-id="181e7-126">Metadados</span><span class="sxs-lookup"><span data-stu-id="181e7-126">Metadata</span></span>  | <span data-ttu-id="181e7-127">Além de implementar todos os recursos do modo de descoberta, o modo de metadados também tenta recuperar metadados de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="181e7-127">In addition to implementing all of the features of Discovery mode, Metadata mode also attempts to retrieve metadata from devices.</span></span>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="181e7-128">Para obter mais informações, consulte [usando um host genérico e um cliente para troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md), [usando um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md)e [usando o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="181e7-128">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md), [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md), and [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

## <a name="the-wsd-debug-host"></a><span data-ttu-id="181e7-129">O host de depuração WSD</span><span class="sxs-lookup"><span data-stu-id="181e7-129">The WSD Debug Host</span></span>

<span data-ttu-id="181e7-130">O host de depuração WSD (wsddebug \_host.exe) fornece um console interativo usado para anunciar o host, responder a solicitações de cliente e imprimir informações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="181e7-130">The WSD Debug Host (wsddebug\_host.exe) provides an interactive console used to announce the host, respond to client requests, and print diagnostic information.</span></span>

<span data-ttu-id="181e7-131">O host de depuração WSD opera em um dos dois modos: descoberta e metadados.</span><span class="sxs-lookup"><span data-stu-id="181e7-131">The WSD Debug Host operates in one of two modes: discovery and metadata.</span></span>



| <span data-ttu-id="181e7-132">Mode</span><span class="sxs-lookup"><span data-stu-id="181e7-132">Mode</span></span>      | <span data-ttu-id="181e7-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="181e7-133">Description</span></span>                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="181e7-134">Descoberta</span><span class="sxs-lookup"><span data-stu-id="181e7-134">Discovery</span></span> | <span data-ttu-id="181e7-135">No modo de descoberta, o host de depuração WSD imprime as mensagens WS-Discovery formatadas.</span><span class="sxs-lookup"><span data-stu-id="181e7-135">In Discovery mode, the WSD Debug Host prints formatted WS-Discovery messages.</span></span> <span data-ttu-id="181e7-136">Ele também envia mensagens de [saudação](hello-message.md) e de [adeus](bye-message.md) e responde automaticamente a [investigações](probe-message.md) e a [resolver](resolve-message.md) mensagens.</span><span class="sxs-lookup"><span data-stu-id="181e7-136">It also sends [Hello](hello-message.md) and [Bye](bye-message.md) messages, and automatically responds to [Probe](probe-message.md) and [Resolve](resolve-message.md) messages.</span></span> |
| <span data-ttu-id="181e7-137">Metadados</span><span class="sxs-lookup"><span data-stu-id="181e7-137">Metadata</span></span>  | <span data-ttu-id="181e7-138">Além de implementar todos os recursos do modo de descoberta, o modo de metadados anuncia um serviço de metadados e permite que os clientes se conectem e executem a troca de metadados.</span><span class="sxs-lookup"><span data-stu-id="181e7-138">In addition to implementing all of the features of Discovery mode, Metadata mode advertises a metadata service and allows clients to connect and perform metadata exchange.</span></span>                                                                                       |



 

<span data-ttu-id="181e7-139">Para obter mais informações, consulte [usando um host genérico e um cliente para troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md) e [usando um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="181e7-139">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) and [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="181e7-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="181e7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="181e7-141">Desenvolvimento de aplicativos WSD no Windows</span><span class="sxs-lookup"><span data-stu-id="181e7-141">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="181e7-142">Ferramentas de desenvolvimento do WSDAPI</span><span class="sxs-lookup"><span data-stu-id="181e7-142">WSDAPI Development Tools</span></span>](wsdapi-development-tools.md)
</dt> <dt>

[<span data-ttu-id="181e7-143">Guia de solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="181e7-143">WSDAPI Troubleshooting Guide</span></span>](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



