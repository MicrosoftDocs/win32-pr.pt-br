---
title: Implementação de pipe de Client-Side
description: Implementação de pipe do lado do cliente na chamada de procedimento remoto (RPC).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822902"
---
# <a name="client-side-pipe-implementation"></a><span data-ttu-id="b398d-103">Implementação de pipe de Client-Side</span><span class="sxs-lookup"><span data-stu-id="b398d-103">Client-Side Pipe Implementation</span></span>

<span data-ttu-id="b398d-104">O aplicativo cliente deve implementar os seguintes procedimentos, que o stub do cliente chamará durante a transferência de dados:</span><span class="sxs-lookup"><span data-stu-id="b398d-104">The client application must implement the following procedures, which the client stub will call during data transfer:</span></span>

-   <span data-ttu-id="b398d-105">Um procedimento de pull (para um pipe de entrada)</span><span class="sxs-lookup"><span data-stu-id="b398d-105">A pull procedure (for an input pipe)</span></span>
-   <span data-ttu-id="b398d-106">Um procedimento de push (para um pipe de saída)</span><span class="sxs-lookup"><span data-stu-id="b398d-106">A push procedure (for an output pipe)</span></span>
-   <span data-ttu-id="b398d-107">Um procedimento de alocação para alocar um buffer para os dados de transferência</span><span class="sxs-lookup"><span data-stu-id="b398d-107">An alloc procedure to allocate a buffer for the transfer data</span></span>

<span data-ttu-id="b398d-108">Todos esses procedimentos devem usar os argumentos especificados pelo arquivo de cabeçalho gerado por MIDL.</span><span class="sxs-lookup"><span data-stu-id="b398d-108">All of these procedures must use the arguments specified by the MIDL-generated header file.</span></span> <span data-ttu-id="b398d-109">Além disso, o aplicativo cliente deve ter uma variável de estado para identificar onde localizar ou colocar os dados.</span><span class="sxs-lookup"><span data-stu-id="b398d-109">In addition, the client application must have a state variable to identify where to locate or place data.</span></span>

<span data-ttu-id="b398d-110">O procedimento de alocação também pode ser simples ou tão complexo quanto necessário.</span><span class="sxs-lookup"><span data-stu-id="b398d-110">The alloc procedure can also be as simple or as complex as needed.</span></span> <span data-ttu-id="b398d-111">Por exemplo, ele pode retornar um ponteiro para o mesmo buffer sempre que o stub chamar a função, ou pode alocar uma quantidade de memória diferente a cada vez.</span><span class="sxs-lookup"><span data-stu-id="b398d-111">For example, it can return a pointer to the same buffer every time the stub calls the function, or it can allocate a different amount of memory each time.</span></span> <span data-ttu-id="b398d-112">Se os dados já estiverem no formato adequado (uma matriz de elementos de pipe, por exemplo), você poderá coordenar o procedimento de alocação com o procedimento de pull para alocar um buffer que já contém os dados.</span><span class="sxs-lookup"><span data-stu-id="b398d-112">If your data is already in the proper form (an array of pipe elements, for example) you can coordinate the alloc procedure with the pull procedure to allocate a buffer that already contains the data.</span></span> <span data-ttu-id="b398d-113">Nesse caso, o procedimento de pull pode ser uma rotina vazia.</span><span class="sxs-lookup"><span data-stu-id="b398d-113">In that case, your pull procedure could be an empty routine.</span></span>

<span data-ttu-id="b398d-114">A alocação de buffer deve estar em bytes.</span><span class="sxs-lookup"><span data-stu-id="b398d-114">The buffer allocation must be in bytes.</span></span> <span data-ttu-id="b398d-115">Os procedimentos de push e pull, por outro lado, manipulam elementos, cujo tamanho em bytes depende de como eles foram definidos.</span><span class="sxs-lookup"><span data-stu-id="b398d-115">The push and pull procedures, on the other hand, manipulate elements, whose size in bytes depends on how they were defined.</span></span>

<span data-ttu-id="b398d-116">Esta seção aborda a implementação do cliente de pipes de entrada e saída nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="b398d-116">This section discusses the client implementation of input and output pipes in the following sections:</span></span>

-   [<span data-ttu-id="b398d-117">Implementando pipes de entrada no cliente</span><span class="sxs-lookup"><span data-stu-id="b398d-117">Implementing Input Pipes on the Client</span></span>](implementing-input-pipes-on-the-client.md)
-   [<span data-ttu-id="b398d-118">Implementando os pipes de saída no cliente</span><span class="sxs-lookup"><span data-stu-id="b398d-118">Implementing Output Pipes on the Client</span></span>](implementing-output-pipes-on-the-client.md)

 

 




