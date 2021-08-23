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
ms.openlocfilehash: 81a48c21e34edecbf4dfb4f9c2e87c85a77e3f500ec42b8607f1de004e7679ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511306"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





