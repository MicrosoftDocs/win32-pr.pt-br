---
description: Define um tipo hexadecimal de 4 bytes.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: Tipo simples de HexInt32Type (contadores de desempenho)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766839"
---
# <a name="hexint32type-simple-type-performance-counters"></a>Tipo simples de HexInt32Type (contadores de desempenho)

Define um tipo hexadecimal de 4 bytes.

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O tipo simples **HexInt32Type** é um **xs: String** que é restrito pelo seguinte padrão:

-   `0[xX][0-9A-Fa-f]{1,8}`

    O valor pode conter de um a oito caracteres hexadecimais (por exemplo, 0xA ou 0xac7bd361).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




