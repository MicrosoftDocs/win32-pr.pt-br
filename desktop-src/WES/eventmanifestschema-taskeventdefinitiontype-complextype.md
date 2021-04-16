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
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105794543"
---
# <a name="taskeventdefinitiontype-complex-type"></a>Tipo complexo TaskEventDefinitionType

\[Começando com o compilador de mensagem que acompanha a versão do Windows 7 do SDK do Windows, o tipo complexo TaskEventDefinitionType não está mais disponível. Em vez disso, use opcodes específicos da tarefa para fornecer a mesma funcionalidade.\]

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



| Elemento                                                                      | Type                                                                               | Description                                             |
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





