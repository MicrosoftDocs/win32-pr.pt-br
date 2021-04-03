---
title: Modelos de Memory-Management
description: Modelos de Memory-Management
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916655"
---
# <a name="memory-management-models"></a><span data-ttu-id="3c7b9-103">Modelos de Memory-Management</span><span class="sxs-lookup"><span data-stu-id="3c7b9-103">Memory-Management Models</span></span>

<span data-ttu-id="3c7b9-104">Como desenvolvedor, você tem várias opções de como a memória é alocada e liberada.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-104">As a developer, you have several choices for how memory is allocated and freed.</span></span> <span data-ttu-id="3c7b9-105">Considere uma estrutura de dados complexa que consiste em nós conectados com ponteiros, como uma lista vinculada ou uma árvore.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-105">Consider a complex data structure that consists of nodes connected with pointers, such as a linked list or a tree.</span></span> <span data-ttu-id="3c7b9-106">Você pode aplicar atributos que selecionem um dos seguintes modelos:</span><span class="sxs-lookup"><span data-stu-id="3c7b9-106">You can apply attributes that select one of the following models:</span></span>

-   <span data-ttu-id="3c7b9-107">[Alocação e desalocação de nó por nó](node-by-node-allocation-and-deallocation.md).</span><span class="sxs-lookup"><span data-stu-id="3c7b9-107">[Node-by-node allocation and deallocation](node-by-node-allocation-and-deallocation.md).</span></span>
-   <span data-ttu-id="3c7b9-108">[Um único buffer linear alocado pelo stub para toda a árvore](stub-allocated-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="3c7b9-108">[A single linear buffer allocated by the stub for the entire tree](stub-allocated-buffers.md).</span></span>
-   [<span data-ttu-id="3c7b9-109">Gerenciamento de memória de stub de servidor</span><span class="sxs-lookup"><span data-stu-id="3c7b9-109">Server stub memory management</span></span>](server-stub-memory-management.md)
-   <span data-ttu-id="3c7b9-110">[Um único buffer linear alocado pelo aplicativo cliente para toda a árvore](application-allocated-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="3c7b9-110">[A single linear buffer allocated by the client application for the entire tree](application-allocated-buffer.md).</span></span>
-   <span data-ttu-id="3c7b9-111">[Armazenamento persistente no servidor](persistent-storage-on-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="3c7b9-111">[Persistent storage on the server](persistent-storage-on-the-server.md).</span></span>

 

 




