---
title: Elemento Interval (restartType)
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
ms.openlocfilehash: 2362a5d6ec1a6a9d0d876ef0673f4775e2db3ade0a83696ad2b993e31e02a9ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099986"
---
# <a name="interval-restarttype-element"></a>Elemento Interval (restartType)

Especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa. O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, "PT5M" é 5 minutos, "PT1H" é 1 hora e "PT20M" é 20 minutos). O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.

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

O elemento é definido pelo tipo [**complexo restartType.**](taskschedulerschema-restarttype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                               | Derivado de                                                       | Descrição                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**restartType**](taskschedulerschema-restarttype-complextype.md) | Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.<br/> |



## <a name="remarks"></a>Comentários

Se esse elemento for especificado, o elemento [**Count**](taskschedulerschema-count-restarttype-element.md) também deverá ser especificado para dizer ao Agendador de Tarefas quantas vezes ele deve tentar reiniciar a tarefa.

Para desenvolvimento em C++, consulte [**Propriedade RestartInterval de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).

Para desenvolvimento de scripts, [**consulte TaskSettings.RestartInterval.**](tasksettings-restartinterval.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





