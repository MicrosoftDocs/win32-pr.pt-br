---
title: Elemento opcode (TaskEventDefinitionType)
description: Contém um opcode específico da tarefa para um evento. Todas as definições de opcode são consideradas específicas da tarefa que contém as definições de evento.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- EventLog do elemento opcode
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f3923e0a42375ac7d926d418943af81cc0264e111e6bdc4be56919780dfacf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652146"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>Elemento opcode (TaskEventDefinitionType)

\[a partir do compilador de mensagens fornecido com a versão Windows 7 do SDK do Windows, esse elemento não estará mais disponível.\]

Contém um opcode específico da tarefa para um evento. Todas as definições de opcode são consideradas específicas da tarefa que contém as definições de evento.

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

O elemento **opcode** é definido pelo tipo complexo [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                   | Type                                                                               | Descrição                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [**circunstância**](eventmanifestschema-event-opcode-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Um evento que é publicado com uma tarefa.<br/> |



## <a name="attributes"></a>Atributos



| Nome | Tipo      | Descrição                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | O nome do opcode específico da tarefa.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**tarefa (Definitiontype)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





