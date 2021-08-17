---
title: Tipo complexo TaskListtype
description: Define uma lista de tarefas que são usadas para identificar os componentes de um aplicativo.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- Log de eventos de tipo complexo TaskListtype
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d59457aaeeefeec4b490b4c399a2faafb4f62c22e67a600f741ccc16b3abcaad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750902"
---
# <a name="tasklisttype-complex-type"></a>Tipo complexo TaskListtype

Define uma lista de tarefas que são usadas para identificar os componentes de um aplicativo.

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                       | Type                                                         | Descrição                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**agenda**](eventmanifestschema-task-tasklisttype-element.md) | [**TaskType**](eventmanifestschema-tasktype-complextype.md) | Define um componente ou subcomponente de um aplicativo.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





