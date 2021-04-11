---
title: Elemento LogonTrigger (Trigger)
description: Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- gatilho de logon, elemento XML
- Agendador de Tarefas do elemento LogonTrigger
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294793"
---
# <a name="logontrigger-triggergroup-element"></a>Elemento LogonTrigger (Trigger)

Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

O elemento **LogonTrigger** é definido pelo [**disparador**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md) | [**TriggerType**](taskschedulerschema-triggerstype-complextype.md) | Especifica os gatilhos que iniciam a tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                        | Type                                                                     | Descrição                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Atraso (logonTriggerType)**](taskschedulerschema-delay-logontriggertype-element.md)                         | duration                                                                 | Quantidade de tempo entre quando o usuário faz logon e quando a tarefa é iniciada.<br/>                                              |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | booleano                                                                  | Especifica que o gatilho está habilitado.<br/>                                                                                  |
| [**TriggerBaseType (limite de entrada)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Especifica a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.<br/>                                   |
| [**Repetição (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetição**](taskschedulerschema-repetitiontype-complextype.md) | Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Especifica a data e a hora em que o gatilho é ativado.<br/>                                                              |
| [**UserId (logonTriggerType)**](taskschedulerschema-userid-logontriggertype-element.md)                       | string                                                                   | Identificador do usuário. A tarefa é iniciada quando esse usuário faz logon no computador.<br/>                                      |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, um gatilho de logon é especificado usando o objeto [**LogonTrigger**](logontrigger.md) .

Para desenvolvimento em C++, um gatilho de logon é especificado usando a interface [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) .

Os elementos filho listados acima são definidos pelos tipos de elementos complexos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) . Esses elementos devem ser adicionados na sequência mostrada abaixo.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**TriggerBaseType (limite de entrada)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Repetição (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**UserId (logonTriggerType)**](taskschedulerschema-userid-logontriggertype-element.md)
-   [**Atraso (logonTriggerType)**](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a>Atributos

O atributo listado abaixo é definido pelos tipos de elementos complexos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

-   ID: identificador do gatilho.

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que usa um gatilho de logon, consulte [exemplo de gatilho de logon (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





