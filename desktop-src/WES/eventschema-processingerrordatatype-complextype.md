---
title: Tipo complexo ProcessingErrorDataType
description: Define um erro que ocorreu ao renderizar os dados do evento.
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- Tipo complexo ProcessingErrorDataType EventLog
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ee34e566bafa72812303fcb1f41b664a45aa77772e6ee818b9cb79bc94cbb51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904517"
---
# <a name="processingerrordatatype-complex-type"></a>Tipo complexo ProcessingErrorDataType

Define um erro que ocorreu ao renderizar os dados do evento. Isso poderá ocorrer se os dados do evento não corresponderem à definição do modelo de dados de evento no manifesto.

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
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



| Elemento                                                                          | Type        | Descrição                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [**DataItemName**](eventschema-dataitemname-processingerrordatatype-element.md) | string      | O nome do item de dados do evento que causou o erro.<br/>                    |
| [**ErrorCode**](eventschema-errorcode-processingerrordatatype-element.md)       | unsignedInt | O código de erro do erro que ocorreu ao renderizar os dados do evento.<br/> |
| [**EventPayload**](eventschema-eventpayload-processingerrordatatype-element.md) | Hexbinary   | Um blob binário que contém todos os dados do evento.<br/>                        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





