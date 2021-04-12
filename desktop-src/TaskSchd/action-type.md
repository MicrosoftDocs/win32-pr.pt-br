---
title: Propriedade Action. Type
description: Para scripts, obtém o tipo da ação.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Agendador de Tarefas de propriedade de tipo
- Agendador de Tarefas de propriedade de tipo, objeto de ação
- Agendador de Tarefas de objeto de ação, Propriedade Type
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455511"
---
# <a name="actiontype-property"></a>Propriedade Action. Type

Para scripts, obtém o tipo da ação.

## <a name="syntax"></a>Syntax


```VB
Action.Type As Integer
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade retorna uma das constantes de enumeração de [**\_ \_ tipo de ação de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) a seguir.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**Tarefa \_ do AÇÃO \_ exec**</dt> <dt>0</dt> </dl>                          | Essa ação executa uma operação de linha de comando. Por exemplo, a ação pode executar um script, iniciar um executável ou, se o nome de um documento for fornecido, localizar seu aplicativo associado e iniciar o aplicativo com o documento.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**Tarefa \_ do \_ \_ Manipulador com de ação**</dt> <dt>5</dt> </dl>    | Essa ação dispara um manipulador.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**Tarefa \_ do AÇÃO \_ Enviar \_ email**</dt> <dt>6</dt> </dl>       | Essa ação envia uma mensagem de email.<br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**Tarefa \_ do AÇÃO \_ Mostrar \_ mensagem**</dt> <dt>7</dt> </dl> | Essa ação mostra uma caixa de mensagem.<br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

O tipo de ação é definido quando a ação é criada e não pode ser alterada posteriormente. Para obter informações sobre como criar uma ação, consulte [**ActionCollection. Create**](actioncollection-create.md).

Para obter informações sobre como as ações e tarefas funcionam em conjunto, consulte [ações da tarefa](task-actions.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tipo de ação da tarefa \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Ação**](action.md)
</dt> </dl>

 

 





