---
title: atributo requestedit
description: O atributo \ requestedit \ indica que a propriedade dá suporte à notificação OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- requestedit do atributo MIDL
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105750261"
---
# <a name="requestedit-attribute"></a>atributo requestedit

O atributo **\[ \] requestedit** indica que a propriedade dá suporte à notificação **OnRequestEdit** .

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*opcional-atributos* 
</dt> <dd>

Zero ou mais atributos MIDL.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função no arquivo IDL.

</dd> <dt>

*params* 
</dt> <dd>

Zero ou mais parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

O suporte à notificação **OnRequestEdit** significa que, antes que uma alteração seja feita, o objeto enviará ao cliente uma solicitação de permissão para alterar uma propriedade. Um objeto pode dar suporte à ligação de dados, mas não tem esse atributo.

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

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 