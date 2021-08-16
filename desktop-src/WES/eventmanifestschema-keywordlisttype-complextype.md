---
title: Tipo complexo
description: Define uma lista de palavras-chave que categorizam eventos. | Tipo complexo
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- Log de tipos de tipo complexo de
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: da027136deed48a97b2ea9384bc37a1a45d00650d90b8fd855ea8226e58583aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343633"
---
# <a name="keywordlisttype-complex-type"></a>Tipo complexo

Define uma lista de palavras-chave que categorizam eventos.

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                | Type                                                               | Descrição                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**chaves**](eventmanifestschema-keyword-keywordlisttype-element.md) | [**Keywordtype**](eventmanifestschema-keywordtype-complextype.md) | Define uma palavra-chave que identifica uma categoria de eventos. Você pode especificar um máximo de 48 palavras-chave.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





