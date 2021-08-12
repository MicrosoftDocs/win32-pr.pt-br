---
title: Tipo complexo DefinitionType
description: Define uma lista de eventos que seu provedor pode registrar.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- Tipo complexo DefinitionType EventLog
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f62ab040f57fdeb4e4208554c642e9b0bc2fb1135512d1c512f0b0ef90b69e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589631"
---
# <a name="definitiontype-complex-type"></a>Tipo complexo DefinitionType

Define uma lista de eventos que seu provedor pode registrar.

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                           | Type                                                                                       | Descrição                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Evento**](eventmanifestschema-event-definitiontype-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)         | Define um evento que seu provedor pode registrar em log.<br/>                                                                                                                                                                                                                                 |
| [**Tarefa**](eventmanifestschema-task-definitiontype-element.md)   | [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) | Sem suporte.<br/> **Windows Server 2008 e Windows Vista:** Define um evento específico de tarefa que seu provedor pode registrar em log. (A partir do compilador de mensagens que acompanha a versão Windows 7 do SDK do Windows, não há mais suporte para eventos específicos da tarefa.)<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





