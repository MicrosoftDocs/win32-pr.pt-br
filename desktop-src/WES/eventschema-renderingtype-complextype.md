---
title: Tipo complexo RenderingInfoType
description: Define as mensagens renderizadas para o evento.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- Log de eventos do tipo complexo RenderingInfoType
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455838"
---
# <a name="renderinginfotype-complex-type"></a>Tipo complexo RenderingInfoType

Define as mensagens renderizadas para o evento.

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                             | Type   | Descrição                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [**Canal**](eventschema-task-renderingtype-element.md)           | string | A cadeia de caracteres de mensagem renderizada do canal especificado no evento.<br/> |
| [**Palavra-chave**](eventschema-keyword-keywords-element.md)             | string | A cadeia de caracteres de mensagem renderizada de uma palavra-chave especificada no evento.<br/>   |
| [**Palavras-chave**](eventschema-keywords-renderingtype-element.md)      |        | Uma lista de palavras-chave renderizadas.<br/>                                       |
| [**Geral**](eventschema-level-renderingtype-element.md)            | string | A cadeia de caracteres de mensagem renderizada do nível especificado no evento.<br/>   |
| [**Mensagem**](eventschema-message-renderingtype-element.md)        | string | A cadeia de caracteres de mensagem renderizada do evento.<br/>                          |
| [**Opcode**](eventschema-opcode-renderingtype-element.md)          | string | A cadeia de caracteres de mensagem renderizada do opcode especificado no evento.<br/>  |
| [**Provedor**](eventschema-publisher-renderinginfotype-element.md) | string | A cadeia de caracteres de mensagem renderizada para o provedor.<br/>                      |
| [**Tarefa**](eventschema-task-renderingtype-element.md)              | string | A cadeia de caracteres de mensagem renderizada da tarefa especificada no evento.<br/>    |



## <a name="attributes"></a>Atributos



| Nome    | Tipo     | Descrição                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| Cultura | Linguagem | O nome do idioma (por exemplo, en-US) que identifica a localidade usada para renderizar as cadeias de caracteres de mensagem.<br/> |



## <a name="remarks"></a>Comentários

Somente os eventos que foram coletados usando o serviço [coletor de eventos do Windows](/windows/desktop/WEC/windows-event-collector) conterão esta seção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

