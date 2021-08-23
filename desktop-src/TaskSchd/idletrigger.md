---
title: Objeto IdleTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa quando ocorre uma condição ociosa.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- gatilho ocioso Agendador de Tarefas , objeto
- Objeto IdleTrigger Agendador de Tarefas
- Objeto IdleTrigger Agendador de Tarefas , descrito
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
ms.openlocfilehash: 41a3c538dbd04f3eb20a86f495fcf4a8b027b51fbe5cd6443cd8ff3a69ac6ff5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621136"
---
# <a name="idletrigger-object"></a>Objeto IdleTrigger

Objeto de script que representa um gatilho que inicia uma tarefa quando ocorre uma condição ociosa. Para obter informações sobre condições ociosas, consulte [Condições ociosas da tarefa](task-idle-conditions.md).

## <a name="members"></a>Membros

O **objeto IdleTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto IdleTrigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define um valor booliana que indica se o gatilho está habilitado.<br/>                                                              |
| [EndBoundary](trigger-endboundary.md)<br/>                   | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.<br/>                                                 |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define o identificador do gatilho.<br/>                                                                                             |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define um valor que indica com que frequência a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                                            |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Somente leitura<br/>  | Herdado do [**objeto Trigger.**](trigger.md) Obtém o tipo do gatilho.<br/>                                                                                                            |



 

## <a name="remarks"></a>Comentários

Um gatilho ocioso só disparará uma ação de tarefa se o computador entrar em um estado ocioso após o limite de início do gatilho.

Ao ler ou escrever XML para uma tarefa, um gatilho ocioso é especificado usando o [**elemento IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) do esquema Agendador de Tarefas.

Se uma tarefa for disparada por um gatilho ocioso, a propriedade [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) será ignorada.

Se a instância inicial de uma tarefa com um gatilho ocioso ainda estiver em execução, a tarefa só será inicializada uma vez sem repetições, mesmo que várias repetições seja definida na [**propriedade Repetição.**](trigger-repetition.md) Esse comportamento não ocorrerá se a tarefa parar por si só.

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

[Agendador de Tarefas objetos](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





