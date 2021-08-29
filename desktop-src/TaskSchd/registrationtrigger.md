---
title: Objeto RegistrationTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa quando a tarefa é registrada ou atualizada.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- gatilho de registro Agendador de Tarefas , objeto
- Objeto RegistrationTrigger Agendador de Tarefas
- Objeto RegistrationTrigger Agendador de Tarefas , descrito
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85020e3c5a2d5c3167ac2ec6ed251a37c1bc98056dae867a5a07b63ee7148dae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759566"
---
# <a name="registrationtrigger-object"></a>Objeto RegistrationTrigger

Objeto de script que representa um gatilho que inicia uma tarefa quando a tarefa é registrada ou atualizada.

## <a name="members"></a>Membros

O **objeto RegistrationTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto RegistrationTrigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atrasar**](registrationtrigger-delay.md)<br/>               | Leitura/gravação<br/> | Obtém ou define a quantidade de tempo entre quando a tarefa é registrada e quando a tarefa é iniciada.<br/>                                                                                |
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define um valor booliana que indica se o gatilho está habilitado.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a quantidade máxima de tempo que a tarefa lançada pelo gatilho tem permissão para ser executado.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define o identificador do gatilho.<br/>                                                                               |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a frequência com que a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Herdado do [**objeto Trigger.**](trigger.md) Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Somente leitura<br/>  | Herdado do [**objeto Trigger.**](trigger.md) Obtém o tipo do gatilho.<br/>                                                                                              |



 

## <a name="remarks"></a>Comentários

Ao criar seu próprio XML para uma tarefa, um gatilho de registro é especificado usando o [**elemento RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) do Agendador de Tarefas esquema.

Se uma tarefa com um gatilho de registro atrasado for registrada e o computador em que a tarefa está registrada for desligado ou reiniciado durante o atraso, antes da tarefa ser executado, a tarefa não será executado e o atraso será perdido.

## <a name="examples"></a>Exemplos

Para obter mais informações e um exemplo de código para esse objeto de script, consulte [Exemplo de gatilho de registro (Scripts).](registration-trigger-example--scripting-.md)

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

 

 





