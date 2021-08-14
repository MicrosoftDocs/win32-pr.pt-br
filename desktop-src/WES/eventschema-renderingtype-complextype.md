---
title: Tipo complexo RenderingInfoType
description: Define as mensagens renderizadas para o evento.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- Tipo complexo RenderingInfoType EventLog
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d4a70c8bc97abc3dea7cd04e9ce491b64cb62dcc892fcde318d69dcdc996e2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588459"
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
| [**Keywords**](eventschema-keywords-renderingtype-element.md)      |        | Uma lista de palavras-chave renderizadas.<br/>                                       |
| [**Nível**](eventschema-level-renderingtype-element.md)            | string | A cadeia de caracteres de mensagem renderizada do nível especificado no evento.<br/>   |
| [**Mensagem**](eventschema-message-renderingtype-element.md)        | string | A cadeia de caracteres de mensagem renderizada do evento.<br/>                          |
| [**Opcode**](eventschema-opcode-renderingtype-element.md)          | string | A cadeia de caracteres de mensagem renderizada do opcode especificado no evento.<br/>  |
| [**Provedor**](eventschema-publisher-renderinginfotype-element.md) | string | A cadeia de caracteres de mensagem renderizada para o provedor.<br/>                      |
| [**Tarefa**](eventschema-task-renderingtype-element.md)              | string | A cadeia de caracteres de mensagem renderizada da tarefa especificada no evento.<br/>    |



## <a name="attributes"></a>Atributos



| Nome    | Tipo     | Descrição                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| Cultura | Linguagem | O nome do idioma (por exemplo, en-US) que identifica a localidade usada para renderizar as cadeias de caracteres de mensagem.<br/> |



## <a name="remarks"></a>Comentários

Somente os eventos que foram coletados usando o serviço [Windows Coletor de](/windows/desktop/WEC/windows-event-collector) Eventos conterão esta seção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

