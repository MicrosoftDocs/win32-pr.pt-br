---
title: midl_user_allocate atributo
description: A \_ função de alocação de usuário MIDL \_ é uma função que os aplicativos cliente e servidor fornecem para alocar memória.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate do atributo MIDL
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16729e0a0a422c8ed2d8a8f323b563cb6a268fcb041e6a9d2ba13a9c9b847d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806654"
---
# <a name="midl_user_allocate-attribute"></a>atributo de alocação de \_ usuário MIDL \_

A função de **\_ \_ alocação de usuário MIDL** é uma função que os aplicativos cliente e servidor fornecem para alocar memória.

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cBytes* 
</dt> <dd>

Especifica a contagem de bytes a serem alocados.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os aplicativos cliente e os aplicativos de servidor devem implementar a função de **\_ \_ alocação de usuário MIDL** , a menos que você esteja compilando no modo uso-Compatibility ([**/OSF**](-osf.md)). Os aplicativos e os stubs gerados chamam a **\_ \_ alocação de usuário de MIDL** ao lidar com objetos referenciados por ponteiros:

-   O aplicativo de servidor deve chamar o **\_ usuário MIDL \_ ALLOCATE** para alocar memória para o aplicativos € ", por exemplo, ao criar um novo nó.
-   O stub do servidor chama o **usuário de MIDL \_ \_ alocar** ao desempacotar dados apontados para o espaço de endereço do servidor.
-   O stub do cliente chama a **\_ \_ alocação do usuário de MIDL** ao desempacotar dados do servidor que é referenciado por um ponteiro [**out**](out-idl.md) . Observe que para **\[** [](in.md) **\]** ponteiros in, **\[ out \]** e **\[** [**Unique**](unique.md) **\]** , o stub do cliente chama o **usuário de MIDL \_ \_ ALLOCATE** somente se o valor do ponteiro **\[ exclusivo \]** era **nulo** na entrada e muda para um valor não **nulo** durante a chamada. Se o ponteiro **\[ \] exclusivo** não for **nulo** na entrada, o stub do cliente gravará os dados associados em uma memória existente.

Se **a \_ \_ alocação de usuário MIDL** falhar ao alocar memória, ela deverá retornar um ponteiro **nulo** .

É recomendável que **a \_ \_ alocação de usuário de MIDL** retorne um ponteiro que tenha 8 bytes alinhados.

## <a name="examples"></a>Exemplos


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[**aloca**](allocate.md)
</dt> <dt>

[**matrizes**](arrays-1.md)
</dt> <dt>

[Matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos de matriz e de Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**usuário de MIDL \_ \_ gratuito**](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> </dl>

 

 