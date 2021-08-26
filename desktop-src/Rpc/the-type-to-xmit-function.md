---
title: A função type_to_xmit função
description: Os stubs chamam o tipo para função xmit para converter o tipo apresentado \_ pelo aplicativo no tipo \_ transmitido.
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970d4a0de9675ac7a5f1b1c1449521177ecb661a1a80fd9ef609a6dc630605a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016496"
---
# <a name="the-type_to_xmit-function"></a>O tipo \_ para \_ xmit Function

Os stubs chamam o **tipo \_ para função \_ xmit** para converter o tipo apresentado pelo aplicativo no tipo transmitido. A função é definida como:

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

O primeiro parâmetro é um ponteiro para os dados do aplicativo. O segundo parâmetro é definido pela função para apontar para os dados transmitidos. A função deve alocar memória para o tipo transmitido.

No exemplo a seguir, o cliente chama o procedimento remoto que tem um **\[ parâmetro de entrada e \]** saída do tipo DOUBLE LINK \_ \_ TYPE. O stub do cliente chama o tipo para função **\_ \_ xmit,** aqui chamado DOUBLE LINK TYPE para xmit, para converter dados de lista de vinculados duplos \_ em uma matriz \_ \_ \_ dimensionada.

A função determina o número de elementos na lista, aloca uma matriz grande o suficiente para manter esses elementos e copia os elementos da lista para a matriz. Antes que a função retorne, o segundo parâmetro, *ppArray*, é definido para apontar para a estrutura de dados recém-alocada.


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



 

 




