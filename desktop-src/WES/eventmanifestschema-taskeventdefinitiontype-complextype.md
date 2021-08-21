---
title: Tipo complexo TaskEventDefinitionType
description: Define um evento específico de tarefa que seu provedor pode registrar. | Tipo complexo TaskEventDefinitionType
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- Log de eventos do tipo complexo TaskEventDefinitionType
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44a4fc7ca8784b3472fea3b0d4f4e657ce615fae05a8cc7372aa3cca0fedb431
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055834"
---
# <a name="taskeventdefinitiontype-complex-type"></a>Tipo complexo TaskEventDefinitionType

\[começando com o compilador de mensagem fornecido com a versão Windows 7 do SDK do Windows, o tipo complexo TaskEventDefinitionType não está mais disponível. Em vez disso, use opcodes específicos da tarefa para fornecer a mesma funcionalidade.\]

Define um evento específico de tarefa que seu provedor pode registrar.

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                      | Type                                                                               | Descrição                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| **event**                                                                    | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Um evento específico da tarefa publicado com uma tarefa.<br/> |
| [**opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | Um opcode específico da tarefa que para um evento. <br/>   |



## <a name="attributes"></a>Atributos



| Nome | Tipo      | Descrição                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | O nome do opcode específico da tarefa.<br/> |
| name | anyURI    | O nome da tarefa.<br/>                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





