---
title: objeto EventTrigger (Windows. ui. xaml. h)
description: Objeto de script que representa um gatilho que inicia uma tarefa quando ocorre um evento do sistema.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- Agendador de Tarefas de gatilho de evento, objeto
- Agendador de Tarefas de objeto EventTrigger
- Agendador de Tarefas de objeto EventTrigger, descrito
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a355106ee4fcd6756e7aaf59c19664f91204ffb1caae6ebc2dbe45575a5f2ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060161"
---
# <a name="eventtrigger-object"></a>Objeto EventTrigger

Objeto de script que representa um gatilho que inicia uma tarefa quando ocorre um evento do sistema.

## <a name="members"></a>Membros

O objeto **EventTrigger** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **EventTrigger** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atrasar**](eventtrigger-delay.md)<br/>                      | Leitura/gravação<br/> | Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o evento ocorre e quando a tarefa é iniciada.<br/>                                                                                                                                                                                                                                                            |
| [**habilitado**](trigger-enabled.md)<br/>                       | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define um valor booliano que indica se o gatilho está habilitado.<br/>                                                                                                                                                                                                                                             |
| [**Limite de fim**](trigger-endboundary.md)<br/>               | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.<br/>                                                                                                                                                                                              |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a quantidade máxima de tempo que a tarefa iniciada por esse gatilho tem permissão para ser executada.<br/>                                                                                                                                                                                                                       |
| [**Sessão**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define o identificador do gatilho.<br/>                                                                                                                                                                                                                                                                            |
| [**Repetição**](trigger-repetition.md)<br/>                 | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/>                                                                                                                                                                                                       |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Leitura/gravação<br/> | Herdado do objeto de [**gatilho**](trigger.md) . Obtém ou define a data e a hora em que o gatilho é ativado.<br/>                                                                                                                                                                                                                                                           |
| [**Assinatura**](eventtrigger-subscription.md)<br/>        | Leitura/gravação<br/> | Obtém ou define a cadeia de caracteres de consulta XPath que identifica o evento que dispara o gatilho.<br/>                                                                                                                                                                                                                                                                                         |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Somente leitura<br/>  | Herdado do objeto de [**gatilho**](trigger.md) . Obtém o tipo do gatilho.<br/>                                                                                                                                                                                                                                                                                           |
| [**ValueQueries**](eventtrigger-valuequeries.md)<br/>        | Leitura/gravação<br/> | Obtém ou define uma coleção de consultas XPath nomeadas. Cada consulta na coleção é aplicada ao último XML de evento de correspondência que é retornado da consulta de assinatura especificada na propriedade de [**assinatura**](eventtrigger-subscription.md) . O nome da consulta pode ser usado como uma variável na mensagem de uma ação de [**Exmessageaction**](showmessageaction.md) .<br/> |



 

## <a name="remarks"></a>Comentários

Um máximo de 500 tarefas com assinaturas de evento podem ser criadas. Uma assinatura de evento que consulta uma variedade de eventos pode ser usada para disparar uma tarefa que usa a mesma ação em resposta aos eventos que estão sendo registrados.

Ao ler ou gravar seu próprio XML para uma tarefa, um gatilho de evento é especificado usando o elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e um exemplo de código para esse objeto de script, consulte [exemplo de gatilho de evento (script)](/previous-versions//aa446887(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>Windows. ui. xaml. h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Of**](trigger.md)
</dt> <dt>

[**Disparador**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

