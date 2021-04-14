---
title: Tipo complexo do EventType
description: Define o nó raiz do esquema de evento.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- Log de eventos do tipo complexo do EventType
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369290"
---
# <a name="eventtype-complex-type"></a>Tipo complexo do EventType

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
| [**BinaryEventData**](eventschema-binaryeventdata-eventtype-element.md)         | hexBinary                                                                          | Contém os dados de evento como um blob binário. Os dados do evento são renderizados como um blob binário se a função de renderização não puder localizar os metadados usados para decodificar o evento.<br/>                                                                                                                                                            |
| [**DebugData**](eventschema-debugdata-eventtype-element.md)                     | [**DebugDataType**](eventschema-debugdatatype-complextype.md)                     | Contém os dados que podem ser registrados para eventos de pré-processamento (pré-processador de rastreamento de software) do Windows.<br/>                                                                                                                                                                                                                                    |
| [**EventData**](eventschema-eventdata-eventtype-element.md)                     | [**EventDataType**](eventschema-eventdatatype-complextype.md)                     | Contém os dados do evento. A ordem dos itens de dados no modelo determina o layout dos dados do evento.<br/>                                                                                                                                                                                                                 |
| [**ProcessingErrorData**](eventschema-processingerrordata-eventtype-element.md) | [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) | Contém detalhes do erro que ocorreu ao tentar renderizar o evento. Isso pode ocorrer se os dados do evento não corresponderem à definição de dados do evento no manifesto. Os dados do evento são incluídos como um blob binário.<br/>                                                                                                         |
| [**RenderingInfo**](eventschema-renderinginfo-eventtype-element.md)             | [**RenderingInfoType**](eventschema-renderingtype-complextype.md)                 | Contém as cadeias de caracteres de mensagem renderizadas para o evento (inclui a cadeia de mensagem do evento e as cadeias de mensagens para qualquer uma das propriedades do evento, como nível, tarefa e opcode). Somente os eventos que foram coletados usando o serviço [coletor de eventos do Windows](/windows/desktop/WEC/windows-event-collector) conterão esta seção.<br/> |
| [**Sistema**](eventschema-system-eventtype-element.md)                           | [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)       | Contém informações que identificam o provedor e como ele foi habilitado, o evento, o canal no qual o evento foi gravado e informações do sistema, como as IDs de processo e thread.<br/>                                                                                                                                   |
| [**UserData**](eventschema-userdata-eventtype-element.md)                       | [**UserDataType**](eventschema-userdatatype-complextype.md)                       | Contém os dados do evento. A seção de dados do usuário do modelo determina o layout dos dados do evento.<br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a>Comentários

Normalmente, esta seção conterá com a seção **EVENTDATA** ou **UserData** . A seção **EVENTDATA** será usada se o modelo não contiver uma seção **UserData** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

