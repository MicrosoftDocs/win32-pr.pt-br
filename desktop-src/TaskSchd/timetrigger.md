---
title: Objeto TimeTrigger (Windows.applicationmodel.background.h)
description: Objeto de script que representa um gatilho que inicia uma tarefa em uma data e hora específicas.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- time trigger Agendador de Tarefas , object
- Objeto TimeTrigger Agendador de Tarefas
- Objeto TimeTrigger Agendador de Tarefas , descrito
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f0fb6f5eaff5101f3cc1f5c4aeb2245335e4f65b27d2fafb364df2d05618ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771976"
---
# <a name="timetrigger-object"></a>Objeto TimeTrigger

Objeto de script que representa um gatilho que inicia uma tarefa em uma data e hora específicas.

## <a name="members"></a>Membros

O **objeto TimeTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto TimeTrigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define um valor booliana que indica se o gatilho está habilitado.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define a quantidade máxima de tempo que a tarefa lançada pelo gatilho tem permissão para ser executado.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define o identificador do gatilho.<br/>                                                                               |
| [**RandomDelay**](dailytrigger-randomdelay.md)<br/>          | Leitura/gravação<br/> | Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.<br/>                                                                                    |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define a frequência com que a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define a data e a hora em que o gatilho é ativado. Este elemento é obrigatório.<br/>                                    |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Somente leitura<br/>  | Herdado do [**gatilho**](trigger.md). Obtém o tipo do gatilho.<br/>                                                                                              |



 

## <a name="remarks"></a>Comentários

O [**elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de tempo e calendário [**(TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) e [**CalendarTrigger).**](taskschedulerschema-calendartrigger-triggergroup-element.md)

Ao ler ou escrever XML para uma tarefa, um gatilho ocioso é especificado usando o [**elemento TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) do esquema Agendador de Tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e um código de exemplo para esse objeto de script, consulte [Exemplo de gatilho de tempo (scripts).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                             |
| Cabeçalho<br/>                   | <dl> <dt>Windows.applicationmodel.background.h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl>                          |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Gatilho**](trigger.md)
</dt> <dt>

[**Triggercollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





