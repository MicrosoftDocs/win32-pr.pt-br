---
title: atributo helpstringcontext
description: O atributo \ helpstringcontext \ especifica um identificador de contexto de ajuda de 32 bits no arquivo de ajuda. Você pode aplicar o atributo \ helpstringcontextname a biblioteca, interface, dispinterface, módulo, coclasse, Instruções typedef, propriedades, parâmetros e métodos.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- helpstringcontext do atributo MIDL
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64e97ea0d7b41d87ef1d535d562f3b515dda4f59a67f6d5e35f97bed8b1f9ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807231"
---
# <a name="helpstringcontext-attribute"></a>atributo helpstringcontext

O atributo **\[ helpstringcontext \]** especifica um identificador de contexto de ajuda de 32 bits no arquivo de ajuda. Você pode aplicar o atributo **\[ \] helpstringcontext** a [**biblioteca**](library.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**módulo**](module.md), [**coclass**](coclass.md), instruções [**typedef**](typedef.md) , propriedades, parâmetros e métodos.

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ContextId* 
</dt> <dd>

Um inteiro exclusivo que identifica o texto de ajuda associado à instrução MIDL atual.

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Zero ou mais atributos MIDL.

</dd> <dt>

*instrução IDL* 
</dt> <dd>

A instrução MIDL à qual o atributo **\[ helpstringcontext \]** será aplicado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use as funções **GetDocumentation2** nas interfaces **ITypeLib2** e **ITypeInfo2** para recuperar a cadeia de caracteres de ajuda.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




