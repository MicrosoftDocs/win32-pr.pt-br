---
title: Exemplo de gatilho semanal (XML)
description: O XML neste exemplo define uma tarefa que inicia o bloco de notas em uma base quinzenal.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104365424"
---
# <a name="weekly-trigger-example-xml"></a>Exemplo de gatilho semanal (XML)

O XML neste exemplo define uma tarefa que inicia o bloco de notas em uma base quinzenal.

Para registrar uma tarefa que é definida em XML, você pode usar a função [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta de linha de comando Schtasks.exe. Se você usar a ferramenta de Schtasks.exe (localizada no diretório C: \\ Windows \\ System32), poderá usar o comando a seguir para registrar a tarefa: **SCHTASKS/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a>Para definir uma tarefa para iniciar o bloco de notas a cada outra semana na segunda-feira às 8:00

O exemplo de XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando o bloco de notas), um único gatilho de calendário (inicia a tarefa a cada outra semana na segunda-feira às 8:00 AM) e várias outras configurações de tarefa que afetam o modo como a tarefa é manipulada pelo Agendador de Tarefas.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a bi-weekly basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-05-01T09:00:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every other week on Monday at 8:00am.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-05-02T08:00:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00</EndBoundary>
            <ScheduleByWeek>
                <WeeksInterval>2</WeeksInterval>
                <DaysOfWeek>
                    <Monday/>
                </DaysOfWeek>
            </ScheduleByWeek>
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



## <a name="taskscheduler-schema-elements"></a>Elementos do esquema TaskScheduler

Aqui estão alguns elementos importantes para ter em mente ao usar este exemplo.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Contém informações de registro sobre a tarefa.

-   [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md)

    Define o gatilho que inicia a tarefa.

-   [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Define o gatilho de calendário semanal. Nesse caso, somente quatro elementos filho são usados: os limites inicial e final que especificam quando o gatilho é ativado e desativado, o agendamento semanal e os dias da semana em que a tarefa será executada. O elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de calendário.

-   [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    Define o agendamento semanal. Nesse caso, o intervalo é definido para executar a tarefa a cada segunda semana em uma segunda-feira.

-   [**Beneficiário**](taskschedulerschema-principal-principaltype-element.md)

    Define o contexto de segurança em que uma tarefa é executada.

-   [**Configurações**](taskschedulerschema-settings-tasktype-element.md)

    Define as configurações de tarefa que Agendador de Tarefas usa para executar a tarefa.

-   [**Ações**](taskschedulerschema-actions-tasktype-element.md)

    Define as ações que a tarefa executa (nesse caso, executando o bloco de notas).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




