---
title: Elemento EventTrigger (Trigger)
description: Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- Agendador de Tarefas de gatilho de evento, elemento
- Agendador de Tarefas de elemento EventTrigger
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cecf46250fface0f716adbf287cda3269b86f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455634"
---
# <a name="eventtrigger-triggergroup-element"></a>Elemento EventTrigger (Trigger)

Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

O elemento **EventTrigger** é definido pelo [**disparador**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md) | [**TriggerType**](taskschedulerschema-triggerstype-complextype.md) | Especifica os gatilhos que iniciam a tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                              | Type                                                                     | Descrição                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Atraso (eventTriggertype)**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                 | Especifica a quantidade de tempo entre o momento em que o evento ocorre e quando a tarefa é iniciada.<br/>                                |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)             | booleano                                                                  | Especifica que o gatilho está habilitado.<br/>                                                                                  |
| [**TriggerBaseType (limite de entrada)**](taskschedulerschema-endboundary-triggerbasetype-element.md)     | dateTime                                                                 | Especifica a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**Repetição (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)       | [**repetição**](taskschedulerschema-repetitiontype-complextype.md) | Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md) | dateTime                                                                 | Especifica a data e a hora em que o gatilho é ativado.<br/>                                                              |
| [**Assinatura (eventTriggertype)**](taskschedulerschema-subscription-eventtriggertype-element.md) | string                                                                   | Especifica a consulta XPath que identifica o evento que dispara o gatilho.<br/>                                             |



## <a name="attributes"></a>Atributos



| Nome | Tipo | Descrição                           |
|------|------|---------------------------------------|
| ID   | ID   | Identificador do gatilho.<br/> |



## <a name="remarks"></a>Comentários

Um máximo de 500 tarefas com assinaturas de evento podem ser criadas. Uma assinatura de evento que consulta uma variedade de eventos pode ser usada para disparar uma tarefa que usa a mesma ação em resposta aos eventos que estão sendo registrados.

Para o desenvolvimento de script, um gatilho de evento é definido pelo objeto [**EventTrigger**](eventtrigger.md) .

Para desenvolvimento em C++, um gatilho de evento é definido pela interface [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) .

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que usa um gatilho de evento, consulte [exemplo de gatilho de evento (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

