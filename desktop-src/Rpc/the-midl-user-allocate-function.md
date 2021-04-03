---
title: A função midl_user_allocate
description: A \_ função de alocação de usuário MIDL \_ é um procedimento que deve ser fornecido por desenvolvedores de aplicativos RPC.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084726"
---
# <a name="the-midl_user_allocate-function"></a>A função de alocação de \_ usuário MIDL \_

A função de **\_ \_ alocação de usuário MIDL** é um procedimento que deve ser fornecido por desenvolvedores de aplicativos RPC. Ele aloca memória para os stubs RPC e rotinas de biblioteca. A função de **\_ \_ alocação de usuário MIDL** deve corresponder ao seguinte protótipo:

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

O parâmetro *cBytes* especifica o número de bytes a serem alocados. Os aplicativos cliente e os aplicativos de servidor devem implementar a função de **\_ \_ alocação de usuário MIDL** , a menos que você esteja compilando no modo uso-Compatibility (/OSF). Os aplicativos e os stubs gerados chamam o **usuário de MIDL \_ \_ alocar** direta ou indiretamente para gerenciar objetos alocados. Por exemplo:

-   Os aplicativos cliente e servidor chamam **o \_ usuário MIDL \_ ALLOCATE** para alocar memória para o aplicativo, como ao criar um novo nó em uma árvore ou em uma lista vinculada.
-   O stub de servidor chama a **\_ \_ alocação do usuário de MIDL** ao desempacotar dados no espaço de endereço do servidor.
-   O stub do cliente chama a **\_ \_ alocação do usuário de MIDL** ao desempacotar dados do servidor que é referenciado por um \[ \] ponteiro out. Observe que para \[ \] \[ ponteiros in, out \] e \[ Unique \] , o stub do cliente chama o **usuário de MIDL \_ \_ ALLOCATE** somente se o \[ valor do ponteiro exclusivo \] era nulo na entrada e muda para um valor não nulo durante a chamada. Se o \[ \] ponteiro exclusivo não for nulo na entrada, o stub do cliente gravará os dados associados em uma memória existente.

Se **a \_ \_ alocação de usuário MIDL** falhar ao alocar memória, ela deverá retornar um ponteiro nulo.

A função de **\_ \_ alocação de usuário MIDL** deve retornar um ponteiro alinhado de 8 bytes.

Por exemplo, os programas de exemplo fornecidos com a plataforma SDK (Software Development Kit) implementam a **\_ \_ alocação de usuário de MIDL** em termos da função [**malloc**](pointers-and-memory-allocation.md)C:


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> Se o pacote RpcSs estiver habilitado (por exemplo, como resultado do uso do atributo \[ [**habilitar \_ alocação**](/windows/desktop/Midl/enable-allocate) \] ), use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) para alocar memória no lado do servidor. Para obter informações adicionais sobre \[ **habilitar \_ alocar** \] , consulte [referência de MIDL](/windows/desktop/Midl/midl-language-reference).

 

 

 