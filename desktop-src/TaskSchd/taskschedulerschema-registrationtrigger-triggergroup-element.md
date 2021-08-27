---
title: Elemento RegistrationTrigger (Trigger)
description: Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- gatilho de registro Agendador de Tarefas, elemento XML
- Agendador de Tarefas do elemento RegistrationTrigger
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 548ffec6bf5982aac407905d944d029b222b741c0c03fe66645f68e771c87342
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099966"
---
# <a name="registrationtrigger-triggergroup-element"></a>Elemento RegistrationTrigger (Trigger)

Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

O elemento **RegistrationTrigger** é definido pelo tipo complexo [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md) | [**TriggerType**](taskschedulerschema-triggerstype-complextype.md) | Especifica os gatilhos que iniciam a tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                        | Type                                                                     | Descrição                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Atraso (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                   | duration                                                                 | Especifica a quantidade de tempo entre quando a tarefa é registrada e quando a tarefa é iniciada.<br/>                          |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | booleano                                                                  | Especifica que o gatilho está habilitado.<br/>                                                                                  |
| [**TriggerBaseType (limite de entrada)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Especifica a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.<br/>                                   |
| [**Repetição (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetição**](taskschedulerschema-repetitiontype-complextype.md) | Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Especifica a data e a hora em que o gatilho é ativado.<br/>                                                              |



## <a name="attributes"></a>Atributos



| Nome | Tipo | Descrição                           |
|------|------|---------------------------------------|
| ID   | ID   | Identificador do gatilho.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, um gatilho de registro é especificado usando o objeto [**RegistrationTrigger**](registrationtrigger.md) .

Para desenvolvimento em C++, um gatilho de registro é especificado usando a interface [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) .

Os elementos filho listados acima são definidos pelos tipos de elementos complexos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) . Esses elementos devem ser adicionados na sequência mostrada abaixo.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**TriggerBaseType (limite de entrada)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Repetição (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**Atraso (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho de inicialização, consulte [exemplo de gatilho de registro (XML)](registration-trigger-example--xml-.md).

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

 

 





