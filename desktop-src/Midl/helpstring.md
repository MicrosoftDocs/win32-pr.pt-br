---
title: atributo HelpString
description: O atributo \ HelpString \ especifica uma cadeia de caracteres que é usada para descrever o elemento ao qual se aplica.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- atributo HelpString MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abb433d7112bc4c3257345d086ccf308cc1892b61a99991b485ce4962b5851e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013864"
---
# <a name="helpstring-attribute"></a>atributo HelpString

O atributo **\[ HelpString \]** especifica uma cadeia de caracteres que é usada para descrever o elemento ao qual se aplica. Você pode aplicar o atributo **\[ HelpString \]** às instruções library, importlib, interface, dispinterface, module ou coclass, TYPEDEFs, propriedades e métodos.

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ajuda-texto-cadeia de caracteres* 
</dt> <dd>

Uma cadeia de caracteres com terminação zero contendo texto de ajuda.

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Zero ou mais instruções de atributo MIDL.

</dd> <dt>

*elementos* 
</dt> <dd>

Uma das seguintes diretivas: [**library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).

</dd> <dt>

*nome do elemento* 
</dt> <dd>

O nome que outros componentes de software podem usar para delinear o elemento atual

</dd> <dt>

*defini* 
</dt> <dd>

Especifica as instruções que compõem a definição do elemento.

</dd> <dt>

*instrução IDL* 
</dt> <dd>

Uma instrução de definição de interface MIDL, como [**propget**](propget.md) ou [**propput**](propput.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Use as funções [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) nas interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) e [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) para recuperar a cadeia de caracteres de ajuda.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**modulo**](module.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 