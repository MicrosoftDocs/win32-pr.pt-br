---
title: Elemento StateChange (sessionStateChangeTriggerType)
description: Contém o tipo de Terminal Server alteração de sessão que dispararia um lançamento de tarefa.
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- Agendador de Tarefas do elemento StateChange
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88b7e46b23cf6778379a967e03d8f168de3b18d20a734812bacdad940850136a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356328"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a>Elemento StateChange (sessionStateChangeTriggerType)

Contém o tipo de Terminal Server alteração de sessão que dispararia um lançamento de tarefa.

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

O elemento **StateChange** é definido pelo tipo complexo [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                       | Derivado de                                                                                           | Descrição                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade StateChange de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).

Para desenvolvimento de script, consulte [**SessionStateChangeTrigger. StateChange**](sessionstatechangetrigger-statechange.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





