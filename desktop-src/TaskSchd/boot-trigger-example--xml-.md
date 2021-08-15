---
title: Exemplo de gatilho de inicialização (XML)
description: o XML neste exemplo define uma tarefa que inicia Bloco de notas quando o sistema é inicializado.
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 75b4c9628da5ef56ec006faf9d7301661dfd0f76894ebb4f5f37cc1035d40f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860315"
---
# <a name="boot-trigger-example-xml"></a>Exemplo de gatilho de inicialização (XML)

o XML neste exemplo define uma tarefa que inicia Bloco de notas quando o sistema é inicializado.

Para registrar uma tarefa que é definida em XML, você pode usar a função [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta de linha de comando Schtasks.exe. se você usar a ferramenta de Schtasks.exe (localizada no diretório C: \\ Windows \\ System32), poderá usar o comando a seguir para registrar a tarefa: **schtasks/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>para definir uma tarefa para iniciar o Bloco de notas na inicialização do sistema

o exemplo de XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando Bloco de notas), um único gatilho de inicialização que inicia a tarefa quando o sistema é inicializado e várias outras configurações de tarefa que afetam o modo como a tarefa é manipulada pelo Agendador de Tarefas.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the system is booted.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad on system boot.</Description>
    </RegistrationInfo>
    <Triggers>
        <BootTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </BootTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
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

Aqui estão alguns elementos importantes para ter em mente ao usar este exemplo.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contém informações de registro sobre a tarefa.
-   [**Triggers**](taskschedulerschema-triggers-tasktype-element.md): define o gatilho que inicia a tarefa.
-   [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): define o gatilho de inicialização. Nesse caso, somente dois elementos filho são usados: os limites inicial e final que especificam quando o gatilho é ativado e desativado.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): define o contexto de segurança em que uma tarefa é executada.
-   [**Configurações**](taskschedulerschema-settings-tasktype-element.md): define as configurações de tarefa que o Agendador de Tarefas usa para executar a tarefa.
-   [**Ações**](taskschedulerschema-actions-tasktype-element.md): define as ações que a tarefa executa. nesse caso, a execução de Bloco de notas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




