---
title: tipo simples priorityType
description: Define os valores mínimo e máximo para o elemento Priority (settingsType).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- tipo simples priorityType Agendador de Tarefas
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 71bdf8b87a641247ce2064ccf44ee861d79aab0593229e4cd7b38035c5c7c124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424426"
---
# <a name="prioritytype-simple-type"></a>tipo simples priorityType

Define os valores mínimo e máximo para o [**elemento Priority (settingsType).**](taskschedulerschema-priority-settingstype-element.md)

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O **tipo simples priorityType** define os valores a seguir.



| Valor | Descrição                         |
|-------|-------------------------------------|
| 0     | Inteiro mínimo permitido.<br/> |
| 10    | Inteiro máximo permitido.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas tipos simples de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





