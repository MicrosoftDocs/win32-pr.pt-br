---
title: Canais virtuais dinâmicos
description: As APIs de canal virtual dinâmico (DVC) estendem as APIs de canal virtual existentes para Serviços de Área de Trabalho Remota, conhecidas como APIs de SVC (canal virtual estático).
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363955"
---
# <a name="dynamic-virtual-channels"></a><span data-ttu-id="2b52b-103">Canais virtuais dinâmicos</span><span class="sxs-lookup"><span data-stu-id="2b52b-103">Dynamic Virtual Channels</span></span>

<span data-ttu-id="2b52b-104">As APIs de canal virtual dinâmico (DVC) estendem as APIs de canal virtual existentes para Serviços de Área de Trabalho Remota, conhecidas como APIs de SVC (canal virtual estático).</span><span class="sxs-lookup"><span data-stu-id="2b52b-104">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span> <span data-ttu-id="2b52b-105">As APIs DVC resolvem várias limitações que existiam em APIs SVC entre o cliente e o servidor, como:</span><span class="sxs-lookup"><span data-stu-id="2b52b-105">DVC APIs address several limitations that existed in SVC APIs between the client and server, such as:</span></span>

-   <span data-ttu-id="2b52b-106">Um número limitado de canais</span><span class="sxs-lookup"><span data-stu-id="2b52b-106">A limited number of channels</span></span>
-   <span data-ttu-id="2b52b-107">Reconstrução de pacote</span><span class="sxs-lookup"><span data-stu-id="2b52b-107">Packet reconstruction</span></span>

<span data-ttu-id="2b52b-108">As APIs do DVC ajudarão você a implementar módulos no lado do servidor e do cliente de uma conexão Serviços de Área de Trabalho Remota que se comunicam entre si.</span><span class="sxs-lookup"><span data-stu-id="2b52b-108">DVC APIs will help you to implement modules on the server and client side of a Remote Desktop Services connection that communicate with each other.</span></span>

<span data-ttu-id="2b52b-109">Como muitas outras arquiteturas de cliente/servidor, uma conexão é estabelecida com base em uma parte de dados comumente acordada, conhecida como um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="2b52b-109">Like many other client/server architectures, a connection is established based on a commonly agreed upon piece of data, referred to as an endpoint.</span></span> <span data-ttu-id="2b52b-110">Um exemplo semelhante é o TCP/IP, em que um ponto de extremidade é estabelecido por meio de uma combinação de endereço IP do servidor e o nome da porta.</span><span class="sxs-lookup"><span data-stu-id="2b52b-110">A similar example is TCP/IP, where an endpoint is established through a combination of server IP address and the port name.</span></span> <span data-ttu-id="2b52b-111">Outro exemplo são pipes nomeados, em que um ponto de extremidade é uma combinação do nome do servidor e do nome do pipe.</span><span class="sxs-lookup"><span data-stu-id="2b52b-111">Another example is named pipes, where an endpoint is a combination of the server name and the pipe name.</span></span> <span data-ttu-id="2b52b-112">Em uma conexão Serviços de Área de Trabalho Remota, há apenas dois lados envolvidos.</span><span class="sxs-lookup"><span data-stu-id="2b52b-112">In a Remote Desktop Services connection there are only two sides involved.</span></span> <span data-ttu-id="2b52b-113">Portanto, o ponto de extremidade consiste em uma cadeia de caracteres arbitrária simples que identifica exclusivamente a conexão.</span><span class="sxs-lookup"><span data-stu-id="2b52b-113">Therefore, the endpoint consists of a simple arbitrary string that uniquely identifies the connection.</span></span> <span data-ttu-id="2b52b-114">Assim como TCP/IP e pipes nomeados, várias conexões podem iniciar com o mesmo nome de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="2b52b-114">Much like TCP/IP and named pipes, multiple connections can initiate from the same endpoint name.</span></span> <span data-ttu-id="2b52b-115">Nesse sentido, as conexões não têm nomes; apenas um ouvinte que aguarda solicitações de entrada no ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="2b52b-115">In that sense, connections do not have names; just a listener that waits for incoming requests on the endpoint.</span></span>

<span data-ttu-id="2b52b-116">As APIs DVC consistem no seguinte:</span><span class="sxs-lookup"><span data-stu-id="2b52b-116">The DVC APIs consist of the following:</span></span>

-   <span data-ttu-id="2b52b-117">APIs de cliente</span><span class="sxs-lookup"><span data-stu-id="2b52b-117">Client APIs</span></span>

    <span data-ttu-id="2b52b-118">Essas APIs estão disponíveis no cliente de Conexão de Área de Trabalho Remota (RDC) como um plug-in.</span><span class="sxs-lookup"><span data-stu-id="2b52b-118">These APIs are available in the Remote Desktop Connection (RDC) client as a plug-in.</span></span> <span data-ttu-id="2b52b-119">O lado do cliente está no modo passivo, onde ele escuta conexões de entrada, mas não estabelece ativamente uma conexão.</span><span class="sxs-lookup"><span data-stu-id="2b52b-119">The client side is in passive mode, where it listens for incoming connections but does not actively establish a connection.</span></span>

-   <span data-ttu-id="2b52b-120">APIs de servidor</span><span class="sxs-lookup"><span data-stu-id="2b52b-120">Server APIs</span></span>

    <span data-ttu-id="2b52b-121">Essas APIs iniciam ativamente a conexão.</span><span class="sxs-lookup"><span data-stu-id="2b52b-121">These APIs actively initiate the connection.</span></span>

<span data-ttu-id="2b52b-122">Para obter informações sobre como gravar um módulo de canal virtual dinâmico (DVC), consulte [detalhes de implementação do DVC](dvc-implementation-details.md).</span><span class="sxs-lookup"><span data-stu-id="2b52b-122">For information about how to write a dynamic virtual channel (DVC) module, see [DVC Implementation Details](dvc-implementation-details.md).</span></span>

 

 




