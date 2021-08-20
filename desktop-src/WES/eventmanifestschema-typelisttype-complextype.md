---
title: Tipo complexo TypeListType
description: Define os tipos que são usados no manifesto.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- Log de eventos do tipo complexo TypeListType
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6d82d4b7d7369af23c3275a24f299f778d833073e55668f9624a9e5efbfaf544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117936871"
---
# <a name="typelisttype-complex-type"></a>Tipo complexo TypeListType

Define os tipos que são usados no manifesto.

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Type                                                                           | Descrição                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**intipos**](eventmanifestschema-intypes-typelisttype-element.md)   | [**InputTypeListType**](eventmanifestschema-inputtypelisttype-complextype.md) | Define uma lista de tipos de dados de entrada.<br/>                                                              |
| [**xmltipos**](eventmanifestschema-xmltypes-typelisttype-element.md) | [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)     | Define uma lista de tipos de saída que o serviço usa para determinar como renderizar um tipo de dados de entrada.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





