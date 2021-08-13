---
title: atributo de controle
description: O atributo \ Control \ identifica uma coclass ou biblioteca como um controle COM, do qual um site de contêiner derivará bibliotecas de tipos adicionais ou classes de objeto de componente.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- atributo de controle MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6372ffb7f7d9f19769e419b12c0b109736a9867360224e023f1b622c653854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643675"
---
# <a name="control-attribute"></a>atributo de controle

O atributo **\[ Control \]** identifica uma [**coclass**](coclass.md) ou [**biblioteca**](library.md) como um controle com, da qual um site de contêiner derivará bibliotecas de tipo adicionais ou classes de objeto de componente.

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à [**biblioteca**](library.md) ou à instrução [**coclass**](coclass.md) . Separe vários atributos com vírgulas.

</dd> <dt>

*lib-ou-Coclassname* 
</dt> <dd>

Especifica o nome da [**biblioteca**](library.md) ou [**coclass**](coclass.md).

</dd> <dt>

*definições* 
</dt> <dd>

Instruções MIDL que especificam os membros da [**biblioteca**](library.md) ou [**coclass**](coclass.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse atributo permite marcar bibliotecas de tipos que descrevem controles para que não sejam exibidas em navegadores de tipos destinados a objetos não visuais.

### <a name="flags"></a>Flags

TYPEFLAG \_ FCONTROL, LIBFLAG \_ FCONTROL

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**biblioteca**](library.md)
</dt> </dl>

 

 