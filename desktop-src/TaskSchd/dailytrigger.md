---
title: Objeto DailyTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa com base em uma agenda diária.
ms.assetid: f03f53a0-0060-4793-96c1-b47a96852579
keywords:
- gatilho diário Agendador de Tarefas , objeto
- Objeto DailyTrigger Agendador de Tarefas
- Objeto DailyTrigger Agendador de Tarefas , descrito
topic_type:
- apiref
api_name:
- DailyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b330906b309bbd672fcb9c333bc254fb02ee668549764d7dc1375f6ac405a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060174"
---
# <a name="dailytrigger-object"></a>Objeto DailyTrigger

Objeto de script que representa um gatilho que inicia uma tarefa com base em uma agenda diária.

## <a name="members"></a>Membros

O **objeto DailyTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto DailyTrigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysInterval**](dailytrigger-daysinterval.md)<br/>        | Leitura/gravação<br/> | Obtém ou define o intervalo entre os dias na agenda.<br/>                                                                                                                      |
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define um valor booliana que indica se o gatilho está habilitado.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a quantidade máxima de tempo que a tarefa lançada pelo gatilho tem permissão para ser executado.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define o identificador do gatilho.<br/>                                                                               |
| [**RandomDelay**](dailytrigger-randomdelay.md)<br/>          | Leitura/gravação<br/> | Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.<br/>                                                                                               |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a frequência com que a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Somente leitura<br/>  | Herdado do [**objeto Trigger.**](trigger.md) Obtém o tipo do gatilho.<br/>                                                                                              |



 

## <a name="remarks"></a>Comentários

A hora do dia em que a tarefa é iniciada é definida pela [**propriedade StartBoundary.**](trigger-startboundary.md)

Um intervalo de 1 produz uma agenda diária. Um intervalo de 2 produz uma agenda a cada dois dias e assim por diante.

Ao ler ou escrever seu próprio XML para uma tarefa, um gatilho diário é especificado usando o [**elemento ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) do Agendador de Tarefas esquema.

## <a name="examples"></a>Exemplos

Para obter mais informações e um exemplo de código para esse objeto de script, consulte Exemplo de [gatilho diário (Scripts).](daily-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Gatilho**](trigger.md)
</dt> <dt>

[**Triggercollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





