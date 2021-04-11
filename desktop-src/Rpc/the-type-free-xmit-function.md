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
# <a name="the-type_free_xmit-function"></a>A \_ função de \_ transmissão gratuita de tipo

Os stubs chamam a função de **\_ \_ transmissão gratuita de tipo** para liberar memória associada aos dados transmitidos. Depois que o [tipo \_ da função de \_ transmissão](the-type-from-xmit-function.md) converte os dados transmitidos para seu tipo apresentado, a memória não é mais necessária. A função é definida como:

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

O parâmetro é um ponteiro para a memória que contém o tipo transmitido.

Neste exemplo, a memória contém uma matriz que está em uma única estrutura. A \_ transmissão gratuita do tipo de link da função \_ \_ \_ usa o usuário de MIDL da função fornecida pelo usuário \_ \_ livre para liberar a memória:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




