---
title: Tipo simples de HexInt64Type
description: Define um tipo hexadecimal de 8 bytes. | Tipo simples de HexInt64Type
ms.assetid: 2e81ec2b-cf67-42df-92a0-bf45b6dca051
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
ms.openlocfilehash: 8947e594bb067140510b0b5d2046a898018a291e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104370861"
---
# <a name="hexint64type-simple-type"></a>Tipo simples de HexInt64Type

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

O tipo simples **HexInt64Type** é uma [cadeia de caracteres](/dotnet/api/system.string) que é restrita pelo seguinte padrão:

-   `0[xX][0-9A-Fa-f]{1,16}`

    O valor pode conter de um a dezesseis caracteres hexadecimais (por exemplo, 0xA ou 0xac7bd361004fe190).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

