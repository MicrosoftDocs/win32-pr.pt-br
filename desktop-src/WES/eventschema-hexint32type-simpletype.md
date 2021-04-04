---
title: Tipo simples de HexInt32Type (esquema de evento)
description: Define um tipo hexadecimal de 4 bytes. | Tipo simples de HexInt32Type (esquema de evento)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
keywords:
- Log de eventos de tipo simples HexInt32Type
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c9bd7a11d0e648cc451ec837f0f8711ca334d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930364"
---
# <a name="hexint32type-simple-type-event-schema"></a>Tipo simples de HexInt32Type (esquema de evento)

Define um tipo hexadecimal de 4 bytes.

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O tipo simples **HexInt32Type** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:

-   `0[xX][0-9A-Fa-f]{1,8}`

    O valor pode conter de um a oito caracteres hexadecimais (por exemplo, 0xA ou 0xac7bd361).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





