---
title: Tipo simples de UInt16type
description: Define um tipo curto sem sinal.
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- Log de eventos de tipo simples UInt16type
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e687f42a43a12266267a0531ce078e8c6b5d1031
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645082"
---
# <a name="uint16type-simple-type"></a>Tipo simples de UInt16type

Define um tipo curto sem sinal. O valor pode ser especificado como um inteiro de 2 bytes ou um valor hexadecimal no intervalo de 0 a 65.535.

``` syntax
<xs:simpleType name="UInt16Type">
    <xs:union
        memberValues="unsignedShort HexInt16Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





