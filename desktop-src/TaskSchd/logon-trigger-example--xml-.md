---
title: Exemplo de gatilho de logon (XML)
description: O XML neste exemplo define uma tarefa que começa Bloco de notas quando um usuário faz login.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7e92216748a799c5cf8a3ae32393db2b33c680861b2a5d3249eb19c527474e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760053"
---
# <a name="logon-trigger-example-xml"></a>Exemplo de gatilho de logon (XML)

O XML neste exemplo define uma tarefa que começa Bloco de notas quando um usuário faz login.

Para registrar uma tarefa definida em XML, você pode usar a função [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta Schtasks.exe de linha de comando. Se você usar a ferramenta Schtasks.exe (localizada no diretório C: Windows System32), poderá usar o seguinte comando para registrar a \\ \\ tarefa: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>Para definir uma tarefa para iniciar o Bloco de notas na inicialização do sistema

O exemplo XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando o Bloco de notas), um único gatilho de logon que inicia a tarefa quando um usuário faz logon e várias outras configurações de tarefa que afetam como a tarefa é tratada pelo Agendador de Tarefas.

> [!Note]  
> De definir o valor do **elemento UserId** como um nome de usuário no computador no qual a tarefa está registrada.

 


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



## <a name="taskscheduler-schema-elements"></a>Elementos de esquema TaskScheduler

Veja a seguir alguns elementos importantes a ter em mente ao usar este exemplo:

-   [**RegistrationInfo:**](taskschedulerschema-registrationinfo-tasktype-element.md)contém informações de registro sobre a tarefa.
-   [**Gatilhos:**](taskschedulerschema-triggers-tasktype-element.md)define o gatilho que inicia a tarefa.
-   [**LogonTrigger:**](taskschedulerschema-logontrigger-triggergroup-element.md)define o gatilho de logon. Nesse caso, três elementos filho são usados: os limites de início e término que especificam quando o gatilho é ativado e desativado e o [**elemento UserId**](taskschedulerschema-userid-logontriggertype-element.md) que identifica o usuário. A tarefa é iniciada quando esse usuário faz logona no computador..
-   [**Entidade**](taskschedulerschema-principal-principaltype-element.md)de segurança: define o contexto de segurança no qual uma tarefa é executado.
-   [**Configurações**](taskschedulerschema-settings-tasktype-element.md): define as configurações de tarefa que o Agendador de Tarefas usa para executar a tarefa.
-   [**Ações**](taskschedulerschema-actions-tasktype-element.md): define as ações que a tarefa executa. Nesse caso, executando Bloco de notas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




