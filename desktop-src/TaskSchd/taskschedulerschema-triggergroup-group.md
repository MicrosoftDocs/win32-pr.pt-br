---
title: Grupo de disparadores
description: Define o grupo de gatilhos.
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- Agendador de Tarefasdor de gatilho
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce0203cd9515808891f93223dd7b3ebaf2642103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086443"
---
# <a name="triggergroup-group"></a>Grupo de disparadores

Define o grupo de gatilhos.

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                 | Type                                                                                                   | Descrição                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                             | Um gatilho que inicia uma tarefa quando o sistema é inicializado.<br/>                                                |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)                     | Um gatilho que inicia uma tarefa com base em uma agenda de DOW (dia da semana) diária, semanal, mensal ou mensal.<br/> |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [**eventTriggertype**](taskschedulerschema-eventtriggertype-complextype.md)                           | Um gatilho que inicia uma tarefa quando ocorre um evento do sistema.<br/>                                               |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                             | Um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.<br/>                                |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)                           | Um gatilho que inicia uma tarefa quando um usuário faz logon.<br/>                                                      |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)             | Um gatilho que inicia uma tarefa quando a tarefa é registrada.<br/>                                              |
| [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado.<br/>                             |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md)                             | Um gatilho que inicia uma tarefa quando o gatilho é ativado.<br/>                                            |



## <a name="remarks"></a>Comentários

Ao ler ou gravar XML, os elementos definidos por esse grupo são os elementos filho do elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





