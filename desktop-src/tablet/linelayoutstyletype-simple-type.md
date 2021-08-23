---
description: Define os valores válidos para o atributo Style do elemento LineLayout.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Tipo simples LineLayoutStyleType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2aa0a42ca2f295cdcccad05931ba651d4018ba377d8d10f09f85b82dcaaea8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031834"
---
# <a name="linelayoutstyletype-simple-type"></a>Tipo simples LineLayoutStyleType

Define os valores válidos para o **atributo Style** do [elemento LineLayout](linelayout-element.md).

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O **tipo simples LineLayoutStyleType** é uma cadeia de caracteres restrita pelo seguinte padrão:

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a>Comentários

Os valores válidos **para o** atributo Style do [elemento LineLayout](linelayout-element.md) são:

-   Nenhum
-   Sólido
-   Traço
-   Ponto
-   DashDot
-   DashDotDot
-   Double

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                     |



 

 




