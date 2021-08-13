---
title: atributo propputref
description: O atributo \ propputref\ especifica uma função de configuração de propriedade que usa uma referência em vez de um valor .
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- atributo propputref MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e80b0baa4f78537142043b374c206ade0f3d51d7ca30c2f57e1c4ae4e9b695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641959"
---
# <a name="propputref-attribute"></a>atributo propputref

O **\[ atributo \] propputref** especifica uma função de configuração de propriedade que usa uma referência em vez de um valor.

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*optional-property-attributes* 
</dt> <dd>

Zero ou mais atributos de propriedade.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

O tipo dos dados retornados pelo procedimento remoto.

</dd> <dt>

*Nome da função* 
</dt> <dd>

O nome do procedimento remoto.

</dd> <dt>

*parameters* 
</dt> <dd>

Zero ou mais parâmetros para o procedimento remoto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma função que tem o **\[ atributo propputref \]** também deve ter, como seu último parâmetro, um ponteiro que tenha o **\[** [**no**](in.md) atributo **\]** .

A propriedade deve ter o mesmo nome que a função. No máximo, um dos **\[** [**atributos propget**](propget.md), propput e **\]** **\[** [](propput.md) **\]** **\[ propputref \]** pode ser especificado para uma função.

### <a name="flags"></a>Flags

INVOKE \_ PROPERTYPUTREF

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

[**Em**](in.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 