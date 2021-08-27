---
title: Ações de tarefa
description: Os itens de trabalho executados por uma tarefa são chamados de ações. Uma tarefa pode ter uma única ação ou um máximo de 32 ações. Esteja ciente de que quando várias ações são especificadas, elas são executadas sequencialmente.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- ações Agendador de Tarefas
- ações Agendador de Tarefas , descrito
- ações Agendador de Tarefas , executar ação
- ações Agendador de Tarefas , ação do manipulador COM
- execute action Agendador de Tarefas
- Ação do manipulador COM Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a7cc4a0e3ecbd4d55e4731379287f2cf4fd660
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470491"
---
# <a name="task-actions"></a>Ações de tarefa

Os itens de trabalho executados por uma tarefa são chamados de ações. Uma tarefa pode ter uma única ação ou um máximo de 32 ações. Esteja ciente de que quando várias ações são especificadas, elas são executadas sequencialmente.

## <a name="types-of-actions"></a>Tipos de ações

A tabela de ações a seguir descreve o tipo de trabalho ou ações que podem ser realizadas por uma tarefa.

| Tipo de ação      | Descrição                                                             |
|---------------------|-------------------------------------------------------------------------|
| Ação comHandler   | Essa ação dispara um manipulador COM.                                        |
| Ação exec         | Essa ação executa uma operação de linha de comando, como iniciar Bloco de notas. |
| Ação de email       | Essa ação envia um email quando uma tarefa é disparada.                    |
| Mostrar Ação de Mensagem | Essa ação mostra uma caixa de mensagem com uma mensagem e um título especificados.     |



 

## <a name="specifying-actions"></a>Especificando ações

As ações de uma tarefa são especificadas quando a tarefa é definida e armazenada em uma coleção de ações usadas pelo Agendador de Tarefas serviço. A tabela a seguir lista links para tópicos de referência para as APIs e elementos XML associados a ações.

Para obter mais informações e exemplos sobre como usar as interfaces Agendador de Tarefas, objetos de script e XML, consulte Usando o [Agendador de Tarefas](using-the-task-scheduler.md).

### <a name="interface-apis-for-c-development"></a>APIs de interface para desenvolvimento em C++



| API                                                                    | Descrição                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Propriedade Actions de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | Obtém ou define as ações executadas pela tarefa.              |
| [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | Contém as ações executadas pela tarefa.                  |
| [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | Representa uma ação que dispara um manipulador.                   |
| [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | Representa uma ação que executa uma operação de linha de comando. |
| [**IEmailAction**](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | Representa uma ação que envia uma mensagem de email.            |
| [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | Representa uma ação que mostra uma caixa de mensagem.               |



 

### <a name="scripting-object-apis-for-scripting-development"></a>APIs de objeto de script para desenvolvimento de scripts



| API                                                      | Descrição                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**TaskDefinition.Actions**](taskdefinition-actions.md) | Obtém ou define as ações executadas pela tarefa.              |
| [**Actioncollection**](actioncollection.md)             | Contém as ações executadas pela tarefa.                  |
| [**ComHandlerAction**](comhandleraction.md)             | Representa uma ação que dispara um manipulador.                   |
| [**ExecAction**](execaction.md)                         | Representa uma ação que executa uma operação de linha de comando. |
| [**EmailAction**](emailaction.md)                       | Representa uma ação que envia uma mensagem de email.            |
| [**ShowMessageAction**](showmessageaction.md)           | Representa uma ação que mostra uma caixa de mensagem.               |



 

### <a name="xml-elements"></a>Elementos XML



| Elemento                                                                    | Descrição                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Ações**](taskschedulerschema-actions-tasktype-element.md)            | Define as ações executadas pela tarefa.                   |
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | Representa uma ação que dispara um manipulador.                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | Representa uma ação que executa uma operação de linha de comando. |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | Representa uma ação que envia uma mensagem de email.            |
| [**Showmessage**](taskschedulerschema-showmessage-actiongroup-element.md) | Representa uma ação que mostra uma caixa de mensagem.               |



 

## <a name="using-variables-in-action-properties"></a>Usando variáveis em propriedades de ação

Algumas propriedades de ação do tipo **BSTR** podem conter variáveis $(Arg0), $(Arg1), ..., $(Arg32) em seus valores de cadeia de caracteres. Essas variáveis são substituídas pelos valores especificados no parâmetro *params* dos métodos [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) e [**IRegisteredTask::RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ou estão contidas no gatilho de evento para a tarefa. A tabela a seguir lista as propriedades de ação que podem usar variáveis em seus valores de cadeia de caracteres.


| Ação | Propriedades | 
|--------|------------|
| Ação do manipulador COM | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Propriedade ClassId de IComHandlerAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Propriedade Data de IComHandlerAction</strong></a></li></ul><br /> Script:<ul><li><a href="comhandleraction-classid.md"><strong>ComHandlerAction.ClassId</strong></a></li><li><a href="comhandleraction-data.md"><strong>ComHandlerAction.Data</strong></a></li></ul><br /> | 
| Ação de email | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Propriedade Body de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Propriedade Server de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Propriedade Subject de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>Para a propriedade de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Propriedade Cc de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Propriedade Bcc de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>Propriedade ReplyTo de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>Da propriedade de IEmailAction</strong></a></li></ul><br /> Script:<ul><li><a href="emailaction-body.md"><strong>EmailAction.Body</strong></a></li><li><a href="emailaction-server.md"><strong>EmailAction.Server</strong></a></li><li><a href="emailaction-subject.md"><strong>EmailAction.Subject</strong></a></li><li><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></li><li><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></li><li><a href="emailaction-bcc.md"><strong>Emailaction. Bcc</strong></a></li><li><a href="emailaction-replyto.md"><strong>Emailaction. ReplyTo</strong></a></li><li><a href="emailaction-from.md"><strong>Emailaction. from</strong></a></li></ul><br /> | 
| Ação de exec | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Propriedade Arguments de IExecAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Propriedade WorkingDirectory de IExecAction</strong></a></li></ul><br /> Script:<ul><li><a href="execaction-arguments.md"><strong>Argumentos execaction.</strong></a></li><li><a href="execaction-workingdirectory.md"><strong>Execaction. WorkingDirectory</strong></a></li></ul><br /> | 
| Mostrar ação de mensagem | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Propriedade Title de IShowMessageAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Propriedade MessageBody de IShowMessageAction</strong></a></li></ul><br /> Script:<ul><li><a href="showmessageaction-title.md"><strong>Nome da mensagem. title</strong></a></li><li><a href="showmessageaction-messagebody.md"><strong>MessageBody.</strong></a></li></ul><br /> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Agendador de Tarefas](about-the-task-scheduler.md)
</dt> </dl>

 

 





