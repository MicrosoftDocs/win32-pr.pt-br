---
title: atributo helpcontext
description: O atributo \ HelpContext \ especifica um identificador de contexto que permite ao usuário exibir informações sobre esse elemento no arquivo de ajuda.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- atributo HelpContext MIDL
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3caa5dd32257fb5d75bbf77cde4ae5e71c6e97574cd1c263ead47aacedccadc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895246"
---
# <a name="helpcontext-attribute"></a>atributo helpcontext

O \[  \] atributo HelpContext especifica um identificador de contexto que permite ao usuário exibir informações sobre esse elemento no arquivo de ajuda.

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a [**biblioteca**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**módulo**](module.md), [**typedef**](typedef.md), **métodos**, **\[ propriedade \]** ou [**coclass**](coclass.md).

</dd> <dt>

*HelpContext-Value* 
</dt> <dd>

Um inteiro exclusivo que identifica o texto de ajuda associado ao elemento MIDL atual.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica uma lista de um ou mais atributos que se aplicam ao elemento MIDL como um todo.

</dd> <dt>

*elementos* 
</dt> <dd>

Uma das seguintes diretivas: [**library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).

</dd> <dt>

*nome do elemento* 
</dt> <dd>

O nome que outros componentes de software podem usar para delinear o elemento atual.

</dd> <dt>

*definições* 
</dt> <dd>

Especifica as instruções que compõem a definição do elemento.

</dd> </dl>

## <a name="remarks"></a>Comentários

O \[ **atributo HelpContext** \] pode ser aplicado aos seguintes elementos: [**library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).

O *HelpContext-Value* é um identificador de contexto de 32 bits dentro do arquivo de ajuda que pode ser recuperado com as funções [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) nas interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) e [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) .

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[**modulo**](module.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 