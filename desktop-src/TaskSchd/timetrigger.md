---
title: Objeto timetrigger (Windows. ApplicationModel. Background. h)
description: Objeto de script que representa um gatilho que inicia uma tarefa em uma data e hora específicas.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- Agendador de Tarefas do gatilho de tempo, objeto
- Agendador de Tarefas de objeto timetrigger
- Agendador de Tarefas de objeto timetrigger, descrito
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
ms.openlocfilehash: 1a8403b93e1c5292ade9f6f402b7e41994339140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295824"
---
# <a name="timetrigger-object"></a>Objeto timetrigger

Objeto de script que representa um gatilho que inicia uma tarefa em uma data e hora específicas.

## <a name="members"></a>Membros

O objeto **timetrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **timetrigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define um valor booliano que indica se o gatilho está habilitado.<br/>                                                |
| [**Limite de fim**](trigger-endboundary.md)<br/>               | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.<br/>                           |
| [**Sessão**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define o identificador do gatilho.<br/>                                                                               |
| [**RandomDelay**](dailytrigger-randomdelay.md)<br/>          | Leitura/gravação<br/> | Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.<br/>                                                                                    |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Herdado do [**gatilho**](trigger.md). Obtém ou define a data e a hora em que o gatilho é ativado. Este elemento é obrigatório.<br/>                                    |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Somente leitura<br/>  | Herdado do [**gatilho**](trigger.md). Obtém o tipo do gatilho.<br/>                                                                                              |



 

## <a name="remarks"></a>Comentários

O elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de tempo e calendário ([**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) e [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Ao ler ou gravar XML para uma tarefa, um gatilho de ociosidade é especificado usando o elemento [**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                             |
| parâmetro<br/>                   | <dl> <dt>Windows. ApplicationModel. Background. h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>                          |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Of**](trigger.md)
</dt> <dt>

[**Disparador**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





