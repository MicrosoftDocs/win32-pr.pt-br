---
title: ID do atributo
description: O atributo \ id\ especifica um DISPID para uma função de membro (uma propriedade ou um método, em uma interface ou dispinterface).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- atributo de id MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4d783265ebfcf9dca454c80c39031dc0c37dfb63a8749b4d0e6299a510d91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643062"
---
# <a name="id-attribute"></a>ID do atributo

O **\[ atributo \] id** especifica um DISPID para uma função de membro (uma propriedade ou um método, em uma interface ou dispinterface).

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*id-num* 
</dt> <dd>

DISPID para a função.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos de interface MIDL.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função no arquivo IDL.

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Zero ou mais parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o atributo **\[ id \]** quando quiser atribuir um DISPID padrão (como DISPID VALUE, DISPID NEWENUM etc.) a um método ou propriedade ou quando você implementar seu próprio \_ \_ **IDispatch::Invoke** em vez de delegar a **DispInvoke** / **ITypeInfo::Invoke**.

Se você não usar o **\[ atributo id \]** em uma interface, o compilador MIDL atribuirá um DISPID para você. No entanto, ao especificar uma dispinterface usando propriedades e métodos, você deve especificar um DISPID para cada propriedade e método.

O *id-num* é um valor integral positivo de 32 bits. As IDs negativas são reservadas para uso pela Automação.

## <a name="examples"></a>Exemplos

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 