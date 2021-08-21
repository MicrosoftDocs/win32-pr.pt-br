---
title: Tipo simples HexInt64Type (esquema de evento)
description: Define um tipo hexadecimal de 8 byte. | Tipo simples HexInt64Type (esquema de evento)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
keywords:
- Tipo simples HexInt64Type EventLog
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fcc4e3cea12be0fecaf7cef2dcd6f9687f4aa4340f9eaca4f8a6bad10c88eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120141"
---
# <a name="hexint64type-simple-type-event-schema"></a>Tipo simples HexInt64Type (esquema de evento)

Define um tipo hexadecimal de 8 byte.

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O **tipo simples HexInt64Type** é **uma** cadeia de caracteres restrita pelo seguinte padrão:

-   `0[xX][0-9A-Fa-f]{1,16}`

    O valor pode conter de um a 16 caracteres hexadecimais (por exemplo, 0xa ou 0xac7bd361004fe190).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





