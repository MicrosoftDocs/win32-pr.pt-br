---
title: Ponteiros e alocação de memória
description: A capacidade de alterar a memória por meio de ponteiros geralmente exige que o servidor e o cliente aloquem memória suficiente para os elementos na matriz.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdd4c51207de093dfe2d32ec0c275aa7a05a317
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084784"
---
# <a name="pointers-and-memory-allocation"></a>Ponteiros e alocação de memória

A capacidade de alterar a memória por meio de ponteiros geralmente exige que o servidor e o cliente aloquem memória suficiente para os elementos na matriz.

Quando um stub deve alocar ou liberar memória, ele chama funções de biblioteca em tempo de execução que, por sua vez, chamam as funções [**\_ \_ disallocate do usuário de MIDL**](/windows/desktop/Midl/midl-user-allocate-1) e o usuário de [**MIDL \_ \_ gratuito**](/windows/desktop/Midl/midl-user-free-1). Essas funções não são incluídas como parte da biblioteca de tempo de execução. Você precisa escrever suas próprias versões dessas funções e vinculá-las ao seu aplicativo. Dessa forma, você pode decidir como gerenciar a memória. Ao compilar o arquivo IDL no modo uso-Compatibility (**/OSF**), você não precisa implementar essas funções. Você deve escrever essas funções nos seguintes protótipos:

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



 

 