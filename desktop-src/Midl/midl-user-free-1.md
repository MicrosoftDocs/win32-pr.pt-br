---
title: midl_user_free atributo
description: A \_ função gratuita do usuário MIDL \_ é fornecida por aplicativos cliente e servidor para desalocar a memória alocada dinamicamente.
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free do atributo MIDL
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293982"
---
# <a name="midl_user_free-attribute"></a>atributo de usuário de MIDL \_ \_ livre

A **função \_ \_ gratuita do usuário MIDL** é fornecida por aplicativos cliente e servidor para desalocar a memória alocada dinamicamente.

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DTI* 
</dt> <dd>

Um ponteiro para o bloco de memória a ser liberado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O aplicativo cliente e o aplicativo de servidor devem implementar a função de **\_ usuário \_ de MIDL** , a menos que você esteja compilando no modo uso-Compatibility ([**/OSF**](-osf.md)). A função de **\_ usuário \_ de MIDL** deve ser capaz de liberar todo o armazenamento alocado por [**\_ \_ alocação de usuário MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function).

Aplicativos e stubs chamam o **\_ usuário MIDL \_ gratuito** ao lidar com objetos referenciados por ponteiros:

-   O aplicativo de servidor deve chamar o **\_ usuário MIDL \_ gratuitamente** para memória livre alocada pelo aplicativos € ", por exemplo, ao excluir um nó especificado.
-   O stub de servidor chama o **\_ usuário MIDL \_ gratuitamente** para liberar memória no servidor após o marshaling de todos os **\[** [](out-idl.md) **\]** argumentos, **\[** argumentos [**de**](in.md) **saída \]** e o valor de retorno.

## <a name="examples"></a>Exemplos


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Storage**](arrays-1.md)
</dt> <dt>

[Matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos de matriz e de Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**\_alocar usuário de MIDL \_**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> </dl>

 

 