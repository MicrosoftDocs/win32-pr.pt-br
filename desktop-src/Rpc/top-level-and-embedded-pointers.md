---
title: Top-Level e ponteiros inseridos
description: Para entender como os ponteiros e seus elementos de dados associados são alocados no Microsoft RPC, você precisa diferenciar os ponteiros de nível superior e os ponteiros inseridos.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453704"
---
# <a name="top-level-and-embedded-pointers"></a><span data-ttu-id="f49c3-103">Top-Level e ponteiros inseridos</span><span class="sxs-lookup"><span data-stu-id="f49c3-103">Top-Level and Embedded Pointers</span></span>

<span data-ttu-id="f49c3-104">Para entender como os ponteiros e seus elementos de dados associados são alocados no Microsoft RPC, você precisa diferenciar os *ponteiros de nível superior* e os *ponteiros inseridos*.</span><span class="sxs-lookup"><span data-stu-id="f49c3-104">To understand how pointers and their associated data elements are allocated in Microsoft RPC, you have to differentiate between *top-level pointers* and *embedded pointers*.</span></span> <span data-ttu-id="f49c3-105">Também é útil fazer referência ao conjunto de todos os ponteiros que não são ponteiros de nível superior.</span><span class="sxs-lookup"><span data-stu-id="f49c3-105">It is also useful to refer to the set of all pointers that are not top-level pointers.</span></span>

<span data-ttu-id="f49c3-106">Os *ponteiros de nível superior* são aqueles especificados como os nomes dos parâmetros nos protótipos de função.</span><span class="sxs-lookup"><span data-stu-id="f49c3-106">*Top-level pointers* are those that are specified as the names of parameters in function prototypes.</span></span> <span data-ttu-id="f49c3-107">Ponteiros de nível superior e seus referents são sempre alocados no servidor.</span><span class="sxs-lookup"><span data-stu-id="f49c3-107">Top-level pointers and their referents are always allocated on the server.</span></span>

<span data-ttu-id="f49c3-108">*Ponteiros inseridos* são ponteiros inseridos em estruturas de dados como matrizes, estruturas e uniões.</span><span class="sxs-lookup"><span data-stu-id="f49c3-108">*Embedded pointers* are pointers that are embedded in data structures such as arrays, structures, and unions.</span></span> <span data-ttu-id="f49c3-109">Quando os ponteiros inseridos só gravam a saída em um buffer e são nulos na entrada, o aplicativo do servidor pode alterar seus valores para não nulo.</span><span class="sxs-lookup"><span data-stu-id="f49c3-109">When embedded pointers only write output to a buffer and are null on input, the server application can change their values to non-null.</span></span> <span data-ttu-id="f49c3-110">Nesse caso, os stubs de cliente alocam a nova memória para esses dados.</span><span class="sxs-lookup"><span data-stu-id="f49c3-110">In this case, the client stubs allocate new memory for this data.</span></span>

<span data-ttu-id="f49c3-111">Se o ponteiro inserido não for nulo no cliente antes da chamada, os stubs não alocarão memória no cliente no retorno.</span><span class="sxs-lookup"><span data-stu-id="f49c3-111">If the embedded pointer is not null on the client before the call, the stubs do not allocate memory on the client on return.</span></span> <span data-ttu-id="f49c3-112">Em vez disso, os stubs tentam gravar a memória associada ao ponteiro inserido na memória existente no cliente associado a esse ponteiro, substituindo os dados já ali.</span><span class="sxs-lookup"><span data-stu-id="f49c3-112">Instead, the stubs attempt to write the memory associated with the embedded pointer into the existing memory on the client associated with that pointer, overwriting the data already there.</span></span>

> [!Note]  
> <span data-ttu-id="f49c3-113">Para dados lidos ou gravados em um buffer, e que não especifica o tamanho do buffer, o comprimento da saída deve ser menor ou igual ao comprimento da entrada.</span><span class="sxs-lookup"><span data-stu-id="f49c3-113">For data read from or writen to a buffer, and which does not specify the buffer size, output length must be less than or equal to input length.</span></span> <span data-ttu-id="f49c3-114">Uma exceção RPC é gerada quando o estouro é detectado.</span><span class="sxs-lookup"><span data-stu-id="f49c3-114">An RPC exception is raised when overflow is detected.</span></span> <span data-ttu-id="f49c3-115">Para dados de cadeia de caracteres, o comprimento de saída é determinado pela verificação do comprimento da cadeia de caracteres de entrada.</span><span class="sxs-lookup"><span data-stu-id="f49c3-115">For string data, output length is determined by checking length of the input string.</span></span> <span data-ttu-id="f49c3-116">Portanto, cadeias de caracteres de saída não podem exceder o comprimento das cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="f49c3-116">Therefore, output strings cannot exceed length of input strings.</span></span> <span data-ttu-id="f49c3-117">As diretrizes de práticas recomendadas são evitar isso sempre incluindo um parâmetro de tamanho especificado para indicar o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="f49c3-117">Best practice guidance is to avoid this by always including a size-specified parameter to indicate size of the buffer.</span></span>

 

<span data-ttu-id="f49c3-118">Ponteiros de somente gravação inseridos são discutidos na [combinação de ponteiros e atributos direcionais](combining-pointer-and-directional-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="f49c3-118">Embedded write-only pointers are discussed in [Combining Pointer and Directional Attributes](combining-pointer-and-directional-attributes.md).</span></span>

<span data-ttu-id="f49c3-119">O termo *ponteiros de nível nontop* refere-se a todos os ponteiros que não são especificados como nomes de parâmetro no protótipo de função, incluindo ponteiros incorporados e vários níveis de ponteiros aninhados.</span><span class="sxs-lookup"><span data-stu-id="f49c3-119">The term *nontop-level pointers* refers to all pointers that are not specified as parameter names in the function prototype, including both embedded pointers and multiple levels of nested pointers.</span></span>

 

 




