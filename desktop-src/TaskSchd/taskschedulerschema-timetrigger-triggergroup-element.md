---
title: Elemento timetrigger (distrigger)
description: Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- Agendador de Tarefas de elemento de gatilho
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6b766a64f87b43feb23200176c5d23e254638a0022ea4d77b64264ca1d507d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355843"
---
# <a name="timetrigger-triggergroup-element"></a>Elemento timetrigger (distrigger)

Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

O elemento **timetrigger** é definido pelo [**disparador.**](taskschedulerschema-triggergroup-group.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md) | [**TriggerType**](taskschedulerschema-triggerstype-complextype.md) | Especifica os gatilhos que iniciam a tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                        | Type                                                                     | Descrição                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | booleano                                                                  | Especifica que o gatilho está habilitado.<br/>                                                                                  |
| [**TriggerBaseType (limite de entrada)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Especifica a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.<br/>                                   |
| [**Repetição (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetição**](taskschedulerschema-repetitiontype-complextype.md) | Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Especifica a data e a hora em que o gatilho é ativado. Este elemento é obrigatório.<br/>                                    |



## <a name="attributes"></a>Atributos



| Nome | Tipo       | Descrição                               |
|------|------------|-------------------------------------------|
| ID   | **cadeia de caracteres** | O identificador do gatilho.<br/> |



## <a name="remarks"></a>Comentários

O elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de tempo e calendário (**timetrigger** e [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Para o desenvolvimento de scripts, um gatilho de tempo é especificado usando o objeto [**timetrigger**](timetrigger.md) .

Para desenvolvimento em C++, um gatilho de tempo é especificado usando a interface [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) .

Os elementos filho listados acima são definidos pelos tipos de elementos complexos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) . Esses elementos devem ser adicionados na sequência mostrada abaixo.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**TriggerBaseType (limite de entrada)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Repetição (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho de tempo, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





