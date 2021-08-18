---
title: Objeto LogonTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa quando um usuário faz logon.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- gatilho de logon Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto LogonTrigger
- Agendador de Tarefas de objeto LogonTrigger, descrito
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aed10ba9c0c792a5e4f882988ca07770c4ac568cb893b8ffac16a3a24efd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760093"
---
# <a name="logontrigger-object"></a>Objeto LogonTrigger

Objeto de script que representa um gatilho que inicia uma tarefa quando um usuário faz logon. Quando o serviço de Agendador de Tarefas é iniciado, todos os usuários conectados são enumerados e todas as tarefas registradas com gatilhos de logon que correspondem ao usuário conectado são executadas.

## <a name="members"></a>Membros

O objeto **LogonTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **LogonTrigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atrasar**](logontrigger-delay.md)<br/>                      | Leitura/gravação<br/> | Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o usuário faz logon e quando o trabalho é iniciado.<br/>                                                                              |
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define um valor booliano que indica se o gatilho está habilitado.<br/>                                                              |
| [**Limite de fim**](trigger-endboundary.md)<br/>               | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.<br/>                                         |
| [**Sessão**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define o identificador do gatilho.<br/>                                                                                             |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define um valor que indica a frequência em que a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                                            |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Somente leitura<br/>  | Herdado do objeto de [**gatilho**](trigger.md) . Obtém o tipo do gatilho.<br/>                                                                                                            |
| [**ID**](logontrigger-userid.md)<br/>                    | Leitura/gravação<br/> | Obtém ou define o identificador do usuário.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Comentários

Se você quiser que uma tarefa seja disparada quando qualquer membro de um grupo fizer logon no computador em vez de quando um usuário específico fizer logon, não atribua um valor à propriedade [**LogonTrigger. UserID**](logontrigger-userid.md) . Em vez disso, crie um gatilho de logon com uma propriedade **LogonTrigger. UserID** vazia e atribua um valor para a entidade de segurança da tarefa usando a propriedade [**principal. GroupId**](principal-groupid.md) .

Ao ler ou gravar XML para uma tarefa, um gatilho de logon é especificado usando o elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de logon (script)](logon-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Of**](trigger.md)
</dt> </dl>

 

 





