---
title: Tipo complexo triggersType
description: Define o grupo (triggerGroup) para todos os elementos de gatilho.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- tipo complexo triggersType Agendador de Tarefas
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c2bd6fa4011841958ad08239640024f9878528aecb1307487c3354ac74e31db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610533"
---
# <a name="triggerstype-complex-type"></a>Tipo complexo triggersType

Define o grupo ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) para todos os elementos de gatilho. O [**grupo triggerGroup**](taskschedulerschema-triggergroup-group.md) contém a lista de gatilhos que podem ser usados em uma tarefa.

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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





