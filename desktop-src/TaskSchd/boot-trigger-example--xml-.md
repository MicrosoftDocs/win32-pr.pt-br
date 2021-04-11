---
title: Exemplo de gatilho de inicialização (XML)
description: O XML neste exemplo define uma tarefa que inicia o bloco de notas quando o sistema é inicializado.
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8f9f5ea10f92979b0798b12a6225f8ba74a38ee
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104293699"
---
# <a name="boot-trigger-example-xml"></a><span data-ttu-id="64129-103">Exemplo de gatilho de inicialização (XML)</span><span class="sxs-lookup"><span data-stu-id="64129-103">Boot Trigger Example (XML)</span></span>

<span data-ttu-id="64129-104">O XML neste exemplo define uma tarefa que inicia o bloco de notas quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="64129-104">The XML in this example defines a task that starts Notepad when the system is booted.</span></span>

<span data-ttu-id="64129-105">Para registrar uma tarefa que é definida em XML, você pode usar a função [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta de linha de comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="64129-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="64129-106">Se você usar a ferramenta de Schtasks.exe (localizada no diretório C: \\ Windows \\ System32), poderá usar o comando a seguir para registrar a tarefa: **SCHTASKS/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="64129-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="64129-107">Para definir uma tarefa para iniciar o bloco de notas na inicialização do sistema</span><span class="sxs-lookup"><span data-stu-id="64129-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="64129-108">O exemplo de XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando o bloco de notas), um único gatilho de inicialização que inicia a tarefa quando o sistema é inicializado e várias outras configurações de tarefa que afetam o modo como a tarefa é manipulada pelo Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="64129-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single boot trigger that starts the task when the system is booted, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="64129-109">Elementos do esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="64129-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="64129-110">Aqui estão alguns elementos importantes para ter em mente ao usar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="64129-110">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="64129-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contém informações de registro sobre a tarefa.</span><span class="sxs-lookup"><span data-stu-id="64129-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="64129-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): define o gatilho que inicia a tarefa.</span><span class="sxs-lookup"><span data-stu-id="64129-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="64129-113">[**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): define o gatilho de inicialização.</span><span class="sxs-lookup"><span data-stu-id="64129-113">[**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): Defines the boot trigger.</span></span> <span data-ttu-id="64129-114">Nesse caso, somente dois elementos filho são usados: os limites inicial e final que especificam quando o gatilho é ativado e desativado.</span><span class="sxs-lookup"><span data-stu-id="64129-114">In this case only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="64129-115">[**Principal**](taskschedulerschema-principal-principaltype-element.md): define o contexto de segurança em que uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="64129-115">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="64129-116">[**Configurações**](taskschedulerschema-settings-tasktype-element.md): define as configurações de tarefa que o Agendador de tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="64129-116">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="64129-117">[**Ações**](taskschedulerschema-actions-tasktype-element.md): define as ações que a tarefa executa.</span><span class="sxs-lookup"><span data-stu-id="64129-117">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="64129-118">Nesse caso, executar o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="64129-118">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64129-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64129-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64129-120">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="64129-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




