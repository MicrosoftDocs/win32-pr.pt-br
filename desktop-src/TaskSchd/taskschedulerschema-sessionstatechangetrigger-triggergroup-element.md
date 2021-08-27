---
title: Elemento SessionStateChangeTrigger (Trigger)
description: Especifica um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- Agendador de Tarefas do elemento SessionStateChangeTrigger
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d22b2f47584f437c01575ffecfb6d5c25e312b9584ba46abc9d6997e14187eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099816"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a>Elemento SessionStateChangeTrigger (Trigger)

Especifica um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado.

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

O elemento **SessionStateChangeTrigger** é definido pelo [**disparador**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md) | [**TriggerType**](taskschedulerschema-triggerstype-complextype.md) | Especifica os gatilhos que iniciam a tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                      | Type                                                                                    | Descrição                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atrasar**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Especifica um valor que indica o comprimento do atraso antes que uma tarefa seja iniciada quando uma alteração de estado de sessão de Terminal Server for detectada.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Especifica o tipo de Terminal Server alteração de sessão que dispararia uma inicialização de tarefa.<br/>                                                     |
| [**ID**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md)                 | Especifica o usuário para a sessão de Terminal Server. Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.<br/>              |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, um gatilho de alteração de estado de sessão é especificado usando o objeto [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) .

Para desenvolvimento em C++, um gatilho de alteração de estado de sessão é especificado usando a interface [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





