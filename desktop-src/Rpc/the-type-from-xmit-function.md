---
title: A função type_from_xmit de dados
description: Os stubs chamam o tipo da função xmit para converter dados de seu tipo transmitido para o \_ tipo que é apresentado ao \_ aplicativo.
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a38e372467208c76111728080037c65f5dca2856304a49f06e7e33426277eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923695"
---
# <a name="the-type_from_xmit-function"></a>O tipo \_ da \_ função xmit

Os stubs chamam o **tipo \_ da função \_ xmit** para converter dados de seu tipo transmitido para o tipo que é apresentado ao aplicativo. A função é definida como:

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

O primeiro parâmetro é um ponteiro para os dados transmitidos. A função define o segundo parâmetro para apontar para os dados apresentados.

O **tipo da função \_ \_ xmit** deve gerenciar a memória para o tipo apresentado. A função deve alocar memória para toda a estrutura de dados que começa no endereço indicado pelo segundo parâmetro, exceto pelo próprio parâmetro (o stub aloca memória para o nó raiz e o passa para a função). O valor do segundo parâmetro não pode ser alternado durante a chamada. A função pode alterar o conteúdo nesse endereço.

Neste exemplo, a função DOUBLE LINK TYPE de xmit converte a matriz \_ \_ \_ \_ dimensionada em uma lista vinculada dupla. A função retém o ponteiro válido para o início da lista, libera a memória associada ao restante da lista e, em seguida, cria uma nova lista que começa no mesmo ponteiro. A função usa uma função de **utilitário, InsertNewNode,** para anexar um nó de lista ao final da lista e atribuir os *ponteiros pNext* e *pPrevious* aos valores apropriados.


```C++
void __RPC_USER DOUBLE_LINK_TYPE_from_xmit(
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    DOUBLE_LINK_TYPE *pCurrent;
    int i;
 
    if (pArray->sSize <= 0) 
    {  
        // error checking
        return;
    }
 
    if (pList == NULL) // if invalid, create the list head
        pList = InsertNewNode(pArray->asNumber[0], NULL);             
    else 
    {    
        DOUBLE_LINK_TYPE_free_inst(pList);  // free all other nodes
        pList->sNumber = pArray->asNumber[0];
        pList->pNext = NULL; 
    }
 
    pCurrent = pList; 
    for (i = 1; i < pArray->sSize; i++)  
        pCurrent = InsertNewNode(pArray->asNumber[i], pCurrent);
    
    return;
}
```



 

 




