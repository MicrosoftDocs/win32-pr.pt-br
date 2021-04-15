---
title: Objeto IdleTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa quando ocorre uma condição ociosa.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- Agendador de Tarefas do gatilho de ociosidade, objeto
- Agendador de Tarefas de objeto IdleTrigger
- Agendador de Tarefas de objeto IdleTrigger, descrito
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72288827fec34257bf4f54a152031ef37068790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761341"
---
# <a name="idletrigger-object"></a>Objeto IdleTrigger

Objeto de script que representa um gatilho que inicia uma tarefa quando ocorre uma condição ociosa. Para obter informações sobre condições ociosas, consulte [condições de ociosidade da tarefa](task-idle-conditions.md).

## <a name="members"></a>Membros

O objeto **IdleTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **IdleTrigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define um valor booliano que indica se o gatilho está habilitado.<br/>                                                              |
| [Limite de fim](trigger-endboundary.md)<br/>                   | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.<br/>                                                 |
| [**Sessão**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define o identificador do gatilho.<br/>                                                                                             |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define um valor que indica a frequência em que a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                                            |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Somente leitura<br/>  | Herdado do objeto de [**gatilho**](trigger.md) . Obtém o tipo do gatilho.<br/>                                                                                                            |



 

## <a name="remarks"></a>Comentários

Um gatilho ocioso só disparará uma ação de tarefa se o computador entrar em um estado ocioso após o limite de início do gatilho.

Ao ler ou gravar XML para uma tarefa, um gatilho de ociosidade é especificado usando o elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) do esquema de Agendador de tarefas.

Se uma tarefa for disparada por um gatilho ocioso, a propriedade [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) será ignorada.

Se a instância inicial de uma tarefa com um gatilho de ociosidade ainda estiver em execução, a tarefa será iniciada apenas uma vez sem repetições, mesmo que várias repetições sejam definidas na propriedade de [**repetição**](trigger-repetition.md) . Esse comportamento não ocorrerá se a tarefa for interrompida por si só.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Of**](trigger.md)
</dt> <dt>

[Objetos Agendador de Tarefas](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





