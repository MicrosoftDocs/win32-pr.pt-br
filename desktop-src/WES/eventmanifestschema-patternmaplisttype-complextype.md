---
title: Tipo complexo PatternMapListType
description: Não usado. Define uma lista de pares de expressões regulares que são usados para alterar a cadeia de caracteres da mensagem.
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- Log de eventos do tipo complexo PatternMapListType
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbf96f7033f353662578e477fb8e35e0bfcda6db390f6492e29840e5e1faa5cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136199"
---
# <a name="patternmaplisttype-complex-type"></a>Tipo complexo PatternMapListType

Não usado. Define uma lista de pares de expressões regulares que são usados para alterar a cadeia de caracteres da mensagem.

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                         | Type                                                                     | Descrição                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**patternMap**](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [**PatternMapType**](eventmanifestschema-patternmaptype-complextype.md) | Define um mapeamento entre duas expressões regulares. Uma expressão é usada para localizar uma cadeia de caracteres correspondente na cadeia de caracteres de mensagem e a outra é usada para alterar a cadeia de caracteres antes que o serviço a Coloque novamente na cadeia de caracteres de mensagem. O primeiro mapeamento de padrão que corresponde a é usado e outros padrões não são tentados.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





