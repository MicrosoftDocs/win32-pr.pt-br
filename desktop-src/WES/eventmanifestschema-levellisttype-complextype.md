---
title: Tipo complexo LevelListType
description: Define uma lista de níveis de severidade que especificam o detalhamento de um evento.
ms.assetid: 82102f8a-271e-4c3d-9b0a-1e20eaa87497
keywords:
- Log de eventos do tipo complexo LevelListType
topic_type:
- apiref
api_name:
- LevelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4456ade3977603948997304393a1c9414cb0c458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455973"
---
# <a name="levellisttype-complex-type"></a>Tipo complexo LevelListType

Define uma lista de níveis de severidade que especificam o detalhamento de um evento.

``` syntax
<xs:complexType name="LevelListType">
    <xs:sequence>
        <xs:element name="level"
            type="LevelType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                          | Type                                                           | Descrição                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**geral**](eventmanifestschema-level-levellisttype-element.md) | [**LevelType**](eventmanifestschema-leveltype-complextype.md) | Define um valor de severidade que determina o detalhamento de eventos durante o registro em log.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





