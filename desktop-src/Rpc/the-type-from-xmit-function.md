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
# <a name="the-type_from_xmit-function"></a><span data-ttu-id="aa994-104">O tipo \_ da \_ função de transmissão</span><span class="sxs-lookup"><span data-stu-id="aa994-104">The type\_from\_xmit Function</span></span>

<span data-ttu-id="aa994-105">Os stubs chamam o **tipo \_ da função de \_ transmissão** para converter dados de seu tipo transmitido para o tipo que é apresentado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa994-105">The stubs call the **type\_from\_xmit** function to convert data from its transmitted type to the type that is presented to the application.</span></span> <span data-ttu-id="aa994-106">A função é definida como:</span><span class="sxs-lookup"><span data-stu-id="aa994-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

<span data-ttu-id="aa994-107">O primeiro parâmetro é um ponteiro para os dados transmitidos.</span><span class="sxs-lookup"><span data-stu-id="aa994-107">The first parameter is a pointer to the transmitted data.</span></span> <span data-ttu-id="aa994-108">A função define o segundo parâmetro para apontar para os dados apresentados.</span><span class="sxs-lookup"><span data-stu-id="aa994-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="aa994-109">O **tipo \_ da função de \_ transmissão** deve gerenciar memória para o tipo apresentado.</span><span class="sxs-lookup"><span data-stu-id="aa994-109">The **type\_from\_xmit** function must manage memory for the presented type.</span></span> <span data-ttu-id="aa994-110">A função deve alocar memória para toda a estrutura de dados iniciada no endereço indicado pelo segundo parâmetro, exceto pelo próprio parâmetro (o stub aloca memória para o nó raiz e a transmite para a função).</span><span class="sxs-lookup"><span data-stu-id="aa994-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="aa994-111">O valor do segundo parâmetro não pode ser alterado durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="aa994-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="aa994-112">A função pode alterar o conteúdo nesse endereço.</span><span class="sxs-lookup"><span data-stu-id="aa994-112">The function can change the contents at that address.</span></span>

<span data-ttu-id="aa994-113">Neste exemplo, a função \_ \_ tipo de link duplo \_ de \_ transmissão converte a matriz dimensionada em uma lista de links duplos.</span><span class="sxs-lookup"><span data-stu-id="aa994-113">In this example, the function DOUBLE\_LINK\_TYPE\_from\_xmit converts the sized array to a double-linked list.</span></span> <span data-ttu-id="aa994-114">A função retém o ponteiro válido para o início da lista, libera a memória associada ao restante da lista e, em seguida, cria uma nova lista que começa no mesmo ponteiro.</span><span class="sxs-lookup"><span data-stu-id="aa994-114">The function retains the valid pointer to the beginning of the list, frees memory associated with the rest of the list, then creates a new list that starts at the same pointer.</span></span> <span data-ttu-id="aa994-115">A função usa uma função de utilitário, **InsertNewNode**, para acrescentar um nó de lista ao final da lista e atribuir os ponteiros *pNext* e *pPrevious* aos valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="aa994-115">The function uses a utility function, **InsertNewNode**, to append a list node to the end of the list and to assign the *pNext* and *pPrevious* pointers to appropriate values.</span></span>


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



 

 




