---
title: Tipo complexo InstrumentationType
description: Define o conteúdo da seção de instrumentação do manifesto.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Log de eventos do tipo complexo InstrumentationType
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1679ae310a996458aad3e25aba74955036094e00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811375"
---
# <a name="instrumentationtype-complex-type"></a>Tipo complexo InstrumentationType

Define o conteúdo da seção de instrumentação do manifesto.

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                  | Type                                                             | Descrição                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**LostFocus**](eventmanifestschema-events-instrumentationtype-element.md) | [**EventType**](eventmanifestschema-eventstype-complextype.md) | Contém uma lista de provedores que o manifesto define.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





