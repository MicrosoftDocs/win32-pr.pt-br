---
title: Objeto trigger
description: Objeto de script que fornece as propriedades comuns herdadas por todos os objetos de gatilho.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- gatilhos Agendador de Tarefas , objeto de gatilho
- Gatilho de objeto Agendador de Tarefas
- Gatilho de objeto Agendador de Tarefas , descrito
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
ms.openlocfilehash: 3b27427bf77465be119fc678cb4babf85254fa437b350c54d4409c0cd5b28024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002004"
---
# <a name="trigger-object"></a>Objeto trigger

Objeto de script que fornece as propriedades comuns herdadas por todos os objetos de gatilho.

## <a name="members"></a>Membros

O **objeto Trigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto Trigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define um valor booliana que indica se o gatilho está habilitado.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Leitura/gravação<br/> | Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Obtém ou define a quantidade máxima de tempo que a tarefa lançada pelo gatilho tem permissão para ser executado.<br/>                                         |
| [**Id**](trigger-id.md)<br/>                                 | Leitura/gravação<br/> | Obtém ou define o identificador do gatilho.<br/>                                                                                             |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define um valor que indica com que frequência a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.<br/> |
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

Ao ler ou escrever XML, os gatilhos de uma tarefa são especificados no elemento [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) do esquema Agendador de Tarefas dados.

## <a name="examples"></a>Exemplos

Para obter mais informações e um código de exemplo para esse objeto de script, consulte [Exemplo de gatilho de tempo (scripts).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Triggercollection**](triggercollection.md)
</dt> </dl>

 

 





