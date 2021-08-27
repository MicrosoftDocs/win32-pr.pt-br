---
title: Tipo complexo monthlyScheduleType
description: Define os elementos filho e informações de sequenciamento para o elemento ScheduleByMonth (calendarTriggerType).
ms.assetid: 3ade775c-ca44-403e-9602-80095c7dba1a
keywords:
- tipo complexo monthlyScheduleType Agendador de Tarefas
topic_type:
- apiref
api_name:
- monthlyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06bb8786e817c59209d4b3807d119c017a6a04ae3eff5cfe623b76d57e04b9f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991136"
---
# <a name="monthlyscheduletype-complex-type"></a>Tipo complexo monthlyScheduleType

Define os elementos filho e informações de sequenciamento para o [**elemento ScheduleByMonth (calendarTriggerType).**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)

``` syntax
<xs:complexType name="monthlyScheduleType">
    <xs:all>
        <xs:element name="DaysOfMonth"
            type="daysOfMonthType"
            minOccurs="0"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                            | Type                                                                       | Descrição                                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Especifica os dias do mês durante os quais a tarefa é executado.<br/>                         |
| [**Meses**](taskschedulerschema-months-monthlyscheduletype-element.md)           | [**monthsType**](taskschedulerschema-monthstype-complextype.md)           | Especifica os meses do ano durante os quais a tarefa é executado para um agendamento mensal.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas complexos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





