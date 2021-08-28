---
title: Objeto Action
description: Objeto de script que fornece as propriedades comuns herdadas por todos os objetos de ação.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Objetos de ação Agendador de Tarefas
- Objeto de ação Agendador de Tarefas , descrito
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
ms.openlocfilehash: e4b9f41521f1af8b4601faafce9674277b172ad4cde3f364fc2ab7a84cfcc0df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739036"
---
# <a name="action-object"></a>Objeto Action

Objeto de script que fornece as propriedades comuns herdadas por todos os objetos de ação. Um objeto de ação é criado pelo [**método ActionCollection.Create.**](actioncollection-create.md)

## <a name="members"></a>Membros

O **objeto Action** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto Action** tem essas propriedades.



| Propriedade                               | Tipo de acesso           | Descrição                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [**Id**](action-id.md)<br/>     | Leitura/gravação<br/> | Obtém ou define o identificador da ação.<br/> |
| [**Tipo**](action-type.md)<br/> | Somente leitura<br/>  | Obtém o tipo da ação.<br/>               |



 

## <a name="remarks"></a>Comentários

Para obter informações sobre como as ações e tarefas funcionam em conjunto, consulte [Ações de tarefa](task-actions.md). A tabela a seguir contém os objetos de script que representam as ações que podem ser executadas:



| API                                            | Descrição                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**ComHandlerAction**](comhandleraction.md)   | Representa uma ação que dispara um manipulador.                   |
| [**ExecAction**](execaction.md)               | Representa uma ação que executa uma operação de linha de comando. |
| [**EmailAction**](emailaction.md)             | Representa uma ação que envia uma mensagem de email.            |
| [**ShowMessageAction**](showmessageaction.md) | Representa uma ação que mostra uma caixa de mensagem.               |



 

Ao ler ou escrever XML, as ações de uma tarefa são especificadas no elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) do esquema Agendador de Tarefas dados.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte Exemplo de gatilho de tempo [(script),](time-trigger-example--scripting-.md) exemplo de gatilho de evento [(script),](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))exemplo de gatilho diário [(script),](daily-trigger-example--scripting-.md)exemplo de gatilho de registro [(script),](registration-trigger-example--scripting-.md)exemplo de gatilho semanal [(script),](weekly-trigger-example--scripting-.md)exemplo de gatilho de [logon (script)](logon-trigger-example--scripting-.md)ou Exemplo de gatilho de [inicialização (scripts).](boot-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas script de objetos](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





