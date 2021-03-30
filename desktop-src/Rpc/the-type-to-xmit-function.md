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
# <a name="the-type_to_xmit-function"></a>O tipo \_ para a \_ função de transmissão

Os stubs chamam o tipo para a função de **\_ \_ transmissão** para converter o tipo apresentado pelo aplicativo no tipo transmitido. A função é definida como:

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

O primeiro parâmetro é um ponteiro para os dados do aplicativo. O segundo parâmetro é definido pela função para apontar para os dados transmitidos. A função deve alocar memória para o tipo transmitido.

No exemplo a seguir, o cliente chama o procedimento remoto que tem um parâmetro **\[ in e \] out** do tipo \_ tipo link duplo \_ . O stub do cliente chama o **tipo para a função \_ de \_ transmissão** , aqui chamado de \_ tipo de link duplo \_ \_ para \_ transmissão, para converter dados de lista de vínculo duplo em uma matriz dimensionada.

A função determina o número de elementos na lista, aloca uma matriz grande o suficiente para conter esses elementos e, em seguida, copia os elementos da lista na matriz. Antes que a função retorne, o segundo parâmetro, *ppArray*, é definido para apontar para a estrutura de dados alocada recentemente.


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



 

 




