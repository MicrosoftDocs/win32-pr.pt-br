---
title: ID do atributo
description: O atributo \ ID \ especifica um DISPID para uma função membro (uma propriedade ou um método, em uma interface ou Dispinterface).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- atributo de ID MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365872"
---
# <a name="id-attribute"></a>ID do atributo

O atributo **\[ ID \]** especifica um DISPID para uma função membro (uma propriedade ou um método, em uma interface ou Dispinterface).

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID-num* 
</dt> <dd>

DISPID para a função.

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos de interface MIDL.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função no arquivo IDL.

</dd> <dt>

*opcional-lista de parâmetros* 
</dt> <dd>

Zero ou mais parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o atributo **\[ \] ID** quando desejar atribuir um DISPID padrão (como o valor DISPID \_ , DISPID \_ NEWENUM etc.) a um método ou propriedade, ou quando você implementar seu próprio **IDispatch:: Invoke** em vez de delegar para o **DispInvoke** / **ITypeInfo:: Invoke**.

Se você não usar o atributo **\[ ID \]** em uma interface, o compilador MIDL atribuirá um DISPID para você. No entanto, ao especificar uma dispinterface usando propriedades e métodos, você deve especificar um DISPID para cada propriedade e método.

O *ID-num* é um valor integral positivo de 32 bits. As IDs negativas são reservadas para uso pela automação.

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

[**interface**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 