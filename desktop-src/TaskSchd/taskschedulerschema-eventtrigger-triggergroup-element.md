---
title: Elemento EventTrigger (triggerGroup)
description: Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- event trigger Agendador de Tarefas , element
- Elemento EventTrigger Agendador de Tarefas
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 555c8683933b2242d119fc00f29c6d0a33188f6404ca48a00e8a127dd59aa791
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424466"
---
# <a name="eventtrigger-triggergroup-element"></a>Elemento EventTrigger (triggerGroup)

Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

O **elemento EventTrigger** é definido pelo [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica os gatilhos que iniciam a tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                              | Digite                                                                     | Descrição                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay (eventTriggerType)**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                 | Especifica a quantidade de tempo entre quando o evento ocorre e quando a tarefa é iniciada.<br/>                                |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)             | booleano                                                                  | Especifica que o gatilho está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)     | dateTime                                                                 | Especifica a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**Repetição (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)       | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica com que frequência a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md) | dateTime                                                                 | Especifica a data e a hora em que o gatilho é ativado.<br/>                                                              |
| [**Assinatura (eventTriggerType)**](taskschedulerschema-subscription-eventtriggertype-element.md) | string                                                                   | Especifica a consulta XPath que identifica o evento que dispara o gatilho.<br/>                                             |



## <a name="attributes"></a>Atributos



| Nome | Type | Descrição                           |
|------|------|---------------------------------------|
| ID   | ID   | Identificador do gatilho.<br/> |



## <a name="remarks"></a>Comentários

No máximo 500 tarefas com assinaturas de evento podem ser criadas. Uma assinatura de evento que consulta uma variedade de eventos pode ser usada para disparar uma tarefa que usa a mesma ação em resposta aos eventos que estão sendo registrados.

Para desenvolvimento de script, um gatilho de evento é definido pelo [**objeto EventTrigger.**](eventtrigger.md)

Para o desenvolvimento em C++, um gatilho de evento é definido pela interface [**IEventTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)

## <a name="examples"></a>Exemplos

Para ver um exemplo completo do XML para uma tarefa que usa um gatilho de evento, consulte [Exemplo de gatilho de evento (XML).](/previous-versions//aa446889(v=vs.85))

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

