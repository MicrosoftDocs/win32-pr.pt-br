---
title: Elemento Triggers (taskType)
description: Especifica os gatilhos que iniciam a tarefa.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Elemento triggers Agendador de Tarefas
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d067c9e315006c55e07e972e5616525750d8a383d7ed8294f7d39a6acf32caff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610880"
---
# <a name="triggers-tasktype-element"></a>Elemento Triggers (taskType)

Especifica os gatilhos que iniciam a tarefa.

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

O elemento **triggers** é definido pelo tipo complexo [**TriggerType**](taskschedulerschema-triggerstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                          | Derivado de                                                 | Descrição                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Tarefa**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Define a tarefa que é executada pelo serviço de Agendador de Tarefas.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                     | Type                                                                                       | Descrição                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggertype**](taskschedulerschema-eventtriggertype-complextype.md)               | Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.<br/>             |



## <a name="remarks"></a>Comentários

Os elementos filho listados acima podem ser adicionados em qualquer ordem.

Para desenvolvimento em C++, os gatilhos de uma tarefa são especificados usando a [**Propriedade Triggers de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).

Para o desenvolvimento de scripts, os gatilhos de uma tarefa são especificados usando a propriedade [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).

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

 

 





