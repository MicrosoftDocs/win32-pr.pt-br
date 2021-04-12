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
ms.openlocfilehash: 5d1bb655dcf13c70fb989756cb9f5716301934c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294745"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





