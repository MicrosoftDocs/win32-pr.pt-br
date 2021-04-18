---
title: Tipo complexo TriggerType
description: Define o grupo (Trigger) para todos os elementos de gatilho.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- tipo complexo de TriggerType Agendador de Tarefas
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789442"
---
# <a name="triggerstype-complex-type"></a>Tipo complexo TriggerType

Define o grupo ([**Trigger**](taskschedulerschema-triggergroup-group.md)) para todos os elementos de gatilho. O grupo de [**disparadores**](taskschedulerschema-triggergroup-group.md) contém a lista de gatilhos que podem ser usados em uma tarefa.

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





