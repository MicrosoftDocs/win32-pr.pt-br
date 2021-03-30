---
title: Ações de tarefas
description: Os itens de trabalho executados por uma tarefa são chamados de ações. Uma tarefa pode ter uma única ação ou um máximo de 32 ações. Lembre-se de que quando várias ações forem especificadas, elas serão executadas em sequência.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- ações Agendador de Tarefas
- ações Agendador de Tarefas, descritas
- ações Agendador de Tarefas, executar ação
- ações Agendador de Tarefas, ação do manipulador COM
- executar Agendador de Tarefas de ação
- Ação do manipulador COM Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71003e2cea5febfab61617451f3b6ebef4a244a3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "103639757"
---
# <a name="task-actions"></a>Ações de tarefas

Os itens de trabalho executados por uma tarefa são chamados de ações. Uma tarefa pode ter uma única ação ou um máximo de 32 ações. Lembre-se de que quando várias ações forem especificadas, elas serão executadas em sequência.

## <a name="types-of-actions"></a>Tipos de ações

A tabela de ações a seguir descreve o tipo de trabalho ou ações que podem ser realizadas por uma tarefa.

| Tipo de ação      | Descrição                                                             |
|---------------------|-------------------------------------------------------------------------|
| Ação do commanipulador   | Essa ação dispara um manipulador COM.                                        |
| Ação de exec         | Essa ação executa uma operação de linha de comando, como iniciar o bloco de notas. |
| Ação de email       | Essa ação envia um email quando uma tarefa é disparada.                    |
| Mostrar ação de mensagem | Essa ação mostra uma caixa de mensagem com uma mensagem e um título especificados.     |



 

## <a name="specifying-actions"></a>Especificando ações

As ações de uma tarefa são especificadas quando a tarefa é definida e armazenada em uma coleção de ações usadas pelo serviço de Agendador de Tarefas. A tabela a seguir lista links para tópicos de referência para as APIs e elementos XML associados a ações.

Para obter mais informações e exemplos sobre como usar as interfaces de Agendador de Tarefas, os objetos de script e o XML, consulte [usando o Agendador de tarefas](using-the-task-scheduler.md).

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
| [**TaskDefinition. Actions**](taskdefinition-actions.md) | Obtém ou define as ações executadas pela tarefa.              |
| [**Açãocollection**](actioncollection.md)             | Contém as ações executadas pela tarefa.                  |
| [**Comhandleaction**](comhandleraction.md)             | Representa uma ação que dispara um manipulador.                   |
| [**Execaction**](execaction.md)                         | Representa uma ação que executa uma operação de linha de comando. |
| [**Emailaction**](emailaction.md)                       | Representa uma ação que envia uma mensagem de email.            |
| [**Permessageaction**](showmessageaction.md)           | Representa uma ação que mostra uma caixa de mensagem.               |



 

### <a name="xml-elements"></a>Elementos XML



| Elemento                                                                    | Descrição                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Ações**](taskschedulerschema-actions-tasktype-element.md)            | Define as ações executadas pela tarefa.                   |
| [**Commanipulador**](taskschedulerschema-comhandler-actiongroup-element.md)   | Representa uma ação que dispara um manipulador.                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | Representa uma ação que executa uma operação de linha de comando. |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | Representa uma ação que envia uma mensagem de email.            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | Representa uma ação que mostra uma caixa de mensagem.               |



 

## <a name="using-variables-in-action-properties"></a>Usando variáveis em Propriedades de ação

Algumas propriedades de ação do tipo **BSTR** podem conter as variáveis $ (Arg0), $ (arg1),..., $ (Arg32) em seus valores de cadeia de caracteres. Essas variáveis são substituídas pelos valores especificados no parâmetro *params* dos métodos [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) e [**IRegisteredTask:: RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ou estão contidas no gatilho de evento para a tarefa. A tabela a seguir lista as propriedades de ação que podem usar variáveis em seus valores de cadeia de caracteres.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ação</th>
<th>Propriedades</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ação do manipulador COM</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Propriedade ClassID de IComHandlerAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Propriedade data de IComHandlerAction</strong></a></li>
</ul>
<br/> Script:
<ul>
<li><a href="comhandleraction-classid.md"><strong>Comhandleaction. ClassID</strong></a></li>
<li><a href="comhandleraction-data.md"><strong>Comhandleaction. Data</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Ação de email</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Propriedade Body de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Propriedade de servidor de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Propriedade Subject de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>Para a propriedade de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Propriedade CC de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Propriedade BCC de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>Propriedade ReplyTo de IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>Da propriedade de IEmailAction</strong></a></li>
</ul>
<br/> Script:
<ul>
<li><a href="emailaction-body.md"><strong>Emailaction. Body</strong></a></li>
<li><a href="emailaction-server.md"><strong>Emailaction. Server</strong></a></li>
<li><a href="emailaction-subject.md"><strong>Emailaction. Subject</strong></a></li>
<li><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></li>
<li><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></li>
<li><a href="emailaction-bcc.md"><strong>Emailaction. Bcc</strong></a></li>
<li><a href="emailaction-replyto.md"><strong>Emailaction. ReplyTo</strong></a></li>
<li><a href="emailaction-from.md"><strong>Emailaction. from</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Ação de exec</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Propriedade Arguments de IExecAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Propriedade WorkingDirectory de IExecAction</strong></a></li>
</ul>
<br/> Script:
<ul>
<li><a href="execaction-arguments.md"><strong>Argumentos execaction.</strong></a></li>
<li><a href="execaction-workingdirectory.md"><strong>Execaction. WorkingDirectory</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Mostrar ação de mensagem</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Propriedade Title de IShowMessageAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Propriedade MessageBody de IShowMessageAction</strong></a></li>
</ul>
<br/> Script:
<ul>
<li><a href="showmessageaction-title.md"><strong>Nome da mensagem. title</strong></a></li>
<li><a href="showmessageaction-messagebody.md"><strong>MessageBody.</strong></a></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Agendador de Tarefas](about-the-task-scheduler.md)
</dt> </dl>

 

 





