---
title: Exemplo de gatilho de tempo (XML)
description: O XML neste exemplo define uma tarefa que inicia o bloco de notas em um horário específico.
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c683c831aa3a07eeb3a41db9cd2768caeb6307a
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104293696"
---
# <a name="time-trigger-example-xml"></a><span data-ttu-id="5c4f6-103">Exemplo de gatilho de tempo (XML)</span><span class="sxs-lookup"><span data-stu-id="5c4f6-103">Time Trigger Example (XML)</span></span>

<span data-ttu-id="5c4f6-104">O XML neste exemplo define uma tarefa que inicia o bloco de notas em um horário específico.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-104">The XML in this example defines a task that starts Notepad at a specific time.</span></span>

<span data-ttu-id="5c4f6-105">Para registrar uma tarefa que é definida em XML, você pode usar a função [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta de linha de comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="5c4f6-106">Se você usar a ferramenta de Schtasks.exe (localizada no diretório C: \\ Windows \\ System32), poderá usar o comando a seguir para registrar a tarefa: **SCHTASKS/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="5c4f6-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a><span data-ttu-id="5c4f6-107">Para definir uma tarefa para iniciar o bloco de notas em um horário específico</span><span class="sxs-lookup"><span data-stu-id="5c4f6-107">To define a task to start Notepad at a specific time</span></span>

<span data-ttu-id="5c4f6-108">O exemplo de XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando o bloco de notas), um único gatilho de tempo que inicia a tarefa em um horário especificado e várias outras configurações de tarefa que afetam o modo como a tarefa é manipulada pelo Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single time trigger that starts the task at a specified time, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="5c4f6-109">Elementos do esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="5c4f6-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="5c4f6-110">Veja a seguir alguns elementos importantes para ter em mente ao usar este exemplo:</span><span class="sxs-lookup"><span data-stu-id="5c4f6-110">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="5c4f6-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contém informações de registro sobre a tarefa.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="5c4f6-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): define o gatilho que inicia a tarefa.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="5c4f6-113">[**Timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): define o gatilho de tempo.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-113">[**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): Defines the time trigger.</span></span> <span data-ttu-id="5c4f6-114">Nesse caso, três elementos filho são usados: os limites inicial e final que especificam quando o gatilho é ativado e desativado e o limite de tempo de execução que especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-114">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the execution time limit that specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="5c4f6-115">O elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de tempo.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-115">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time triggers.</span></span>
-   <span data-ttu-id="5c4f6-116">[**Principal**](taskschedulerschema-principal-principaltype-element.md): define o contexto de segurança em que uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-116">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="5c4f6-117">[**Configurações**](taskschedulerschema-settings-tasktype-element.md): define as configurações de tarefa que o Agendador de tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-117">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="5c4f6-118">[**Ações**](taskschedulerschema-actions-tasktype-element.md): define as ações que a tarefa executa (nesse caso, executando o bloco de notas).</span><span class="sxs-lookup"><span data-stu-id="5c4f6-118">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions that the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c4f6-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c4f6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c4f6-120">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5c4f6-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




