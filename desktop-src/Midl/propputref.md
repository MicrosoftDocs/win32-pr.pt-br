---
title: atributo propputref
description: O atributo \ propputref \ especifica uma função de configuração de propriedade que usa uma referência em vez de um valor.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- propputref do atributo MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917180"
---
# <a name="propputref-attribute"></a>atributo propputref

O atributo **\[ propputref \]** especifica uma função de configuração de propriedade que usa uma referência em vez de um valor.

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
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

Uma função que tem o atributo **\[ propputref \]** também deve ter, como seu último parâmetro, um ponteiro que tem o **\[** atributo [**in**](in.md) **\]** .

A propriedade deve ter o mesmo nome que a função. No máximo, um dos **\[** atributos [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** e **\[ propputref \]** pode ser especificado para uma função.

### <a name="flags"></a>Flags

INVOCAr \_ PROPERTYPUTREF

## <a name="examples"></a>Exemplos

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 