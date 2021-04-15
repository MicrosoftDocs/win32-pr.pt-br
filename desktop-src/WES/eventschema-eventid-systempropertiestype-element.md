---
title: Elemento EventID (SystemPropertiesType)
description: O identificador que o provedor usou para identificar o evento.
ms.assetid: 2d5ac44b-4157-4b87-bd8f-e992e85dd0b1
keywords:
- EventLog do elemento EventID
topic_type:
- apiref
api_name:
- EventID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac1b2edd671f06d88c8c51b49c16f759fd05e087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454773"
---
# <a name="eventid-systempropertiestype-element"></a>Elemento EventID (SystemPropertiesType)

O identificador que o provedor usou para identificar o evento.

``` syntax
<xs:element name="EventID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedInt"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

O elemento **EventID** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**Sistema (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





