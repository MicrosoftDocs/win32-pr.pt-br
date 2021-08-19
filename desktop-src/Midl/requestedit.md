---
title: atributo requestedit
description: O atributo \ requestedit\ indica que a propriedade dá suporte à notificação OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- atributo requestedit MIDL
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51a894e5d4a09e7535e10a73e1bd118245e5886e0cdbb23b0f0645e588ab4adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146349"
---
# <a name="requestedit-attribute"></a>atributo requestedit

O **\[ atributo \] requestedit** indica que a propriedade dá suporte à **notificação OnRequestEdit.**

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributos opcionais* 
</dt> <dd>

Zero ou mais atributos MIDL.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função no arquivo IDL.

</dd> <dt>

*params* 
</dt> <dd>

Zero ou mais parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

Dar suporte à notificação **onRequestEdit** significa que, antes de uma alteração ser feita, o objeto enviará ao cliente uma solicitação de permissão para alterar uma propriedade. Um objeto pode dar suporte à associação de dados, mas não tem esse atributo.

### <a name="flags"></a>Flags

FUNCFLAG \_ FREQUESTEDIT, VARFLAG \_ FREQUESTEDIT

## <a name="examples"></a>Exemplos

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 