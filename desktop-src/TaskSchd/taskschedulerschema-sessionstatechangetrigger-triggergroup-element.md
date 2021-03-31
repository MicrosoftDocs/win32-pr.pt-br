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
ms.openlocfilehash: d21847a929e79e2da53b1e66a23aec0c2f1c630f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644963"
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
| [**Retardo**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Especifica um valor que indica o comprimento do atraso antes que uma tarefa seja iniciada quando uma alteração de estado de sessão de Terminal Server for detectada.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Especifica o tipo de Terminal Server alteração de sessão que dispararia uma inicialização de tarefa.<br/>                                                     |
| [**ID**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md)                 | Especifica o usuário para a sessão de Terminal Server. Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.<br/>              |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, um gatilho de alteração de estado de sessão é especificado usando o objeto [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) .

Para desenvolvimento em C++, um gatilho de alteração de estado de sessão é especificado usando a interface [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





