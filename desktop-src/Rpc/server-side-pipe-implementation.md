---
title: Implementação de pipe de Server-Side
description: Os programas de servidor para aplicativos distribuídos que usam pipes não precisam implementar nenhuma função Push, pull ou Alloc.
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6927350e10061850c5fac0ab0db7c18570dd2bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005776"
---
# <a name="server-side-pipe-implementation"></a><span data-ttu-id="8c5f2-103">Implementação de pipe de Server-Side</span><span class="sxs-lookup"><span data-stu-id="8c5f2-103">Server-Side Pipe Implementation</span></span>

<span data-ttu-id="8c5f2-104">Os programas de servidor para aplicativos distribuídos que usam pipes não precisam implementar nenhuma função Push, pull ou Alloc.</span><span class="sxs-lookup"><span data-stu-id="8c5f2-104">Server programs for distributed applications that use pipes need not implement any push, pull, or alloc functions.</span></span> <span data-ttu-id="8c5f2-105">Eles precisam conter procedimentos que os clientes podem invocar remotamente para iniciar transferências de dados.</span><span class="sxs-lookup"><span data-stu-id="8c5f2-105">They do need to contain procedures that clients can invoke remotely to initiate data transfers.</span></span> <span data-ttu-id="8c5f2-106">Nos tópicos a seguir, esta seção explica como os procedimentos remotos do servidor podem ser implementados.</span><span class="sxs-lookup"><span data-stu-id="8c5f2-106">In the following topics, this section explains how the server's remote procedures can be implemented.</span></span>

-   [<span data-ttu-id="8c5f2-107">Implementando pipes de entrada no servidor</span><span class="sxs-lookup"><span data-stu-id="8c5f2-107">Implementing Input Pipes on the Server</span></span>](implementing-input-pipes-on-the-server.md)
-   [<span data-ttu-id="8c5f2-108">Implementando os pipes de saída no servidor</span><span class="sxs-lookup"><span data-stu-id="8c5f2-108">Implementing Output Pipes on the Server</span></span>](implementing-output-pipes-on-the-server.md)

 

 




