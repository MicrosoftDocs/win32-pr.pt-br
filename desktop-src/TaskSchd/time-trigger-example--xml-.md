---
title: Exemplo de gatilho de tempo (XML)
description: o XML neste exemplo define uma tarefa que inicia Bloco de notas em um momento específico.
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 25c4cffb3764f96a191b1c5ad0d2999664d536f2df9be9862fa98f0335f3fe23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990805"
---
# <a name="time-trigger-example-xml"></a>Exemplo de gatilho de tempo (XML)

o XML neste exemplo define uma tarefa que inicia Bloco de notas em um momento específico.

Para registrar uma tarefa que é definida em XML, você pode usar a função [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta de linha de comando Schtasks.exe. se você usar a ferramenta de Schtasks.exe (localizada no diretório C: \\ Windows \\ System32), poderá usar o comando a seguir para registrar a tarefa: **schtasks/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a>para definir uma tarefa para iniciar Bloco de notas em uma hora específica

o exemplo de XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando Bloco de notas), um único gatilho de tempo que inicia a tarefa em um horário especificado e várias outras configurações de tarefa que afetam o modo como a tarefa é manipulada pelo Agendador de Tarefas.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe at a specific time.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after at a specified time.</Description>
    </RegistrationInfo>
    <Triggers>
        <TimeTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </TimeTrigger>
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

Veja a seguir alguns elementos importantes para ter em mente ao usar este exemplo:

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contém informações de registro sobre a tarefa.
-   [**Triggers**](taskschedulerschema-triggers-tasktype-element.md): define o gatilho que inicia a tarefa.
-   [**Timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): define o gatilho de tempo. Nesse caso, três elementos filho são usados: os limites inicial e final que especificam quando o gatilho é ativado e desativado e o limite de tempo de execução que especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho. O elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de tempo.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): define o contexto de segurança em que uma tarefa é executada.
-   [**Configurações**](taskschedulerschema-settings-tasktype-element.md): define as configurações de tarefa que o Agendador de Tarefas usa para executar a tarefa.
-   [**ações**](taskschedulerschema-actions-tasktype-element.md): define as ações que a tarefa executa (nesse caso, executando Bloco de notas).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




