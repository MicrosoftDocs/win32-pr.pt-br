---
title: Tipo simples de UInt8Type
description: Define um tipo de byte não assinado.
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- Log de eventos de tipo simples UInt8Type
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3236d7416cbb199037813a8ae870d4f87718081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770540"
---
# <a name="uint8type-simple-type"></a>Tipo simples de UInt8Type

Define um tipo de byte não assinado. O valor pode ser especificado como um inteiro de 1 byte ou um valor hexadecimal no intervalo de 0 a 255.

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





