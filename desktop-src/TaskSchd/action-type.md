---
title: Propriedade Action.Type
description: Para scripts, obtém o tipo da ação.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Tipo de propriedade Agendador de Tarefas
- Propriedade type Agendador de Tarefas , objeto Action
- Objeto de ação Agendador de Tarefas propriedade , Tipo
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
ms.openlocfilehash: 499c7e42b5b2578928796e6f878219e0c53612e454948d390cdb631dcaccd64c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739026"
---
# <a name="actiontype-property"></a>Propriedade Action.Type

Para scripts, obtém o tipo da ação.

## <a name="syntax"></a>Syntax


```VB
Action.Type As Integer
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade retorna uma das seguintes constantes de enumeração [**TASK \_ ACTION \_ TYPE.**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)



| Valor                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**TAREFA \_ ACTION \_ EXEC**</dt> <dt>0</dt> </dl>                          | Essa ação executa uma operação de linha de comando. Por exemplo, a ação pode executar um script, iniciar um executável ou, se o nome de um documento for fornecido, encontrar seu aplicativo associado e iniciar o aplicativo com o documento.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**TAREFA \_ MANIPULADOR \_ COM \_ AÇÃO**</dt> <dt>5</dt> </dl>    | Essa ação dispara um manipulador.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**TAREFA \_ AÇÃO \_ ENVIAR \_ EMAIL**</dt> <dt>6</dt> </dl>       | Essa ação envia uma mensagem de email.<br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**TAREFA \_ ACTION \_ SHOW \_ MESSAGE**</dt> <dt>7</dt> </dl> | Essa ação mostra uma caixa de mensagem.<br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

O tipo de ação é definido quando a ação é criada e não pode ser alterado posteriormente. Para obter informações sobre como criar uma ação, [**consulte ActionCollection.Create**](actioncollection-create.md).

Para obter informações sobre como as ações e tarefas funcionam em conjunto, consulte [Ações de tarefa](task-actions.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TIPO \_ DE AÇÃO DE \_ TAREFA**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Ação**](action.md)
</dt> </dl>

 

 





