---
title: A função type_free_inst
description: Os stubs chamam a \_ função de tipo Free \_ Inst para liberar memória associada ao tipo apresentado.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3754106cf8e0cc6e338f91d6c233181aa33038eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822642"
---
# <a name="the-type_free_inst-function"></a><span data-ttu-id="9f6dc-104">A \_ \_ função Inst sem tipo</span><span class="sxs-lookup"><span data-stu-id="9f6dc-104">The type\_free\_inst Function</span></span>

<span data-ttu-id="9f6dc-105">Os stubs chamam a função de **tipo \_ Free \_ Inst** para liberar memória associada ao tipo apresentado.</span><span class="sxs-lookup"><span data-stu-id="9f6dc-105">The stubs call the **type\_free\_inst** function to free memory associated with the presented type.</span></span> <span data-ttu-id="9f6dc-106">A função é definida como:</span><span class="sxs-lookup"><span data-stu-id="9f6dc-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="9f6dc-107">O parâmetro aponta para a instância de tipo apresentada.</span><span class="sxs-lookup"><span data-stu-id="9f6dc-107">The parameter points to the presented type instance.</span></span> <span data-ttu-id="9f6dc-108">Este objeto não deve ser liberado.</span><span class="sxs-lookup"><span data-stu-id="9f6dc-108">This object should not be freed.</span></span> <span data-ttu-id="9f6dc-109">Para obter uma discussão sobre quando chamar a função, consulte [o \_ atributo transmitir como](the-transmit-as-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="9f6dc-109">For a discussion on when to call the function, see [The transmit\_as Attribute](the-transmit-as-attribute.md).</span></span>

<span data-ttu-id="9f6dc-110">No exemplo a seguir, a lista de links duplos é liberada ao percorrer a lista até o final, fazendo backup e liberando cada elemento da lista.</span><span class="sxs-lookup"><span data-stu-id="9f6dc-110">In the following example, the double-linked list is freed by walking the list to its end, then backing up and freeing each element of the list.</span></span>


```C++
void __RPC_USER DOUBLE_LINK_TYPE_free_inst(
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    while (pList->pNext != NULL)  // go to end of the list
        pList = pList->pNext;

    pList = pList->pPrevious;
    while (pList != NULL) 
    {  
        // back through the list
        midl_user_free(pList->pNext);
        pList = pList->pPrevious;
    }
} 
```



 

 




