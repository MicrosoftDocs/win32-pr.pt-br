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
ms.openlocfilehash: 8087913cacac67f0c7487b5eb41f404ebdc205765c693bdfda9f86995a809493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124296"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





