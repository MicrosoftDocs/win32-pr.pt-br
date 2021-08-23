---
title: Ponteiros e alocação de memória
description: A capacidade de alterar a memória por meio de ponteiros geralmente requer que o servidor e o cliente alocem memória suficiente para os elementos na matriz.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d634b209c1f6369429c432d5fad5d4e64b47aeae16778efd8916c00e65911e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927356"
---
# <a name="pointers-and-memory-allocation"></a>Ponteiros e alocação de memória

A capacidade de alterar a memória por meio de ponteiros geralmente requer que o servidor e o cliente alocem memória suficiente para os elementos na matriz.

Quando um stub deve alocar ou liberar memória, ele chama funções de biblioteca em tempo de executar que, por sua vez, chamam as funções de alocação de usuário médio e usuário [**midl \_ \_ gratuito.**](/windows/desktop/Midl/midl-user-free-1) [**\_ \_**](/windows/desktop/Midl/midl-user-allocate-1) Essas funções não são incluídas como parte da biblioteca em tempo de executar. Você precisa escrever suas próprias versões dessas funções e vinculá-las ao seu aplicativo. Dessa forma, você pode decidir como gerenciar a memória. Ao compilar o arquivo IDL no modo de compatibilidade do OSF (**/osf**), você não precisa implementar essas funções. Você deve gravar essas funções nos seguintes protótipos:

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

Por exemplo, as versões dessas funções para um aplicativo podem simplesmente chamar funções de biblioteca padrão:


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 