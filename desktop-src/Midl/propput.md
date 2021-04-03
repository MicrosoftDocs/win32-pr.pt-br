---
title: atributo propput
description: O atributo \ propput \ especifica uma função de configuração de propriedade. A propriedade deve ter o mesmo nome que a função.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- propput do atributo MIDL
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084474"
---
# <a name="propput-attribute"></a>atributo propput

O atributo **\[ propput \]** especifica uma função de configuração de propriedade. A propriedade deve ter o mesmo nome que a função *.*

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
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

Uma função que tem o atributo **\[ propput \]** também deve ter, como seu último parâmetro, um parâmetro que tem o **\[** atributo [**in**](in.md) **\]** .

No máximo, um de **\[** [**propget**](propget.md) **\]** , **\[ propput \]** e **\[** [**propputref**](propputref.md) **\]** podem ser especificados para uma função.

Se o **\[** atributo [**LCID**](lcid.md) **\]** for usado na lista de parâmetros de uma função que contém um parâmetro com o atributo **\[ propput \]** , o parâmetro **\[ LCID \]** deverá ser segundo para o último.

### <a name="flags"></a>Flags

INVOCAr \_ PROPERTYPUT

## <a name="examples"></a>Exemplos

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Diferenças entre MIDL e MKTYPLIB](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 