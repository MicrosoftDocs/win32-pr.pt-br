---
title: handle_t atributo
description: A \_ palavra-chave t do manipulador declara um objeto para ser do identificador de tipo de identificador primitivo \_ t. Um identificador de associação primitiva é um objeto de dados que pode ser usado pelo aplicativo para representar a associação.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t do atributo MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293955"
---
# <a name="handle_t-attribute"></a>\_atributo t do manipulador

A palavra-chave **\_ t do manipulador** declara um objeto para ser do identificador de tipo de identificador primitivo **\_ t**. Um identificador de associação primitiva é um objeto de dados que pode ser usado pelo aplicativo para representar a associação.

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a>Parâmetros

Este atributo não tem parâmetros.

## <a name="remarks"></a>Comentários

O **tipo \_ t de identificador** é um dos tipos predefinidos da IDL (Interface Definition Language). Ele pode aparecer como um especificador de tipo em declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).

No Microsoft RPC, os parâmetros do tipo **identificador \_ t** só podem ocorrer como **\[** [**em**](in.md) **\]** parâmetros. Os identificadores primitivos não podem ter o **\[** atributo [**exclusivo**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** .

Parâmetros do tipo **Handle \_ t** (parâmetros de identificador primitivo) não são transmitidos na rede.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[Associação e identificadores](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> </dl>

 

 