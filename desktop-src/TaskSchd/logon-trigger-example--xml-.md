---
title: Exemplo de gatilho de logon (XML)
description: O XML neste exemplo define uma tarefa que inicia o bloco de notas quando um usuário faz logon.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d66766ce4cae33c3526ac9d30071ff2082ddc1f2
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104365430"
---
# <a name="logon-trigger-example-xml"></a>Exemplo de gatilho de logon (XML)

O XML neste exemplo define uma tarefa que inicia o bloco de notas quando um usuário faz logon.

Para registrar uma tarefa que é definida em XML, você pode usar a função [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta de linha de comando Schtasks.exe. Se você usar a ferramenta de Schtasks.exe (localizada no diretório C: \\ Windows \\ System32), poderá usar o comando a seguir para registrar a tarefa: **SCHTASKS/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>Para definir uma tarefa para iniciar o bloco de notas na inicialização do sistema

O exemplo de XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando o bloco de notas), um único gatilho de logon que inicia a tarefa quando um usuário faz logon e várias outras configurações de tarefa que afetam o modo como a tarefa é manipulada pelo Agendador de Tarefas.

> [!Note]  
> Defina o valor do elemento **userid** como um nome de usuário no computador em que a tarefa está registrada.

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when a user logs on.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad when a specified user logs on.</Description>
    </RegistrationInfo>
    <Triggers>
        <LogonTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <UserId>DOMAIN_NAME\UserName</UserId>
        </LogonTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <GroupId>Builtin\Administrators</GroupId>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a>Elementos do esquema TaskScheduler

Veja a seguir alguns elementos importantes para ter em mente ao usar este exemplo:

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contém informações de registro sobre a tarefa.
-   [**Triggers**](taskschedulerschema-triggers-tasktype-element.md): define o gatilho que inicia a tarefa.
-   [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md): define o gatilho de logon. Nesse caso, três elementos filho são usados: os limites inicial e final que especificam quando o gatilho é ativado e desativado e o elemento [**userid**](taskschedulerschema-userid-logontriggertype-element.md) que o identificador do usuário. A tarefa é iniciada quando esse usuário faz logon no computador.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): define o contexto de segurança em que uma tarefa é executada.
-   [**Configurações**](taskschedulerschema-settings-tasktype-element.md): define as configurações de tarefa que o Agendador de tarefas usa para executar a tarefa.
-   [**Ações**](taskschedulerschema-actions-tasktype-element.md): define as ações que a tarefa executa. Nesse caso, executar o bloco de notas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




