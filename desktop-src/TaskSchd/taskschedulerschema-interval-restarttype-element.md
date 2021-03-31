---
title: Elemento Interval (restartype)
description: Especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Elemento Interval Agendador de Tarefas
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c97e754e0b29a43d6ba419bd806404fe1b85b2b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918088"
---
# <a name="interval-restarttype-element"></a>Elemento Interval (restartype)

Especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa. O formato para essa cadeia de caracteres é P <days> dt <hours> H <minutes> M <seconds> S (por exemplo, "PT5M" é de 5 minutos, "PT1H" é de 1 hora e "PT20M" é de 20 minutos). O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo tipo complexo [**Restart**](taskschedulerschema-restarttype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                               | Derivado de                                                       | Description                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**Restart**](taskschedulerschema-restarttype-complextype.md) | Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.<br/> |



## <a name="remarks"></a>Comentários

Se esse elemento for especificado, o elemento [**Count**](taskschedulerschema-count-restarttype-element.md) também deverá ser especificado para informar ao agendador de tarefas quantas vezes ele deve tentar reiniciar a tarefa.

Para desenvolvimento em C++, consulte a [**Propriedade RestartInterval de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).

Para desenvolvimento de script, consulte [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





