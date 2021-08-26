---
title: A função type_free_xmit de dados
description: Os stubs chamam a função \_ xmit livre \_ de tipo para liberar memória associada aos dados transmitidos.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c192e30ec4f18d70d6e694e6097cb77ee7a2338230868730dc37c1c3207010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016576"
---
# <a name="the-type_free_xmit-function"></a>A função \_ xmit livre \_ de tipo

Os stubs chamam a **função \_ \_ xmit livre de** tipo para liberar memória associada aos dados transmitidos. Depois que [o tipo da função \_ \_ xmit](the-type-from-xmit-function.md) converte os dados transmitidos em seu tipo apresentado, a memória não é mais necessária. A função é definida como:

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

O parâmetro é um ponteiro para a memória que contém o tipo transmitido.

Neste exemplo, a memória contém uma matriz que está em uma única estrutura. A função DOUBLE LINK TYPE free xmit usa a função fornecida pelo usuário \_ \_ \_ \_ midl \_ livre para liberar \_ a memória:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




