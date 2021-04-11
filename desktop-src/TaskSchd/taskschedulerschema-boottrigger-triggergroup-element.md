---
title: Elemento BootTrigger (Trigger)
description: Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- gatilho de inicialização Agendador de Tarefas, elemento XML
- Agendador de Tarefas do elemento BootTrigger
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295838"
---
# <a name="boottrigger-triggergroup-element"></a>Elemento BootTrigger (Trigger)

Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

O elemento **BootTrigger** é definido pelo tipo complexo [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md) | [**TriggerType**](taskschedulerschema-triggerstype-complextype.md) | Especifica os gatilhos que iniciam a tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                        | Type                                                                     | Descrição                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Atraso (bootTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                           | duration                                                                 | Especifica a quantidade de tempo entre quando o sistema é inicializado e quando a tarefa é iniciada.<br/>                            |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | booleano                                                                  | Especifica que o gatilho está habilitado.<br/>                                                                                  |
| [**TriggerBaseType (limite de entrada)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Especifica a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.<br/>                                   |
| [**Repetição (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetição**](taskschedulerschema-repetitiontype-complextype.md) | Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Especifica a data e a hora em que o gatilho é ativado.<br/>                                                              |



## <a name="attributes"></a>Atributos



| Nome | Tipo       | Descrição                               |
|------|------------|-------------------------------------------|
| ID   | **cadeia de caracteres** | O identificador do gatilho.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de script, um gatilho de inicialização é definido pelo objeto [**BootTrigger**](boottrigger.md) .

Para desenvolvimento em C++, um gatilho de inicialização é definido pelo objeto [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) .

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho de inicialização, consulte [exemplo de gatilho de inicialização (XML)](boot-trigger-example--xml-.md).

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

 

 





