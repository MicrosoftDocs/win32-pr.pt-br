---
title: A função type_to_xmit
description: Os stubs chamam o tipo \_ para a \_ função de transmissão para converter o tipo apresentado pelo aplicativo no tipo transmitido.
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6a6b250d661fc19b0ee8fb68d21f171960e512
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916490"
---
# <a name="the-type_to_xmit-function"></a><span data-ttu-id="b9107-104">O tipo \_ para a \_ função de transmissão</span><span class="sxs-lookup"><span data-stu-id="b9107-104">The type\_to\_xmit Function</span></span>

<span data-ttu-id="b9107-105">Os stubs chamam o tipo para a função de **\_ \_ transmissão** para converter o tipo apresentado pelo aplicativo no tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="b9107-105">The stubs call the **type\_to\_xmit** function to convert the type that is presented by the application into the transmitted type.</span></span> <span data-ttu-id="b9107-106">A função é definida como:</span><span class="sxs-lookup"><span data-stu-id="b9107-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

<span data-ttu-id="b9107-107">O primeiro parâmetro é um ponteiro para os dados do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9107-107">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="b9107-108">O segundo parâmetro é definido pela função para apontar para os dados transmitidos.</span><span class="sxs-lookup"><span data-stu-id="b9107-108">The second parameter is set by the function to point to the transmitted data.</span></span> <span data-ttu-id="b9107-109">A função deve alocar memória para o tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="b9107-109">The function must allocate memory for the transmitted type.</span></span>

<span data-ttu-id="b9107-110">No exemplo a seguir, o cliente chama o procedimento remoto que tem um parâmetro **\[ in e \] out** do tipo \_ tipo link duplo \_ .</span><span class="sxs-lookup"><span data-stu-id="b9107-110">In the following example, the client calls the remote procedure that has an **\[in, out\]** parameter of type DOUBLE\_LINK\_TYPE.</span></span> <span data-ttu-id="b9107-111">O stub do cliente chama o **tipo para a função \_ de \_ transmissão** , aqui chamado de \_ tipo de link duplo \_ \_ para \_ transmissão, para converter dados de lista de vínculo duplo em uma matriz dimensionada.</span><span class="sxs-lookup"><span data-stu-id="b9107-111">The client stub calls the **type\_to\_xmit** function, here named DOUBLE\_LINK\_TYPE\_to\_xmit, to convert double-linked list data into a sized array.</span></span>

<span data-ttu-id="b9107-112">A função determina o número de elementos na lista, aloca uma matriz grande o suficiente para conter esses elementos e, em seguida, copia os elementos da lista na matriz.</span><span class="sxs-lookup"><span data-stu-id="b9107-112">The function determines the number of elements in the list, allocates an array large enough to hold those elements, then copies the list elements into the array.</span></span> <span data-ttu-id="b9107-113">Antes que a função retorne, o segundo parâmetro, *ppArray*, é definido para apontar para a estrutura de dados alocada recentemente.</span><span class="sxs-lookup"><span data-stu-id="b9107-113">Before the function returns, the second parameter, *ppArray*, is set to point to the newly allocated data structure.</span></span>


```C++
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray)
{
    short cCount = 0;
    DOUBLE_LINK_TYPE * pHead = pList;  // save pointer to start 
    DOUBLE_XMIT_TYPE * pArray;
 
    /* count the number of elements to allocate memory */
    for (; pList != NULL; pList = pList->pNext)
        cCount++;
 
    /* allocate the memory for the array */
    pArray = (DOUBLE_XMIT_TYPE *) MIDL_user_allocate 
         (sizeof(DOUBLE_XMIT_TYPE) + (cCount * sizeof(short)));
    pArray->sSize = cCount;
 
    /* copy the linked list contents into the array */
    cCount = 0;
    for (i = 0, pList = pHead; pList != NULL; pList = pList->pNext)
        pArray->asNumber[cCount++] = pList->sNumber;
 
    /* return the address of the pointer to the array */
    *ppArray = pArray;
}
```



 

 




