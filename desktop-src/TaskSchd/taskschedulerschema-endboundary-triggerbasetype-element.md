---
title: Elemento noboundal (triggerBaseType)
description: Especifica a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- Elemento de limite de Agendador de Tarefas
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d687655498301595c1ab888fcc179ec0694f0aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757943"
---
# <a name="endboundary-triggerbasetype-element"></a>Elemento noboundal (triggerBaseType)

Especifica a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

O elemento de **limite** de fim é definido pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                     | Derivado de                                                                               | Descrição                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggertype**](taskschedulerschema-eventtriggertype-complextype.md)               | Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.<br/>             |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, o limite final é especificado usando a propriedade [**Trigger. Endboundal**](trigger-endboundary.md) que é herdada por todos os objetos Trigger.

Para desenvolvimento em C++, o limite final é especificado usando a propriedade [**ITrigger:: Endboundal**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) que é herdada por todas as interfaces de gatilho.

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento de gatilho de inicialização que define um limite final de 1º de janeiro de 2007:8:00 AM.


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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





