---
title: Conectando o cliente e o servidor
description: Para se comunicar, os programas de cliente e servidor devem estabelecer uma sessão de comunicação na rede ou nas redes que os conectam.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- Chamada de procedimento remoto RPC, tarefas, cliente de conexão e servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a22ea7a9a6dd30f2b9495b6d2ee868aac217f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453633"
---
# <a name="connecting-the-client-and-the-server"></a><span data-ttu-id="e1527-104">Conectando o cliente e o servidor</span><span class="sxs-lookup"><span data-stu-id="e1527-104">Connecting the Client and the Server</span></span>

<span data-ttu-id="e1527-105">Para se comunicar, os programas de cliente e servidor devem estabelecer uma sessão de comunicação na rede ou nas redes que os conectam.</span><span class="sxs-lookup"><span data-stu-id="e1527-105">To communicate, client and server programs must establish a communication session across the network or networks that connect them.</span></span> <span data-ttu-id="e1527-106">Depois que eles estabelecem a conexão, o cliente pode chamar procedimentos remotos no programa do servidor como se eles fossem locais para o programa cliente.</span><span class="sxs-lookup"><span data-stu-id="e1527-106">Once they establish the connection, the client can call remote procedures in the server program as if they were local to the client program.</span></span>

<span data-ttu-id="e1527-107">Esta seção fornece uma visão geral conceitual de como estabelecer uma conexão entre clientes e servidores para chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="e1527-107">This section provides a conceptual overview of how to establish a connection between clients and servers for remote procedure calls.</span></span> <span data-ttu-id="e1527-108">Ele não fornece uma discussão aprofundada sobre este tópico.</span><span class="sxs-lookup"><span data-stu-id="e1527-108">It does not provide an in-depth discussion of this topic.</span></span> <span data-ttu-id="e1527-109">Todos os conceitos nesta seção são apresentados em detalhes em capítulos posteriores e na seção de referência da função RPC.</span><span class="sxs-lookup"><span data-stu-id="e1527-109">All of the concepts in this section are presented in detail in later chapters and in the RPC Function Reference section.</span></span>

<span data-ttu-id="e1527-110">A discussão apresentada nesta seção está dividida nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="e1527-110">The discussion presented in this section is divided into the following topics:</span></span>

-   [<span data-ttu-id="e1527-111">Terminologia de ligação de RPC essencial</span><span class="sxs-lookup"><span data-stu-id="e1527-111">Essential RPC Binding Terminology</span></span>](essential-rpc-binding-terminology.md)
-   [<span data-ttu-id="e1527-112">Como o servidor se prepara para uma conexão</span><span class="sxs-lookup"><span data-stu-id="e1527-112">How the Server Prepares for a Connection</span></span>](how-the-server-prepares-for-a-connection.md)
-   [<span data-ttu-id="e1527-113">Como o cliente estabelece uma conexão</span><span class="sxs-lookup"><span data-stu-id="e1527-113">How the Client Establishes a Connection</span></span>](how-the-client-establishes-a-connection.md)

<span data-ttu-id="e1527-114">Observe que a discussão pressupõe identificadores de ligação explícitos.</span><span class="sxs-lookup"><span data-stu-id="e1527-114">Note that the discussion assumes explicit binding handles.</span></span> <span data-ttu-id="e1527-115">No entanto, se seu aplicativo usar outros tipos de identificadores de associação, talvez seja necessário modificar as etapas apresentadas nesta seção.</span><span class="sxs-lookup"><span data-stu-id="e1527-115">However, if your application uses other types of binding handles, you may have to modify the steps presented in this section.</span></span> <span data-ttu-id="e1527-116">Para obter mais informações, consulte [Binding e Handles](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="e1527-116">For more information, see [Binding and Handles](binding-and-handles.md).</span></span>

 

 




