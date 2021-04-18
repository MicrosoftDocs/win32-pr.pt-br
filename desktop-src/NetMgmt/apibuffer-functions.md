---
title: Funções ApiBuffer
description: As funções de ApiBuffer de gerenciamento de rede são usadas para gerenciar a alocação de memória usada por um aplicativo com funções de gerenciamento de rede.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105756716"
---
# <a name="apibuffer-functions"></a><span data-ttu-id="6bc38-103">Funções ApiBuffer</span><span class="sxs-lookup"><span data-stu-id="6bc38-103">ApiBuffer Functions</span></span>

<span data-ttu-id="6bc38-104">As funções de ApiBuffer de gerenciamento de rede são usadas para gerenciar a alocação de memória usada por um aplicativo com funções de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="6bc38-104">The network management ApiBuffer functions are used to manage memory allocation used by an application with network management functions.</span></span> <span data-ttu-id="6bc38-105">No entanto, em geral, para outra memória usada por um aplicativo, você deve usar as [funções de gerenciamento de memória](/windows/desktop/Memory/memory-management-functions) em vez dessas funções ApiBuffer.</span><span class="sxs-lookup"><span data-stu-id="6bc38-105">However, in general, for other memory used by an application you should use the [memory management functions](/windows/desktop/Memory/memory-management-functions) instead of these ApiBuffer functions.</span></span>

<span data-ttu-id="6bc38-106">As funções ApiBuffer são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6bc38-106">The ApiBuffer functions are listed following.</span></span>



| <span data-ttu-id="6bc38-107">Função</span><span class="sxs-lookup"><span data-stu-id="6bc38-107">Function</span></span>                                                 | <span data-ttu-id="6bc38-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6bc38-108">Description</span></span>                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6bc38-109">**NetApiBufferAllocate**</span><span class="sxs-lookup"><span data-stu-id="6bc38-109">**NetApiBufferAllocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | <span data-ttu-id="6bc38-110">Aloca memória a partir do heap.</span><span class="sxs-lookup"><span data-stu-id="6bc38-110">Allocates memory from the heap.</span></span> <span data-ttu-id="6bc38-111">Chame essa função quando precisar de compatibilidade com a função **NetApiBufferFree** .</span><span class="sxs-lookup"><span data-stu-id="6bc38-111">Call this function when you require compatibility with the **NetApiBufferFree** function.</span></span> |
| [<span data-ttu-id="6bc38-112">**NetApiBufferFree**</span><span class="sxs-lookup"><span data-stu-id="6bc38-112">**NetApiBufferFree**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | <span data-ttu-id="6bc38-113">Libera a memória alocada pela função **NetApiBufferAllocate** e outras funções de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="6bc38-113">Frees memory allocated by the **NetApiBufferAllocate** function and other network management functions.</span></span>                   |
| [<span data-ttu-id="6bc38-114">**NetApiBufferReallocate**</span><span class="sxs-lookup"><span data-stu-id="6bc38-114">**NetApiBufferReallocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | <span data-ttu-id="6bc38-115">Altera o tamanho de um buffer alocado por uma chamada para a função **NetApiBufferAllocate** .</span><span class="sxs-lookup"><span data-stu-id="6bc38-115">Changes the size of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                                |
| [<span data-ttu-id="6bc38-116">**NetApiBufferSize**</span><span class="sxs-lookup"><span data-stu-id="6bc38-116">**NetApiBufferSize**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | <span data-ttu-id="6bc38-117">Retorna o tamanho, em bytes, de um buffer alocado por uma chamada para a função **NetApiBufferAllocate** .</span><span class="sxs-lookup"><span data-stu-id="6bc38-117">Returns the size, in bytes, of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                     |



 

<span data-ttu-id="6bc38-118">Para funções remotas que retornam informações para o chamador, a biblioteca de tempo de execução RPC aloca o buffer que contém as informações de retorno.</span><span class="sxs-lookup"><span data-stu-id="6bc38-118">For remotable functions that return information to the caller, the RPC run-time library allocates the buffer containing the return information.</span></span> <span data-ttu-id="6bc38-119">Quando o chamador terminar de processar as informações, ele deverá chamar a função [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) para liberar o buffer alocado.</span><span class="sxs-lookup"><span data-stu-id="6bc38-119">When the caller has finished processing the information, it must call the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function to free the allocated buffer.</span></span>

 

 