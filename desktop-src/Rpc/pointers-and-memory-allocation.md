---
title: Ponteiros e alocação de memória
description: A capacidade de alterar a memória por meio de ponteiros geralmente exige que o servidor e o cliente aloquem memória suficiente para os elementos na matriz.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdd4c51207de093dfe2d32ec0c275aa7a05a317
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084784"
---
# <a name="pointers-and-memory-allocation"></a><span data-ttu-id="25ccb-103">Ponteiros e alocação de memória</span><span class="sxs-lookup"><span data-stu-id="25ccb-103">Pointers and Memory Allocation</span></span>

<span data-ttu-id="25ccb-104">A capacidade de alterar a memória por meio de ponteiros geralmente exige que o servidor e o cliente aloquem memória suficiente para os elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="25ccb-104">The ability to change memory through pointers often requires that the server and the client allocate enough memory for the elements in the array.</span></span>

<span data-ttu-id="25ccb-105">Quando um stub deve alocar ou liberar memória, ele chama funções de biblioteca em tempo de execução que, por sua vez, chamam as funções [**\_ \_ disallocate do usuário de MIDL**](/windows/desktop/Midl/midl-user-allocate-1) e o usuário de [**MIDL \_ \_ gratuito**](/windows/desktop/Midl/midl-user-free-1).</span><span class="sxs-lookup"><span data-stu-id="25ccb-105">When a stub must allocate or free memory, it calls run-time library functions that in turn call the functions [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1).</span></span> <span data-ttu-id="25ccb-106">Essas funções não são incluídas como parte da biblioteca de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="25ccb-106">These functions are not included as part of the run-time library.</span></span> <span data-ttu-id="25ccb-107">Você precisa escrever suas próprias versões dessas funções e vinculá-las ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="25ccb-107">You need to write your own versions of these functions and link them with your application.</span></span> <span data-ttu-id="25ccb-108">Dessa forma, você pode decidir como gerenciar a memória.</span><span class="sxs-lookup"><span data-stu-id="25ccb-108">In this way, you can decide how to manage memory.</span></span> <span data-ttu-id="25ccb-109">Ao compilar o arquivo IDL no modo uso-Compatibility (**/OSF**), você não precisa implementar essas funções.</span><span class="sxs-lookup"><span data-stu-id="25ccb-109">When compiling your IDL file in OSF-compatibility (**/osf**) mode, you do not need to implement these functions.</span></span> <span data-ttu-id="25ccb-110">Você deve escrever essas funções nos seguintes protótipos:</span><span class="sxs-lookup"><span data-stu-id="25ccb-110">You must write these functions to the following prototypes:</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

<span data-ttu-id="25ccb-111">Por exemplo, as versões dessas funções para um aplicativo podem simplesmente chamar funções de biblioteca padrão:</span><span class="sxs-lookup"><span data-stu-id="25ccb-111">For example, the versions of these functions for an application can simply call standard library functions:</span></span>


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 