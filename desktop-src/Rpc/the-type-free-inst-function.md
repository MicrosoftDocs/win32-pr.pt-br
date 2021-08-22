---
title: A função type_free_inst
description: Os stubs chamam a \_ função de tipo Free \_ Inst para liberar memória associada ao tipo apresentado.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc71c8d3557c62eec39fe9a90855ef3ed057d29c21ec60a82ddc7fe04207f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923705"
---
# <a name="the-type_free_inst-function"></a>A \_ \_ função Inst sem tipo

Os stubs chamam a função de **tipo \_ Free \_ Inst** para liberar memória associada ao tipo apresentado. A função é definida como:

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

O parâmetro aponta para a instância de tipo apresentada. Este objeto não deve ser liberado. Para obter uma discussão sobre quando chamar a função, consulte [o \_ atributo transmitir como](the-transmit-as-attribute.md).

No exemplo a seguir, a lista de links duplos é liberada ao percorrer a lista até o final, fazendo backup e liberando cada elemento da lista.


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



 

 




