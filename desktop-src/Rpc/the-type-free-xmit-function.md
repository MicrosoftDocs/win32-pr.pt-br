---
title: A função type_free_xmit
description: Os stubs chamam a \_ função de transmissão gratuita de tipo \_ para liberar memória associada aos dados transmitidos.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33d5cb8079d50923de2161b0384550829a5f22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159891"
---
# <a name="the-type_free_xmit-function"></a><span data-ttu-id="36cb2-104">A \_ função de \_ transmissão gratuita de tipo</span><span class="sxs-lookup"><span data-stu-id="36cb2-104">The type\_free\_xmit Function</span></span>

<span data-ttu-id="36cb2-105">Os stubs chamam a função de **\_ \_ transmissão gratuita de tipo** para liberar memória associada aos dados transmitidos.</span><span class="sxs-lookup"><span data-stu-id="36cb2-105">The stubs call the **type\_free\_xmit** function to free memory associated with the transmitted data.</span></span> <span data-ttu-id="36cb2-106">Depois que o [tipo \_ da função de \_ transmissão](the-type-from-xmit-function.md) converte os dados transmitidos para seu tipo apresentado, a memória não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="36cb2-106">After the [type\_from\_xmit](the-type-from-xmit-function.md) function converts the transmitted data to its presented type, the memory is no longer needed.</span></span> <span data-ttu-id="36cb2-107">A função é definida como:</span><span class="sxs-lookup"><span data-stu-id="36cb2-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

<span data-ttu-id="36cb2-108">O parâmetro é um ponteiro para a memória que contém o tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="36cb2-108">The parameter is a pointer to the memory that contains the transmitted type.</span></span>

<span data-ttu-id="36cb2-109">Neste exemplo, a memória contém uma matriz que está em uma única estrutura.</span><span class="sxs-lookup"><span data-stu-id="36cb2-109">In this example, the memory contains an array that is in a single structure.</span></span> <span data-ttu-id="36cb2-110">A \_ transmissão gratuita do tipo de link da função \_ \_ \_ usa o usuário de MIDL da função fornecida pelo usuário \_ \_ livre para liberar a memória:</span><span class="sxs-lookup"><span data-stu-id="36cb2-110">The function DOUBLE\_LINK\_TYPE\_free\_xmit uses the user-supplied function midl\_user\_free to free the memory:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




