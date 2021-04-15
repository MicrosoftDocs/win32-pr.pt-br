---
title: Objeto de ação
description: Objeto de script que fornece as propriedades comuns que são herdadas por todos os objetos de ação.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Agendador de Tarefas de objeto de ação
- Agendador de Tarefas de objeto de ação, descrito
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499528"
---
# <a name="action-object"></a>Objeto de ação

Objeto de script que fornece as propriedades comuns que são herdadas por todos os objetos de ação. Um objeto Action é criado pelo método [**ActionCollection. Create**](actioncollection-create.md) .

## <a name="members"></a>Membros

O objeto de **ação** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **ação** tem essas propriedades.



| Propriedade                               | Tipo de acesso           | Descrição                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [**Sessão**](action-id.md)<br/>     | Leitura/gravação<br/> | Obtém ou define o identificador da ação.<br/> |
| [**Escreva**](action-type.md)<br/> | Somente leitura<br/>  | Obtém o tipo da ação.<br/>               |



 

## <a name="remarks"></a>Comentários

Para obter informações sobre como as ações e tarefas funcionam em conjunto, consulte [ações da tarefa](task-actions.md). A tabela a seguir contém os objetos de script que representam as ações que podem ser executadas:



| API                                            | Descrição                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**Comhandleaction**](comhandleraction.md)   | Representa uma ação que dispara um manipulador.                   |
| [**Execaction**](execaction.md)               | Representa uma ação que executa uma operação de linha de comando. |
| [**Emailaction**](emailaction.md)             | Representa uma ação que envia uma mensagem de email.            |
| [**Permessageaction**](showmessageaction.md) | Representa uma ação que mostra uma caixa de mensagem.               |



 

Ao ler ou gravar XML, as ações de uma tarefa são especificadas no elemento [**ações**](taskschedulerschema-actions-tasktype-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md) , [exemplo de gatilho de evento (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemplo de gatilho diário (script](daily-trigger-example--scripting-.md)), [exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md), exemplo de [gatilho semanal (Scripting)](weekly-trigger-example--scripting-.md), [exemplo de gatilho de logon (script)](logon-trigger-example--scripting-.md)ou [exemplo de gatilho de inicialização (script)](boot-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas objetos de script](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





