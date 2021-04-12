---
title: Objeto RegistrationTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa quando a tarefa é registrada ou atualizada.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- gatilho de registro Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto RegistrationTrigger
- Agendador de Tarefas de objeto RegistrationTrigger, descrito
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
ms.openlocfilehash: 08bf84fa92b1736b2989c1920abb8f0af2c0b97c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499475"
---
# <a name="registrationtrigger-object"></a>Objeto RegistrationTrigger

Objeto de script que representa um gatilho que inicia uma tarefa quando a tarefa é registrada ou atualizada.

## <a name="members"></a>Membros

O objeto **RegistrationTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **RegistrationTrigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Retardo**](registrationtrigger-delay.md)<br/>               | Leitura/gravação<br/> | Obtém ou define o período de tempo entre quando a tarefa é registrada e quando a tarefa é iniciada.<br/>                                                                                |
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define um valor booliano que indica se o gatilho está habilitado.<br/>                                                |
| [**Limite de fim**](trigger-endboundary.md)<br/>               | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.<br/>                           |
| [**Sessão**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define o identificador do gatilho.<br/>                                                                               |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                              |
| [**Escreva**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Somente leitura<br/>  | Herdado do objeto de [**gatilho**](trigger.md) . Obtém o tipo do gatilho.<br/>                                                                                              |



 

## <a name="remarks"></a>Comentários

Ao criar seu próprio XML para uma tarefa, um gatilho de registro é especificado usando o elemento [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) do esquema de Agendador de tarefas.

Se uma tarefa com um gatilho de registro atrasado for registrada e o computador em que a tarefa está registrada for desligado ou reiniciado durante o atraso, antes da execução da tarefa, a tarefa não será executada e o atraso será perdido.

## <a name="examples"></a>Exemplos

Para obter mais informações e um exemplo de código para esse objeto de script, consulte [exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md).

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

[**Disparador**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





