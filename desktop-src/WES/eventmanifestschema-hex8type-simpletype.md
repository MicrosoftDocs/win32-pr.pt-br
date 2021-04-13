---
title: Tipo simples de HexInt8Type
description: Define um tipo hexadecimal de 1 byte.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- Log de eventos de tipo simples HexInt8Type
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455975"
---
# <a name="hexint8type-simple-type"></a>Tipo simples de HexInt8Type

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

O tipo simples **HexInt8Type** é uma [cadeia de caracteres](/dotnet/api/system.string) que é restrita pelo seguinte padrão:

-   `0[xX][0-9A-Fa-f]{1,2}`

    O valor pode conter de um a dois caracteres hexadecimais (por exemplo, 0xA ou 0xAC).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

