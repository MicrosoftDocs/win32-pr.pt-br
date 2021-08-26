---
title: Elemento Provider (SystemPropertiesType)
description: Identifica o provedor que registrou o evento.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- Elemento De provedor EventLog
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5327bc267272942df30044678a96244d957122c9fbf7878a805bfd48433e20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904516"
---
# <a name="provider-systempropertiestype-element"></a>Elemento Provider (SystemPropertiesType)

Identifica o provedor que registrou o evento.

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

O **elemento Provider** é definido pelo tipo complexo [**SystemPropertiesType.**](eventschema-systempropertiestype-complextype.md)

## <a name="attributes"></a>Atributos



| Nome            | Tipo                                                | Descrição                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Eventsourcename | string                                              | O nome da origem do evento que publicou o evento (se a origem do evento for da API herdada do Log [de](/windows/desktop/EventLog/event-logging) Eventos).<br/> |
| Guid            | [**GUIDType**](eventschema-guidtype-simpletype.md) | O identificador global exclusivo que identifica exclusivamente o provedor.<br/>                                                                   |
| Nome            | anyURI                                              | O nome do provedor de eventos que registrou o evento.<br/>                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

