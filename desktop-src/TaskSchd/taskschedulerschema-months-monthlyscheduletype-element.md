---
title: Mês (monthlyScheduleType) elemento
description: Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
keywords:
- Agendador de Tarefas do elemento months
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b655b47fc3135006f8629246d63350d36a4b32e92398a00f40ae86fe3f70d1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796496"
---
# <a name="months-monthlyscheduletype-element"></a>Mês (monthlyScheduleType) elemento

Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

O elemento **months** é definido pelo tipo complexo [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                    | Derivado de                                                                       | Descrição                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) | Especifica um agendamento mensal. <br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                            | Type | Descrição                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Abril (meses)**](taskschedulerschema-april-monthstype-element.md)         |      | Especifica que a tarefa é executada em abril.<br/>     |
| [**Agosto (meses)**](taskschedulerschema-august-monthstype-element.md)       |      | Especifica que a tarefa é executada em agosto.<br/>    |
| [**Dezembro (meses)**](taskschedulerschema-december-monthstype-element.md)   |      | Especifica que a tarefa é executada em dezembro.<br/>  |
| [**Fevereiro (meses)**](taskschedulerschema-february-monthstype-element.md)   |      | Especifica que a tarefa é executada em fevereiro.<br/>  |
| [**Janeiro (meses)**](taskschedulerschema-january-monthstype-element.md)     |      | Especifica que a tarefa é executada em Janeiro.<br/>   |
| [**Julho (meses)**](taskschedulerschema-july-monthstype-element.md)           |      | Especifica que a tarefa é executada em julho.<br/>      |
| [**Junho (monthtype)**](taskschedulerschema-june-monthstype-element.md)           |      | Especifica que a tarefa é executada em junho.<br/>      |
| [**Março (meses)**](taskschedulerschema-march-monthstype-element.md)         |      | Especifica que a tarefa é executada em março.<br/>     |
| [**Maio (monthtype)**](taskschedulerschema-may-monthstype-element.md)             |      | Especifica que a tarefa é executada em maio.<br/>       |
| [**Novembro (meses)**](taskschedulerschema-november-monthstype-element.md)   |      | Especifica que a tarefa é executada em novembro.<br/>  |
| [**Outubro (meses)**](taskschedulerschema-october-monthstype-element.md)     |      | Especifica que a tarefa é executada em outubro.<br/>   |
| [**Setembro (meses)**](taskschedulerschema-september-monthstype-element.md) |      | Especifica que a tarefa é executada em setembro.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de script, os meses de agendamento são especificados usando a propriedade [**MonthlyTrigger. MonthsOfYear**](monthlytrigger-monthsofyear.md) .

Para desenvolvimento em C++, os meses de agendamento são especificados usando a propriedade [**IMonthlyTrigger:: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) .

## <a name="examples"></a>Exemplos

O XML a seguir define um calendário mensal que inicia a tarefa no 1º e no 15º dia de cada mês do ano.


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
    <Months>
        <January/>
        <February/>
        <March/>
        <April/>
        <May/>
        <June/>
        <July/>
        <August/>
        <September/>
        <October/>
        <November/>
        <December/>
    <Months>
</ScheduleByMonth>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





