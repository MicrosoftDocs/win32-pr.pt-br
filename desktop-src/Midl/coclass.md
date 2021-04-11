---
title: atributo coclass
description: A instrução coclass fornece uma lista das interfaces com suporte para um objeto de componente.
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
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365949"
---
# <a name="coclass-attribute"></a>atributo coclass

A instrução **coclass** fornece uma lista das interfaces com suporte para um objeto de componente.

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

*Categoria-atributo-lista* 
</dt> <dd>

O **\[** atributo [**UUID**](uuid.md) **\]** é necessário em uma **coclass**. Esse é o mesmo **\[ UUID \]** registrado como um CLSID no banco de dados de registro do sistema. Os **\[** atributos [**HelpString**](helpstring.md) **\]** , **\[** [**IdentificaçãoDoContextoDaAjuda**](helpcontext.md) **\]** , **\[** [**licenciado**](licensed.md) **\]** , **\[** [**versão**](version.md) **\]** , **\[** [**controle**](control.md) **\]** , **\[** [**oculto**](hidden.md) **\]** e **\[** [**appobject**](appobject.md) **\]** são aceitos, mas não obrigatórios, antes de uma definição de **coclasse** .

</dd> <dt>

*ClassName* 
</dt> <dd>

Nome pelo qual o objeto comum é conhecido na biblioteca de tipos.

</dd> <dt>

*atributos de interface* 
</dt> <dd>

Atributos opcionais para a interface ou Dispinterface. Os **\[** atributos de [**origem**](source.md) **\]** , **\[** [**padrão**](default.md) **\]** e **\[** [**restritos**](restricted.md) **\]** são aceitos em uma interface ou dispinterface dentro de uma **coclass**.

</dd> <dt>

*InterfaceName* 
</dt> <dd>

Uma interface declarada com a palavra-chave [**interface**](interface.md) ou uma dispinterface declarada com a palavra-chave [**dispinterface**](dispinterface.md) .

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

[**controlo**](control.md)
</dt> <dt>

[**os**](default.md)
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

[**oculto**](hidden.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**licensed**](licensed.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Restricted**](restricted.md)
</dt> <dt>

[**original**](source.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**personalizado**](uuid.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 