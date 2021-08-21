---
description: Define um tipo de cadeia de caracteres para SSIDs (identificadores de conjunto de serviços).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: Tipo simples de networkNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8f653c84f36730ed9f6f078b3713dde414fbf63469bd4ea43f632842d33d7e14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064746"
---
# <a name="networknametype-simple-type"></a>Tipo simples de networkNameType

O tipo simples networkNameType define um tipo de cadeia de caracteres para SSIDs (identificadores de conjunto de serviços). Um SSID é uma cadeia de caracteres que tem pelo menos um caractere e, no máximo, 32 caracteres de comprimento.

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 




