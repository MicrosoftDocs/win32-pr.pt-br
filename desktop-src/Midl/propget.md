---
title: atributo propget
description: O atributo \ propget \ especifica uma função de acessador de propriedade. A propriedade deve ter o mesmo nome que a função.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- propget do atributo MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007392"
---
# <a name="propget-attribute"></a>atributo propget

O atributo **\[ propget \]** especifica uma função de acessador de propriedade. A propriedade deve ter o mesmo nome que a função.

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*opcional-atributos de propriedade* 
</dt> <dd>

Zero ou mais atributos de propriedade.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

O tipo dos dados retornados pelo procedimento remoto.

</dd> <dt>

*nome da função* 
</dt> <dd>

O nome do procedimento remoto.

</dd> <dt>

*parameters* 
</dt> <dd>

Zero ou mais parâmetros para o procedimento remoto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma função que tem o atributo propget também deve ter, como seu último parâmetro, um tipo de ponteiro com os **\[** atributos [**out**](out-idl.md) **\]** e **\[** [**retval**](retval.md) **\]** . Se o último parâmetro não tiver os \[ atributos de out, retval \] , o valor de retorno da função será tratado como um \[ parâmetro retval out \] . Por exemplo, uma função com o protótipo

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

é tratado como

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

No máximo, um de **\[ propget \]**, **\[** [**propput**](propput.md) **\]** e **\[** [**propputref**](propputref.md) **\]** pode ser especificado para uma função.

Se o **\[** [](lcid.md) **\]** atributo LCID for usado na lista de parâmetros de uma função que contém um parâmetro com o **\[** atributo [**propput**](propput.md) **\]** , o parâmetro **\[ LCID \]** deverá ser segundo para o último.

### <a name="flags"></a>Flags

INVOCAr \_ PROPERTYGET

## <a name="examples"></a>Exemplos

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 