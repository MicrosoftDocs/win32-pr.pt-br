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
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810608"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>Elemento opcode (TaskEventDefinitionType)

\[A partir do compilador de mensagens fornecido com a versão do Windows 7 do SDK do Windows, esse elemento não estará mais disponível.\]

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**tarefa (Definitiontype)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





