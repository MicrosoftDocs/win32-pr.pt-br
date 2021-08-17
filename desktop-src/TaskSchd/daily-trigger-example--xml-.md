---
title: Exemplo de gatilho diário (XML)
description: O XML neste exemplo define uma tarefa que começa a Bloco de notas às 8h todos os dias.
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cd98ada9a69f694d59262682317b7e5be91509b4862f8b896e22b7b0deac2167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139499"
---
# <a name="daily-trigger-example-xml"></a>Exemplo de gatilho diário (XML)

O XML neste exemplo define uma tarefa que começa Bloco de notas às 8h todos os dias. O exemplo também mostra como definir um padrão de repetição para o gatilho repetir a tarefa.

Para registrar uma tarefa definida em XML, você pode usar a função [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta Schtasks.exe de linha de comando. Se você usar a ferramenta Schtasks.exe (localizada no diretório C: Windows System32), poderá usar o seguinte comando para registrar a \\ \\ tarefa: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a>Para definir uma tarefa para iniciar Bloco de notas todos os dias às 8h

O exemplo XML a seguir mostra como definir uma tarefa com uma única ação de execução (a partir do Bloco de notas), um único gatilho de calendário (inicia a tarefa todos os dias às 8h) e várias outras configurações de tarefa que afetam como a tarefa é tratada pelo Agendador de Tarefas.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a daily basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every day.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Repetition>
                <Interval>PT1M</Interval>
                <Duration>PT4M</Duration>
            </Repetition>
            <ScheduleByDay>
                <DaysInterval>1</DaysInterval>
            </ScheduleByDay>
        </CalendarTrigger>
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



## <a name="taskscheduler-schema-elements"></a>Elementos de esquema TaskScheduler

Aqui estão alguns elementos importantes a ter em mente ao usar este exemplo.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Contém informações de registro sobre a tarefa.

-   [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md)

    Define o gatilho que inicia a tarefa.

-   [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Define o gatilho de calendário diário. Nesse caso, quatro elementos filho são usados: os limites de início e término que especificam quando o gatilho é ativado e desativado, o agendamento diário e o padrão de repetição para a tarefa. O [**elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de calendário.

-   [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    Define a agenda diária. Nesse caso, o intervalo é definido para executar a tarefa todos os dias.

-   [**Entidade**](taskschedulerschema-principal-principaltype-element.md)de segurança: define o contexto de segurança no qual uma tarefa é executado.
-   [**Configurações**](taskschedulerschema-settings-tasktype-element.md)

    Define as configurações de tarefa que Agendador de Tarefas usa para executar a tarefa.

-   [**Ações**](taskschedulerschema-actions-tasktype-element.md)

    Define as ações que a tarefa executa (nesse caso, executando Bloco de notas).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




