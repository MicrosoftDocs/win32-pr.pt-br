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
ms.openlocfilehash: 3991a767256184f23fbb9defda7e33465c0477e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086445"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





