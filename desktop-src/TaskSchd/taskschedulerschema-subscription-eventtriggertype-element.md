---
title: Elemento Subscription (eventTriggertype)
description: Especifica a consulta XPath que identifica o evento que dispara o gatilho.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Elemento de assinatura Agendador de Tarefas
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645216"
---
# <a name="subscription-eventtriggertype-element"></a>Elemento Subscription (eventTriggertype)

Especifica a consulta XPath que identifica o evento que dispara o gatilho.

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

O elemento **Subscription** é definido pelo tipo complexo [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                       | Derivado de                                                                 | Descrição                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggertype**](taskschedulerschema-eventtriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de script, a assinatura de evento é especificada pela propriedade [**EventTrigger. Subscription**](eventtrigger-subscription.md) .

Para desenvolvimento em C++, a assinatura de evento é especificada pela propriedade [**IEventTrigger:: Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) .

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

 

 





