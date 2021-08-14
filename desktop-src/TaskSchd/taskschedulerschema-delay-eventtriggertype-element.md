---
title: Elemento Delay (eventTriggerType)
description: Especifica a quantidade de tempo entre quando o evento ocorre e quando a tarefa é iniciada.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- Elemento Delay Agendador de Tarefas
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c9523b450d5f1ea86bdf09afba26604ebfe8055661fc18c439b4e30c97169d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357095"
---
# <a name="delay-eventtriggertype-element"></a>Elemento Delay (eventTriggerType)

Especifica a quantidade de tempo entre quando o evento ocorre e quando a tarefa é iniciada. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, em que nY é o número de anos, nM é o número de meses, nD é o número de dias, 'T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

O **elemento Delay** é definido pelo tipo complexo [**eventTriggerType.**](taskschedulerschema-eventtriggertype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                       | Derivado de                                                                 | Descrição                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento de script, o atraso do gatilho de evento é especificado pela [**propriedade EventTrigger.Delay.**](eventtrigger-delay.md)

Para o desenvolvimento em C++, o atraso do gatilho de evento é especificado pela propriedade [**IEventTrigger::D elay.**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





