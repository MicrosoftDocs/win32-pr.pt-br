---
title: atributo appobject
description: O atributo \ appobject \ identifica a coclass como um objeto de aplicativo, que está associado a um aplicativo EXE completo.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- appobject do atributo MIDL
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54cbe8d5c1c7a573216ae9cb55075ba3b3766d0d8c7898233be9364488131e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808328"
---
# <a name="appobject-attribute"></a>atributo appobject

O atributo **\[ appobject \]** identifica a [**coclass**](coclass.md) como um objeto Application, que está associado a um aplicativo exe completo.

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a [**coclass**](coclass.md).

</dd> <dt>

*Categoria-atributo-lista* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à instrução [**coclass**](coclass.md) . Os atributos **de coclasse** permitidos são [**\[ \] HelpString**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ licenciado \]**](licensed.md), [**\[ version \]**](version.md), [**\[ Control \]**](control.md)e [**\[ Hidden \]**](hidden.md).

</dd> <dt>

*ClassName* 
</dt> <dd>

Especifica o nome pelo qual o objeto de componente é conhecido na biblioteca de tipos.

</dd> <dt>

*definição de coclasse* 
</dt> <dd>

Especifica as instruções que compõem a definição da [**coclasse**](coclass.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ appobject \]** também indica que as funções e as propriedades da [**coclass**](coclass.md) estão disponíveis globalmente na biblioteca de tipos atual.

A representação TYPEFLAG para esse atributo é TYPEFLAG \_ FAPPOBJECT

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**controlo**](control.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**oculto**](hidden.md)
</dt> <dt>

[**licensed**](licensed.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 