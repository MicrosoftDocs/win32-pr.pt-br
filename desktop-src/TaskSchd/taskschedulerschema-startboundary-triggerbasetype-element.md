---
title: Elemento StartBoundary (triggerBaseType)
description: Especifica a data e a hora em que o gatilho é ativado.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- Elemento StartBoundary Agendador de Tarefas
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32b91557d812888d9bb6e970be37703537bb3d7645c8a0422df19d5d5fe37a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401960"
---
# <a name="startboundary-triggerbasetype-element"></a>Elemento StartBoundary (triggerBaseType)

Especifica a data e a hora em que o gatilho é ativado.

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

O **elemento StartBoundary** é definido pelo tipo complexo [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                     | Derivado de                                                                               | Description                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Especifica um gatilho diário, semanal, mensal ou um gatilho DOW (dia da semana).<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Especifica um gatilho que inicia uma tarefa quando um usuário faz login.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.<br/>             |



## <a name="remarks"></a>Comentários

O **<StartBoundary>** elemento é um elemento necessário para gatilhos de tempo e calendário ( e [**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md) ).

Para o desenvolvimento de scripts, o limite final é especificado usando a [**propriedade Trigger.StartBoundary**](trigger-startboundary.md) herdada por todos os objetos de gatilho.

Para desenvolvimento em C++, o limite final é especificado usando a propriedade [**ITrigger::StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) herdada por todas as interfaces de gatilho.

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento de gatilho de inicialização que define um limite inicial de 1º de janeiro de 2005: 8h.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





