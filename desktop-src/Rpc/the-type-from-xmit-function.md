---
title: A função type_from_xmit
description: Os stubs chamam o tipo \_ da \_ função de transmissão para converter dados de seu tipo transmitido para o tipo que é apresentado ao aplicativo.
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e594e8586522dd3697f5ae62c95851917741f73c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005961"
---
# <a name="the-type_from_xmit-function"></a>O tipo \_ da \_ função de transmissão

Os stubs chamam o **tipo \_ da função de \_ transmissão** para converter dados de seu tipo transmitido para o tipo que é apresentado ao aplicativo. A função é definida como:

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

O primeiro parâmetro é um ponteiro para os dados transmitidos. A função define o segundo parâmetro para apontar para os dados apresentados.

O **tipo \_ da função de \_ transmissão** deve gerenciar memória para o tipo apresentado. A função deve alocar memória para toda a estrutura de dados iniciada no endereço indicado pelo segundo parâmetro, exceto pelo próprio parâmetro (o stub aloca memória para o nó raiz e a transmite para a função). O valor do segundo parâmetro não pode ser alterado durante a chamada. A função pode alterar o conteúdo nesse endereço.

Neste exemplo, a função \_ \_ tipo de link duplo \_ de \_ transmissão converte a matriz dimensionada em uma lista de links duplos. A função retém o ponteiro válido para o início da lista, libera a memória associada ao restante da lista e, em seguida, cria uma nova lista que começa no mesmo ponteiro. A função usa uma função de utilitário, **InsertNewNode**, para acrescentar um nó de lista ao final da lista e atribuir os ponteiros *pNext* e *pPrevious* aos valores apropriados.


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



 

 




