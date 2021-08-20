---
title: Tipo simples HexInt8Type
description: Define um tipo hexadecimal de 1 byte.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- Tipo simples HexInt8Type EventLog
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d2d70b7258317f16ac4e134f011a85218fa1b63aa768136f68b1d21c901856e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121002"
---
# <a name="hexint8type-simple-type"></a>Tipo simples HexInt8Type

Define um tipo hexadecimal de 1 byte.

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O **tipo simples HexInt8Type** é [uma](/dotnet/api/system.string) cadeia de caracteres restrita pelo seguinte padrão:

-   `0[xX][0-9A-Fa-f]{1,2}`

    O valor pode conter de um a dois caracteres hexadecimais (por exemplo, 0xa ou 0xac).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

