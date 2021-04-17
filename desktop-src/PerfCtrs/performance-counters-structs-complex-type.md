---
description: Define uma lista de estruturas que contêm valores de contadores.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Tipo complexo de structs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783251"
---
# <a name="structs-complex-type"></a>Tipo complexo de structs

Define uma lista de estruturas que contêm valores de contadores.

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento    | Type                                                           | Descrição                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| **struct** | [**homem: struct**](performance-counters-struct-complex-type.md) | O nome de uma estrutura que contém valores de contador.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




