---
title: atributo padrão
description: O atributo \ default \ indica que a interface ou dispinterface, definida em uma coclass, representa a interface de programação padrão. Esse atributo destina-se a uso por linguagens de macro.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- atributo padrão MIDL
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453997"
---
# <a name="default-attribute"></a>atributo padrão

O atributo **\[ \] padrão** indica que a [**interface**](interface.md) ou [**dispinterface**](dispinterface.md), definida em uma [**coclass**](coclass.md), representa a interface de programação padrão. Esse atributo destina-se a uso por linguagens de macro.

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a [**coclass**](coclass.md).

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica atributos de [**coclasse**](coclass.md) adicionais. Separe vários atributos com vírgulas.

</dd> <dt>

*coclass-Name* 
</dt> <dd>

Especifica o nome pelo qual outros componentes de software podem fazer referência a essa [**coclasse**](coclass.md).

</dd> <dt>

*atributo opcional-interface-* 
</dt> <dd>

O **\[** atributo de [**origem**](source.md) **\]** , que especifica que uma interface ou dispinterface é de saída, é o único outro atributo que pode ser usado aqui.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma [**coclass**](coclass.md) pode ter no máximo dois membros **\[ padrão \]** . Uma representa a interface de saída (origem) ou a dispinterface, e a outra representa a interface de entrada (coletor) ou a dispinterface. Se o atributo **\[ padrão \]** não for especificado para nenhum membro da **coclasse** ou **cotipo**, os primeiros membros de saída e de entrada que não têm o atributo **\[** [**restrito**](restricted.md) **\]** serão tratados como os padrões.

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FDEFAULT

## <a name="examples"></a>Exemplos

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Restricted**](restricted.md)
</dt> <dt>

[**original**](source.md)
</dt> </dl>

 

 