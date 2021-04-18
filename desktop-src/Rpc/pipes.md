---
title: Pipes (RPC)
description: O construtor de tipo de pipe é um mecanismo altamente eficiente para passar grandes quantidades de dados ou qualquer quantidade de dados que não esteja disponível na memória de uma só vez.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- RPC de chamada de procedimento remoto, descrito, Pipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454532"
---
# <a name="pipes-rpc"></a><span data-ttu-id="eb27c-104">Pipes (RPC)</span><span class="sxs-lookup"><span data-stu-id="eb27c-104">Pipes (RPC)</span></span>

<span data-ttu-id="eb27c-105">O construtor de tipo de pipe é um mecanismo altamente eficiente para passar grandes quantidades de dados ou qualquer quantidade de dados que não esteja disponível na memória de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="eb27c-105">The pipe type constructor is a highly efficient mechanism for passing large amounts of data, or any quantity of data that is not all available in memory at one time.</span></span> <span data-ttu-id="eb27c-106">Usando um pipe, o tempo de execução de RPC lida com a transferência de dados real, eliminando a sobrecarga associada às chamadas repetidas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="eb27c-106">By using a pipe, RPC run time handles the actual data transfer, eliminating the overhead associated with repeated remote procedure calls.</span></span>

<span data-ttu-id="eb27c-107">Depois que um cliente chama um procedimento remoto que tem um parâmetro de pipe, o cliente e o servidor inserem loops para transferir dados.</span><span class="sxs-lookup"><span data-stu-id="eb27c-107">After a client invokes a remote procedure that has a pipe parameter, the client and server enter loops to transfer data.</span></span> <span data-ttu-id="eb27c-108">Os dados podem ser produzidos no cliente ou no servidor.</span><span class="sxs-lookup"><span data-stu-id="eb27c-108">The data can be produced on the client or the server.</span></span> <span data-ttu-id="eb27c-109">De qualquer forma, a quantidade de dados (em bytes) não precisa ser conhecida com antecedência.</span><span class="sxs-lookup"><span data-stu-id="eb27c-109">Either way, the amount of data (in bytes) does not have to be known in advance.</span></span> <span data-ttu-id="eb27c-110">Os dados podem ser produzidos ou consumidos incrementalmente.</span><span class="sxs-lookup"><span data-stu-id="eb27c-110">The data can be produced or consumed incrementally.</span></span> <span data-ttu-id="eb27c-111">No loop de transferência de dados, o servidor chama rotinas de stub que carregam ou descarregam um buffer de dados.</span><span class="sxs-lookup"><span data-stu-id="eb27c-111">While in the data-transfer loop, the server calls stub routines that load or unload a buffer of data.</span></span> <span data-ttu-id="eb27c-112">O cliente chama procedimentos definidos pelo programador para alocar buffers, carregar dados e descarregar dados dos buffers.</span><span class="sxs-lookup"><span data-stu-id="eb27c-112">The client calls programmer-defined procedures to allocate buffers, load data into and unload data from the buffers.</span></span>

<span data-ttu-id="eb27c-113">Esta seção fornece uma visão geral do uso de pipes para chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="eb27c-113">This section provides an overview of using pipes for remote procedure calls.</span></span> <span data-ttu-id="eb27c-114">Ele apresenta a visão geral dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="eb27c-114">It presents the overview in the following topics:</span></span>

-   [<span data-ttu-id="eb27c-115">Terminologia de pipe essencial</span><span class="sxs-lookup"><span data-stu-id="eb27c-115">Essential Pipe Terminology</span></span>](essential-pipe-terminology.md)
-   [<span data-ttu-id="eb27c-116">O estado do pipe</span><span class="sxs-lookup"><span data-stu-id="eb27c-116">The Pipe State</span></span>](the-pipe-state.md)
-   [<span data-ttu-id="eb27c-117">Definindo pipes em arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="eb27c-117">Defining Pipes in IDL Files</span></span>](defining-pipes-in-idl-files.md)
-   [<span data-ttu-id="eb27c-118">Implementação de pipe do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="eb27c-118">Client-Side Pipe Implementation</span></span>](client-side-pipe-implementation.md)
-   [<span data-ttu-id="eb27c-119">Implementação de pipe do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="eb27c-119">Server-Side Pipe Implementation</span></span>](server-side-pipe-implementation.md)
-   [<span data-ttu-id="eb27c-120">Regras para vários pipes</span><span class="sxs-lookup"><span data-stu-id="eb27c-120">Rules for Multiple Pipes</span></span>](rules-for-multiple-pipes.md)
-   [<span data-ttu-id="eb27c-121">Combinando parâmetros de pipe e nonpipe</span><span class="sxs-lookup"><span data-stu-id="eb27c-121">Combining Pipe and Nonpipe Parameters</span></span>](combining-pipe-and-nonpipe-parameters.md)

<span data-ttu-id="eb27c-122">Para obter mais informações sobre a sintaxe e as restrições do pipe, consulte [pipe](/windows/desktop/Midl/pipe) na referência da linguagem MIDL.</span><span class="sxs-lookup"><span data-stu-id="eb27c-122">For more information on pipe syntax and restrictions, see [pipe](/windows/desktop/Midl/pipe) in the MIDL Language Reference.</span></span> <span data-ttu-id="eb27c-123">O programa de exemplo de pipes no diretório de RPC dos exemplos do SDK (Software Development Kit) da plataforma \\ demonstra como usar os pipes **\[ out \]** para transferir dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="eb27c-123">The PIPES sample program in the Platform Software Development Kit (SDK) samples\\rpc directory demonstrates how to use **\[in,out\]** pipes to transfer data between a client and a server.</span></span>

 

 
