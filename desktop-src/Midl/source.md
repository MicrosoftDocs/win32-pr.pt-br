---
title: atributo source
description: O atributo \ Source \ indica que um membro de uma coclass, propriedade ou método é uma fonte de eventos. Para um membro de uma coclass, esse atributo significa que o membro é chamado em vez de implementado.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- atributo de origem MIDL
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917179"
---
# <a name="source-attribute"></a>atributo source

O atributo **\[ Source \]** indica que um membro de uma [**coclass**](coclass.md), Property ou Method é uma fonte de eventos. Para um membro de uma **coclass**, esse atributo significa que o membro é chamado em vez de implementado.

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*coclass-atributos* 
</dt> <dd>

Zero ou mais atributos que serão aplicados à [**coclass**](coclass.md).

</dd> <dt>

*coclass-Name* 
</dt> <dd>

O identificador de nome da [**coclass**](coclass.md).

</dd> <dt>

*opcional-atributos* 
</dt> <dd>

Zero ou mais atributos MIDL.

</dd> <dt>

*tipo de instrução* 
</dt> <dd>

Pode ser [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).

</dd> <dt>

*nome da instrução* 
</dt> <dd>

O nome da [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).

</dd> <dt>

*tipo de objeto* 
</dt> <dd>

O tipo do objeto que o método retorna. Esse objeto é uma fonte de eventos.

</dd> <dt>

*nome da função* 
</dt> <dd>

O nome de um método em uma [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).

</dd> <dt>

*opcional-lista de parâmetros* 
</dt> <dd>

Zero ou mais parâmetros de método.

</dd> </dl>

## <a name="remarks"></a>Comentários

Em uma propriedade ou método, o atributo de **\[ origem \]** indica que o membro retorna um objeto ou uma variante que é uma fonte de eventos. O objeto implementa **IConnectionPointContainer**.

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FSOURCE, VARFLAG \_ Source, FUNCFLAG \_ Source

## <a name="examples"></a>Exemplos

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 