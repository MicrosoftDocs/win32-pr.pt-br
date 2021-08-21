---
title: Tipo complexo EventType
description: Define o nó raiz do esquema de evento.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- Tipo complexo EventType EventLog
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: da5948021c4a2db50776544c38adfa4ddc6e8ce5bcc1285c879ef528dec759e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957896"
---
# <a name="eventtype-complex-type"></a>Tipo complexo EventType

Define o nó raiz do esquema de evento.

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
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



| Elemento                                                                          | Type                                                                               | Descrição                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BinaryEventData**](eventschema-binaryeventdata-eventtype-element.md)         | Hexbinary                                                                          | Contém os dados de evento como um blob binário. Os dados do evento serão renderizados como um blob binário se a função de renderização não puder encontrar os metadados usados para decodificar o evento.<br/>                                                                                                                                                            |
| [**DebugData**](eventschema-debugdata-eventtype-element.md)                     | [**DebugDataType**](eventschema-debugdatatype-complextype.md)                     | Contém os dados que podem ser registrados em Windows de pré-processador de rastreamento de software (WPP).<br/>                                                                                                                                                                                                                                    |
| [**Eventdata**](eventschema-eventdata-eventtype-element.md)                     | [**EventDataType**](eventschema-eventdatatype-complextype.md)                     | Contém os dados do evento. A ordem dos itens de dados no modelo determina o layout dos dados do evento.<br/>                                                                                                                                                                                                                 |
| [**ProcessingErrorData**](eventschema-processingerrordata-eventtype-element.md) | [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) | Contém detalhes do erro que ocorreu ao tentar renderizar o evento. Isso poderá ocorrer se os dados do evento não corresponderem à definição de dados de evento no manifesto. Os dados do evento são incluídos como um blob binário.<br/>                                                                                                         |
| [**RenderingInfo**](eventschema-renderinginfo-eventtype-element.md)             | [**RenderingInfoType**](eventschema-renderingtype-complextype.md)                 | Contém as cadeias de caracteres de mensagem renderizadas para o evento (inclui a cadeia de caracteres de mensagem do evento e as cadeias de caracteres de mensagem para qualquer uma das propriedades do evento, como level, task e opcode). Somente os eventos que foram coletados usando o [Windows coletor de](/windows/desktop/WEC/windows-event-collector) eventos conterão esta seção.<br/> |
| [**Sistema**](eventschema-system-eventtype-element.md)                           | [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)       | Contém informações que identificam o provedor e como ele foi habilitado, o evento, o canal no qual o evento foi gravado e informações do sistema, como o processo e as IDs de thread.<br/>                                                                                                                                   |
| [**UserData**](eventschema-userdata-eventtype-element.md)                       | [**UserDataType**](eventschema-userdatatype-complextype.md)                       | Contém os dados do evento. A seção de dados do usuário do modelo determina o layout dos dados do evento.<br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a>Comentários

Normalmente, esta seção conterá com a **seção EventData** ou **UserData.** A **seção EventData** será usada se o modelo não tiver uma **seção UserData.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

