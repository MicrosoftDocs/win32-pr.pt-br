---
title: atributo licenciado
description: O atributo \ licenciado \ indica que a coclass à qual ele se aplica é licenciado e deve ser instanciada usando IClassFactory2.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- atributo licenciado MIDL
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007417"
---
# <a name="licensed-attribute"></a>atributo licenciado

O atributo **\[ licenciado \]** indica que a [**coclass**](coclass.md) à qual ela se aplica é licenciada e deve ser instanciada usando [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à instrução [**coclass**](coclass.md) . Os atributos de **coclasse** permitidos são **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[ licenciado \]**, **\[** [**version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** e **\[** [**Hidden**](hidden.md) **\]** .

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

O licenciamento é um recurso do COM que fornece controle sobre a criação de objetos. Os objetos licenciados podem ser criados somente por clientes que estão autorizados a usá-los. O licenciamento é implementado em COM por meio da interface [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) e por suporte para uma chave de licença que pode ser passada em tempo de execução.

### <a name="flags"></a>Flags

TYPEFLAG \_ FLICENSED

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Conteúdo de uma biblioteca de tipos](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
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

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 