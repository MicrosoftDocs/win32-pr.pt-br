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
ms.openlocfilehash: 6b6463644e1bd174be256d51b34ae2ae4ad9ce07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922537"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




