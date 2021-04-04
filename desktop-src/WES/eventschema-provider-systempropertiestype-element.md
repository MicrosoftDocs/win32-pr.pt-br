---
title: Elemento Provider (SystemPropertiesType)
description: Identifica o provedor que registrou o evento.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- O elemento do provedor EventLog
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009021"
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

O elemento **Provider** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nome            | Tipo                                                | Descrição                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| EventSourcename | string                                              | O nome da origem do evento que publicou o evento (se a origem do evento for da API de [log de eventos](/windows/desktop/EventLog/event-logging) herdados).<br/> |
| Guid            | [**GUIDtype**](eventschema-guidtype-simpletype.md) | O identificador global exclusivo que identifica exclusivamente o provedor.<br/>                                                                   |
| Nome            | anyURI                                              | O nome do provedor de eventos que registrou o evento.<br/>                                                                                   |



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

 

