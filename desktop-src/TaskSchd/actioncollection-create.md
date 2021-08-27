---
title: Método ActionCollection. Create
description: Para scripts, o cria e adiciona uma nova ação à coleção.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Criar Agendador de Tarefas do método
- Criar método Agendador de Tarefas, objeto ActionCollection
- Objeto ActionCollection Agendador de Tarefas, método Create
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce517ae33681fcb106e83720fc5ddd7685f26f673c466e24162ce95e9ca442
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072696"
---
# <a name="actioncollectioncreate-method"></a>Método ActionCollection. Create

Para scripts, o cria e adiciona uma nova ação à coleção.

## <a name="syntax"></a>Sintaxe


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* \[ de no\]
</dt> <dd>

Esse parâmetro é definido como uma das constantes de enumeração de [**\_ \_ tipo de ação de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) a seguir.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**Tarefa \_ do AÇÃO \_ exec**</dt> <dt>0</dt> </dl>                          | A ação executa uma operação de linha de comando. Por exemplo, a ação pode executar um script, iniciar um executável ou, se o nome de um documento for fornecido, localizar seu aplicativo associado e iniciar o aplicativo com o documento.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**Tarefa \_ do \_ \_ Manipulador com de ação**</dt> <dt>5</dt> </dl>    | A ação dispara um manipulador.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**Tarefa \_ do AÇÃO \_ Enviar \_ email**</dt> <dt>6</dt> </dl>       | Essa ação envia mensagem de email.<br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**Tarefa \_ do AÇÃO \_ Mostrar \_ mensagem**</dt> <dt>7</dt> </dl> | Essa ação mostra uma caixa de mensagem.<br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um objeto de [**ação**](action.md) que representa a nova ação.

## <a name="remarks"></a>Comentários

Você não pode adicionar mais de 32 ações à coleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tipo de ação da tarefa \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Açãocollection**](actioncollection.md)
</dt> <dt>

[**Ação**](action.md)
</dt> <dt>

[**Execaction**](execaction.md)
</dt> <dt>

[**Emailaction**](emailaction.md)
</dt> <dt>

[**Permessageaction**](showmessageaction.md)
</dt> <dt>

[**Comhandleaction**](comhandleraction.md)
</dt> </dl>

 

 





