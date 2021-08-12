---
title: Tipo complexo EventDataType
description: Define os itens de dados do evento e as estruturas que contêm os dados do evento.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- Log de eventos do tipo complexo EventDataType
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 424f7f5f6472859a06605467c427fc7b9f210a960f0920fb8593778bd757fc06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589019"
---
# <a name="eventdatatype-complex-type"></a>Tipo complexo EventDataType

Define os itens de dados do evento e as estruturas que contêm os dados do evento.

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                              | Type                                                               | Descrição                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Binário**](eventschema-binary-eventdatatype-element.md)           | hexBinary                                                          | Um blob de dados binários para eventos que são gravados usando o [log de eventos](/windows/desktop/EventLog/event-logging).<br/> |
| [**ComplexData**](eventschema-complexdata-eventdatatype-element.md) | [**ComplexDataType**](eventschema-complexdatatype-complextype.md) | Uma estrutura que é definida no modelo para o evento.<br/>                                |
| [**Dados**](eventschema-data-eventdatatype-element.md)               | [**DataType**](eventschema-datafieldtype-complextype.md)          | Um item de dados de nível superior que é definido no modelo para o evento.<br/>                      |



## <a name="attributes"></a>Atributos



| Nome | Tipo   | Descrição                                                       |
|------|--------|-------------------------------------------------------------------|
| Nome | cadeia de caracteres | O nome do modelo que contém os itens de dados.<br/> |



## <a name="remarks"></a>Comentários

A função [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) renderiza matrizes e estruturas como blobs binários.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

