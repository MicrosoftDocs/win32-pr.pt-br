---
description: O perfil de dispositivo para hosts de serviços Web (DPWS) e clientes se comunicam pela rede usando uma série de mensagens SOAP por UDP e HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Padrões de mensagem de troca de metadados e descoberta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104172440"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a><span data-ttu-id="1f700-103">Padrões de mensagem de troca de metadados e descoberta</span><span class="sxs-lookup"><span data-stu-id="1f700-103">Discovery and Metadata Exchange Message Patterns</span></span>

<span data-ttu-id="1f700-104">O perfil de dispositivo para hosts de serviços Web (DPWS) e clientes se comunicam pela rede usando uma série de mensagens SOAP por UDP e HTTP.</span><span class="sxs-lookup"><span data-stu-id="1f700-104">Device Profile for Web Services (DPWS) hosts and clients communicate over the network using a series of SOAP messages over UDP and HTTP.</span></span>

<span data-ttu-id="1f700-105">O diagrama a seguir mostra uma visão geral do tráfego esperado de UDP e HTTP entre um host DPWS e um cliente.</span><span class="sxs-lookup"><span data-stu-id="1f700-105">The following diagram shows an overview of the expected UDP and HTTP traffic between a DPWS host and client.</span></span>

![Diagrama mostrando o tráfego UDP e HTTP entre um host DPWS e um cliente.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

<span data-ttu-id="1f700-107">As mensagens [Hello](hello-message.md), [adeus](bye-message.md), [Probe](probe-message.md), [resolve](resolve-message.md)e [Get](get--metadata-exchange--http-request-and-message.md) são todas geradas sem solicitação de rede; essas mensagens são usadas para anunciar o estado do dispositivo ou para emitir uma solicitação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="1f700-107">[Hello](hello-message.md), [Bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md), and [Get](get--metadata-exchange--http-request-and-message.md) messages are all generated without network solicitation; these messages are used to announce device state or to issue a search request.</span></span> <span data-ttu-id="1f700-108">As mensagens [ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md)e [GetResponse](getresponse--metadata-exchange--message.md) são geradas em resposta à investigação, resolução e obtenção de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1f700-108">[ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md), and [GetResponse](getresponse--metadata-exchange--message.md) messages are generated in response to Probe, Resolve and Get messages.</span></span>

<span data-ttu-id="1f700-109">As mensagens [Hello](hello-message.md), [adeus](bye-message.md), [resolve](resolve-message.md)e [ResolveMatches](resolvematches-message.md) sempre ocorrerão sobre o UDP.</span><span class="sxs-lookup"><span data-stu-id="1f700-109">[Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md), and [ResolveMatches](resolvematches-message.md) messages will always occur over UDP.</span></span> <span data-ttu-id="1f700-110">Da mesma forma, as mensagens de metadados [Get](get--metadata-exchange--http-request-and-message.md) e [GetResponse](getresponse--metadata-exchange--message.md) sempre ocorrerão via http ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1f700-110">Similarly, [Get](get--metadata-exchange--http-request-and-message.md) and [GetResponse](getresponse--metadata-exchange--message.md) metadata messages will always occur over HTTP or HTTPS.</span></span> <span data-ttu-id="1f700-111">As mensagens de [investigação](probe-message.md) e de [ProbeMatches](probematches-message.md) são normalmente transmitidas por UDP, mas ocorrem em uma conexão http ou HTTPS em um cenário de descoberta direcionada.</span><span class="sxs-lookup"><span data-stu-id="1f700-111">[Probe](probe-message.md) and [ProbeMatches](probematches-message.md) messages are normally transmitted over UDP, but take place over an HTTP or HTTPS connection in a directed discovery scenario.</span></span> <span data-ttu-id="1f700-112">Para obter mais informações sobre padrões de mensagem de descoberta direcionada, consulte [Solucionando problemas de aplicativos usando a descoberta direcionada](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="1f700-112">For more information about directed discovery message patterns, see [Troubleshooting Applications Using Directed Discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="1f700-113">A lista a seguir mostra a sequência típica de mensagens na conexão.</span><span class="sxs-lookup"><span data-stu-id="1f700-113">The following list shows the typical sequence of messages on the wire.</span></span> <span data-ttu-id="1f700-114">Nem todas as mensagens são obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="1f700-114">Not all messages are mandatory.</span></span>

1.  [<span data-ttu-id="1f700-115">Olá</span><span class="sxs-lookup"><span data-stu-id="1f700-115">Hello</span></span>](hello-message.md)
2.  [<span data-ttu-id="1f700-116">Investigação</span><span class="sxs-lookup"><span data-stu-id="1f700-116">Probe</span></span>](probe-message.md)
3.  [<span data-ttu-id="1f700-117">ProbeMatches</span><span class="sxs-lookup"><span data-stu-id="1f700-117">ProbeMatches</span></span>](probematches-message.md)
4.  [<span data-ttu-id="1f700-118">Resolver</span><span class="sxs-lookup"><span data-stu-id="1f700-118">Resolve</span></span>](resolve-message.md)
5.  [<span data-ttu-id="1f700-119">ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="1f700-119">ResolveMatches</span></span>](resolvematches-message.md)
6.  <span data-ttu-id="1f700-120">[Get](get--metadata-exchange--http-request-and-message.md) (solicitação de troca de metadados)</span><span class="sxs-lookup"><span data-stu-id="1f700-120">[Get](get--metadata-exchange--http-request-and-message.md) (metadata exchange request)</span></span>
7.  [<span data-ttu-id="1f700-121">GetResponse</span><span class="sxs-lookup"><span data-stu-id="1f700-121">GetResponse</span></span>](getresponse--metadata-exchange--message.md)
8.  [<span data-ttu-id="1f700-122">Logo</span><span class="sxs-lookup"><span data-stu-id="1f700-122">Bye</span></span>](bye-message.md)

## <a name="related-topics"></a><span data-ttu-id="1f700-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f700-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f700-124">Sobre os serviços Web em dispositivos</span><span class="sxs-lookup"><span data-stu-id="1f700-124">About Web Services on Devices</span></span>](about-web-services-for-devices.md)
</dt> </dl>

 

 



