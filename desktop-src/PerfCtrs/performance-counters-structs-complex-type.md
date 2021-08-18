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
ms.openlocfilehash: 0dfa7f72ee537d857f19301aa4df906d94b0bf7ba9e3f7a76bdb6ab82c84dfd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314416"
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



| Elemento    | Digite                                                           | Description                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| **struct** | [**homem: struct**](performance-counters-struct-complex-type.md) | O nome de uma estrutura que contém valores de contador.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 




