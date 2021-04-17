---
description: A API de grafo de pares permite que os aplicativos transmitam dados entre os colegas de forma eficiente e confiável. Os principais conceitos da tecnologia de grafo de pares são os nós de um grafo de mesmo nível e avisos de eventos.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Sobre a API de gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b08e320f1c8d176d0bd34cc7a9a9422c6cfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754518"
---
# <a name="about-the-graphing-api"></a><span data-ttu-id="1b76f-104">Sobre a API de gráfico</span><span class="sxs-lookup"><span data-stu-id="1b76f-104">About the Graphing API</span></span>

<span data-ttu-id="1b76f-105">A API de grafo de pares permite que os aplicativos transmitam dados entre os colegas de forma eficiente e confiável.</span><span class="sxs-lookup"><span data-stu-id="1b76f-105">The Peer Graphing API allows applications to pass data between peers efficiently and reliably.</span></span> <span data-ttu-id="1b76f-106">Os principais conceitos da tecnologia de grafo de pares são os **nós** de um grafo de mesmo nível e avisos de eventos.</span><span class="sxs-lookup"><span data-stu-id="1b76f-106">The core concepts of peer graph technology are the **nodes** of a peer graph, and event notices.</span></span>

## <a name="nodes"></a><span data-ttu-id="1b76f-107">Nós</span><span class="sxs-lookup"><span data-stu-id="1b76f-107">Nodes</span></span>

<span data-ttu-id="1b76f-108">Um nó representa uma instância específica de um par em uma rede.</span><span class="sxs-lookup"><span data-stu-id="1b76f-108">A node represents a specific instance of a peer on a network.</span></span> <span data-ttu-id="1b76f-109">A infraestrutura de API de grafo de pares garante que cada nó tenha uma exibição consistente dos dados em um grafo.</span><span class="sxs-lookup"><span data-stu-id="1b76f-109">The Peer Graphing API infrastructure ensures that each node has a consistent view of the data in a graph.</span></span> <span data-ttu-id="1b76f-110">Um nó tem os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="1b76f-110">A node has the following features:</span></span>

-   <span data-ttu-id="1b76f-111">Pode se conectar a um nó diferente e formar uma rede interrelacionada chamada de grafo par.</span><span class="sxs-lookup"><span data-stu-id="1b76f-111">Can connect to a different node, and form an interrelated network called a peer graph.</span></span>
-   <span data-ttu-id="1b76f-112">Pode compartilhar dados com outros nós em um grafo na forma de um [registro](records.md).</span><span class="sxs-lookup"><span data-stu-id="1b76f-112">Can share data with other nodes in a graph in the form of a [record](records.md).</span></span>
-   <span data-ttu-id="1b76f-113">Pode criar conexões diretas separadas dos gráficos pares estabelecidos usando a [API de agrupamento](about-the-grouping-api.md)de pares.</span><span class="sxs-lookup"><span data-stu-id="1b76f-113">Can create direct connections separate from the peer graphs established by using the Peer [Grouping API](about-the-grouping-api.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="1b76f-114">Conexões diretas permitem que os nós enviem dados privados entre si.</span><span class="sxs-lookup"><span data-stu-id="1b76f-114">Direct connections allow nodes to send private data to each other.</span></span>

     

## <a name="event-notices"></a><span data-ttu-id="1b76f-115">Avisos de eventos</span><span class="sxs-lookup"><span data-stu-id="1b76f-115">Event Notices</span></span>

<span data-ttu-id="1b76f-116">A API de grafo de pares tem uma infraestrutura de eventos que permite que um aplicativo se registre e receba um aviso de um evento de mesmo nível dentro da infraestrutura da API de grafo de pares.</span><span class="sxs-lookup"><span data-stu-id="1b76f-116">The Peer Graphing API has an event infrastructure that allows an application to register and receive notice of a peer event within the Peer Graphing API infrastructure.</span></span> <span data-ttu-id="1b76f-117">Quando algo é alterado em um grafo de mesmo nível, um aplicativo envia um aviso de evento para identificar que ocorreu uma alteração.</span><span class="sxs-lookup"><span data-stu-id="1b76f-117">When something changes within a peer graph, an application sends an event notice to identify that a change has occurred.</span></span>

 

 



