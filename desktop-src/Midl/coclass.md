---
title: atributo coclass
description: A instrução coclass fornece uma listagem das interfaces com suporte para um objeto de componente.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- atributo de coclasse MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbd64ed5565797444b58ea71c0b7daf6c083c4810b0876a8b990a7dd281a84c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807302"
---
# <a name="coclass-attribute"></a>atributo coclass

A **instrução coclass** fornece uma listagem das interfaces com suporte para um objeto de componente.

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*coclass-attribute-list* 
</dt> <dd>

O **\[** [**atributo uuid**](uuid.md) **\]** é necessário em uma **coclasse**. Esse é o mesmo **\[ uuid registrado \]** como um CLSID no banco de dados de registro do sistema. Os **\[** [**atributos helpstring**](helpstring.md), helpcontext , licenciado, versão , controle , oculto e appobject são aceitos, mas não necessários, antes de uma **\]** **\[** [](helpcontext.md) **\]** **\[** [](licensed.md) **\]** **\[** [](version.md) **\]** **\[** [](control.md) **\]** **\[** [](hidden.md) **\]** **\[** [](appobject.md) **\]** **definição de coclasse.**

</dd> <dt>

*Classname* 
</dt> <dd>

Nome pelo qual o objeto comum é conhecido na biblioteca de tipos.

</dd> <dt>

*interface-attributes* 
</dt> <dd>

Atributos opcionais para a interface ou dispinterface. Os atributos de origem , padrão e restritos são **\[** [](source.md) **\]** **\[** [](default.md) **\]** **\[** [](restricted.md) **\]** aceitos em uma interface ou dispinterface dentro de uma **coclasse**.

</dd> <dt>

*Interfacename* 
</dt> <dd>

Uma interface declarada com a palavra-chave [**interface**](interface.md) ou uma dispinterface declarada com a [**palavra-chave dispinterface.**](dispinterface.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

O Microsoft Component Object Model define uma classe como uma implementação que permite **QueryInterface** entre um conjunto de interfaces.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**appobject**](appobject.md)
</dt> <dt>

[**Controle**](control.md)
</dt> <dt>

[**Padrão**](default.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**Escondidos**](hidden.md)
</dt> <dt>

[**Interface**](interface.md)
</dt> <dt>

[**licensed**](licensed.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Restrito**](restricted.md)
</dt> <dt>

[**Fonte**](source.md)
</dt> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 