---
title: Tipo simples de HexInt64Type (esquema de evento)
description: Define um tipo hexadecimal de 8 bytes. | Tipo simples de HexInt64Type (esquema de evento)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
keywords:
- Log de eventos de tipo simples HexInt64Type
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e290c2326415664fbbae3feed9628b86452b10c6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105783653"
---
# <a name="hexint64type-simple-type-event-schema"></a>Tipo simples de HexInt64Type (esquema de evento)

Define um tipo hexadecimal de 8 bytes.

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

O tipo simples **HexInt64Type** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:

-   `0[xX][0-9A-Fa-f]{1,16}`

    O valor pode conter de um a dezesseis caracteres hexadecimais (por exemplo, 0xA ou 0xac7bd361004fe190).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





