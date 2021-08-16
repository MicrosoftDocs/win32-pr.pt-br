---
title: Elemento Delay (registrationTriggerType)
description: Especifica a quantidade de tempo entre quando a tarefa é registrada e quando a tarefa é iniciada.
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
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
ms.openlocfilehash: cd7ba3e9fd0fb71da628ee15bc0f1bdf6281e74ef20f259faf7a5a63504a6f12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131845"
---
# <a name="delay-registrationtriggertype-element"></a>Elemento Delay (registrationTriggerType)

Especifica a quantidade de tempo entre quando a tarefa é registrada e quando a tarefa é iniciada. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

O elemento **Delay** é definido pelo tipo complexo [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                     | Derivado de                                                                               | Descrição                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, o atraso do gatilho de registro é especificado usando a propriedade [**RegistrationTrigger. Delay**](registrationtrigger-delay.md) .

Para desenvolvimento em C++, o atraso do gatilho de registro é especificado usando a propriedade [**IRegistrationTrigger::D epetição**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) .

## <a name="examples"></a>Exemplos

O XML a seguir define um atraso de gatilho de registro que permite um atraso de 5 minutos entre o momento em que a tarefa é registrada e quando a tarefa é iniciada.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



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

 

 





