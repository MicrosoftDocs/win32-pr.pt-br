---
title: Elemento repetition (triggerBaseType)
description: Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Elemento de repetição Agendador de Tarefas
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dfcce3e008a9959ca279f64c83a898eb2239d007d8fc32dfb5da5942395055bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959536"
---
# <a name="repetition-triggerbasetype-element"></a>Elemento repetition (triggerBaseType)

Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

O elemento de **repetição** é definido pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                     | Derivado de                                                                               | Descrição                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggertype**](taskschedulerschema-eventtriggertype-complextype.md)               | Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o computador entra em um estado ocioso.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md)                 | Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.<br/>             |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                   | Type     | Descrição                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [**Permanência**](taskschedulerschema-duration-repetitiontype-element.md)                   | duration | Especifica por quanto tempo o padrão é repetido.<br/>                                                              |
| [**Intervalo**](taskschedulerschema-interval-repetitiontype-element.md)                   | duration | Especifica a quantidade de tempo entre cada reinicialização da tarefa.<br/>                                           |
| [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | booleano  | Especifica que uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição.<br/> |



## <a name="remarks"></a>Comentários

Se você especificar uma duração de repetição para uma tarefa, também deverá especificar o intervalo de repetição.

Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada cinco vezes. As cinco repetições podem ser definidas pelo padrão a seguir.

1.  Uma tarefa é iniciada no início do primeiro minuto.
2.  A próxima tarefa é iniciada no final do primeiro minuto.
3.  A próxima tarefa é iniciada no final do segundo minuto.
4.  A próxima tarefa começa no final do terceiro minuto.
5.  A próxima tarefa é iniciada no final do quarto minuto.

**Windows Server 2003, Windows XP e Windows 2000:** Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada quatro vezes.

**Windows Vista, Windows 7, Windows Server 2008, Windows 8 e Windows Server 2012:** Normalmente, definir a duração da repetição como um múltiplo exato do intervalo produz os números descritos acima. No entanto, sob determinadas condições de carga pesada, é possível que a duração do tempo limite seja iniciada antes que TaskScheduler possa iniciar o intervalo final da tarefa.

Para o desenvolvimento de scripts, o padrão de repetição é especificado usando a propriedade [**Trigger. Repetition**](trigger-repetition.md) que é herdada por todos os objetos Trigger.

Para desenvolvimento em C++, o padrão de repetição é especificado usando a propriedade [**ITRigger:: repetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) que é herdada por todas as interfaces de gatilho.

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento de gatilho de inicialização que especifica um padrão de repetição para um gatilho.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
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

 

 





