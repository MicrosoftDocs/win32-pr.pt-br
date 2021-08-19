---
title: Elemento Binary (EventDataType)
description: Um blob de dados binário para eventos que são gravados usando o Log de Eventos.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- Elemento binário EventLog
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 495310a46a314b944b29eeb2433b7c5581136c6923c5630d8f09486a95e47fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120394"
---
# <a name="binary-eventdatatype-element"></a>Elemento Binary (EventDataType)

Um blob de dados binário para eventos gravados usando o [Log de Eventos](/windows/desktop/EventLog/event-logging).

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

O **elemento Binary** é definido pelo tipo complexo [**EventDataType.**](eventschema-eventdatatype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**EventData (EventType)**](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

