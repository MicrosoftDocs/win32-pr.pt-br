---
title: atributo vinculável
description: O atributo \ acoplável \ indica que a propriedade dá suporte à vinculação de dados.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- atributo vinculável MIDL
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105789784"
---
# <a name="bindable-attribute"></a>atributo vinculável

O atributo **\[ acoplável \]** indica que a propriedade dá suporte à vinculação de dados.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-atributo-lista* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos IDL que se aplicam à interface como um todo. Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam ao protótipo de função para uma propriedade ou um método em uma [**interface**](interface.md) ou [**dispinterface**](dispinterface.md). Os seguintes atributos são válidos: [**\[ HelpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ String \]**](string.md), [**\[ defaultbind \]**](defaultbind.md), [**\[ displaybind \]**](displaybind.md), [**\[ immediatebind \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ propput \]**](propput.md), [**\[ propputref \]**](propputref.md)e [**\[ vararg \]**](vararg.md). Se **vararg** for especificado, o último parâmetro deverá ser uma matriz segura do tipo Variant. Separe vários atributos com vírgulas.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função à qual o atributo **\[ vinculável \]** será aplicado.

</dd> <dt>

*params* 
</dt> <dd>

Lista de parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao dar suporte à ligação de dados, o atributo **\[ vinculável \]** permite que o cliente seja notificado sempre que uma propriedade tiver alterado o valor. (Se você quiser que o cliente seja notificado de alterações iminentes em uma propriedade, use o atributo [**\[ requestedit \]**](requestedit.md) .)

Como o atributo **\[ acoplável \]** se refere à propriedade como um todo, ele deve ser especificado onde quer que a propriedade seja definida. Portanto, você precisa especificar o atributo na função de acesso à propriedade e na função de configuração de propriedade.

### <a name="flags"></a>Flags

FUNCFLAG \_ FBINDABLE, VARFLAG \_ FBINDABLE

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**immediatebind**](immediatebind.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**requestedit**](requestedit.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**vararg**](vararg.md)
</dt> </dl>

 

 