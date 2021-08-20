---
description: Especifica os parâmetros necessários para configurar uma conexão de dados.
ms.assetid: 7a3d3b9d-f799-4927-9c18-04b025788a4a
title: Elemento Context (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Context
api_type:
- Schema
ms.openlocfilehash: 6d5e5d6db0a2d2c2e207a61a7d20d9a084416954b54c98f6429e3916b526e663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066140"
---
# <a name="context-mbnprofile-element"></a>Elemento Context (MBNProfile)

O **elemento Context (MBNProfile)** especifica os parâmetros necessários para configurar uma conexão de dados.

O elemento pode ter os seguintes elementos filho.

-   [**AccessString**](schema-accessstring-contexttype-element.md)
-   [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
-   [**Compactação**](schema-compression-contexttype-element.md)
-   [**AuthProtocol**](schema-authprotocol-contexttype-element.md)

Esse elemento pode ter um máximo de uma ocorrência.

``` syntax
<xs:element name="Context"
    type="contextType"
 />
```

O **elemento** Context é definido pelo [**elemento MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




