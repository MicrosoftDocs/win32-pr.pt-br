---
title: Objeto de gatilho
description: Objeto de script que fornece as propriedades comuns que são herdadas por todos os objetos de gatilho.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- disparadores Agendador de Tarefas, objeto de gatilho
- Agendador de Tarefas do objeto de gatilho
- Agendador de Tarefas do objeto de gatilho, descrito
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824280"
---
# <a name="trigger-object"></a>Objeto de gatilho

Objeto de script que fornece as propriedades comuns que são herdadas por todos os objetos de gatilho.

## <a name="members"></a>Membros

O objeto de **gatilho** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **gatilho** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica se o gatilho está habilitado.<br/>                                                              |
| [**Limite de fim**](trigger-endboundary.md)<br/>               | Leitura/gravação<br/> | Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.<br/>                                         |
| [**Sessão**](trigger-id.md)<br/>                                 | Leitura/gravação<br/> | Obtém ou define o identificador do gatilho.<br/>                                                                                             |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define um valor que indica a frequência em que a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Obtém ou define a data e a hora em que o gatilho é ativado. O gatilho pode iniciar a tarefa depois que o gatilho é ativado.<br/>             |
| [**Tipo**](trigger-type.md)<br/>                             |                       | Obtém o tipo do gatilho.<br/>                                                                                                            |



 

## <a name="remarks"></a>Comentários

O Agendador de Tarefas fornece os seguintes objetos individuais para os diferentes gatilhos que uma tarefa pode usar:

-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**SessionStateChangeTrigger**](sessionstatechangetrigger.md)

Ao ler ou gravar XML, os gatilhos de uma tarefa são especificados no elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Disparador**](triggercollection.md)
</dt> </dl>

 

 





