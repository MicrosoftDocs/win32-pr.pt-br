---
title: Exibindo nomes e Estados de tarefas (scripts)
description: Este exemplo de script mostra como enumerar tarefas em uma pasta de tarefas e exibir valores de propriedade de cada tarefa.
ms.assetid: 2a84a752-fbf3-4041-8b0a-304f89a49354
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7a8f22977f8cfd2d40b3c37a1cc8d7bcb5259e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364157"
---
# <a name="displaying-task-names-and-states-scripting"></a><span data-ttu-id="f8024-103">Exibindo nomes e Estados de tarefas (scripts)</span><span class="sxs-lookup"><span data-stu-id="f8024-103">Displaying Task Names and States (Scripting)</span></span>

<span data-ttu-id="f8024-104">Este exemplo de script mostra como enumerar tarefas em uma pasta de tarefas e exibir valores de propriedade de cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="f8024-104">This scripting example shows how to enumerate tasks in a task folder and display property values from each task.</span></span>

<span data-ttu-id="f8024-105">O procedimento a seguir descreve como exibir nomes de tarefas e Estados de todas as tarefas em uma pasta de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f8024-105">The following procedure describes how to display task names and states for all the tasks in a task folder.</span></span>

<span data-ttu-id="f8024-106">**Para exibir nomes de tarefas e o estado de todas as tarefas em uma pasta de tarefas**</span><span class="sxs-lookup"><span data-stu-id="f8024-106">**To display task names and state for all the tasks in a task folder**</span></span>

1.  <span data-ttu-id="f8024-107">Crie o objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f8024-107">Create the [**TaskService**](taskservice.md) object.</span></span>

    <span data-ttu-id="f8024-108">Esse objeto permite que você se conecte ao serviço de Agendador de Tarefas e acesse uma pasta de tarefas específica.</span><span class="sxs-lookup"><span data-stu-id="f8024-108">This object allows you to connect to the Task Scheduler service and access a specific task folder.</span></span>

2.  <span data-ttu-id="f8024-109">Obtenha uma pasta de tarefas que contém as tarefas sobre as quais você deseja obter informações.</span><span class="sxs-lookup"><span data-stu-id="f8024-109">Get a task folder that holds the tasks you want information about.</span></span>

    <span data-ttu-id="f8024-110">Use o método [**TaskService. GetFolder**](taskservice-getfolder.md) para obter a pasta.</span><span class="sxs-lookup"><span data-stu-id="f8024-110">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder.</span></span>

3.  <span data-ttu-id="f8024-111">Obtenha a coleção de tarefas da pasta.</span><span class="sxs-lookup"><span data-stu-id="f8024-111">Get the collection of tasks from the folder.</span></span>

    <span data-ttu-id="f8024-112">Use o método [**TaskFolder.**](taskfolder-gettasks.md) gettasks para obter a coleção de tarefas ([**RegisteredTaskCollection**](registeredtaskcollection.md)).</span><span class="sxs-lookup"><span data-stu-id="f8024-112">Use the [**TaskFolder.GetTasks**](taskfolder-gettasks.md) method to get the collection of tasks ([**RegisteredTaskCollection**](registeredtaskcollection.md)).</span></span>

4.  <span data-ttu-id="f8024-113">Obtenha o número de tarefas na coleção e Enumere-as em cada tarefa na coleção.</span><span class="sxs-lookup"><span data-stu-id="f8024-113">Get the number of tasks in the collection and enumerate through each task in the collection.</span></span>

    <span data-ttu-id="f8024-114">Use a coleção [**RegisteredTaskCollection**](registeredtaskcollection.md) de objetos para obter uma instância de objeto [**RegisteredTask**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="f8024-114">Use the [**RegisteredTaskCollection**](registeredtaskcollection.md) collection of objects to get a [**RegisteredTask**](registeredtask.md) object instance.</span></span> <span data-ttu-id="f8024-115">Cada instância conterá uma tarefa na coleção.</span><span class="sxs-lookup"><span data-stu-id="f8024-115">Each instance will contain a task in the collection.</span></span> <span data-ttu-id="f8024-116">Em seguida, você pode exibir as informações (valores de propriedade) de cada tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="f8024-116">You can then display the information (property values) from each registered task.</span></span>

<span data-ttu-id="f8024-117">O exemplo de VBScript a seguir mostra como enumerar por meio de uma coleção de tarefas registradas na pasta de tarefas raiz e exibir o nome e o estado de cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="f8024-117">The following VBScript example shows how to enumerate through a collection of registered tasks in the root task folder and display the name and state for each task.</span></span>


```VB
'---------------------------------------------------------
' This sample enumerates through the tasks on the local computer and
' displays their name and state.
'---------------------------------------------------------


' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

' Get the task folder that contains the tasks. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")
 
Dim taskCollection
Set taskCollection = rootFolder.GetTasks(0)

Dim numberOfTasks
numberOfTasks = taskCollection.Count

If numberOfTasks = 0 Then 
    Wscript.Echo "No tasks are registered."
Else
    WScript.Echo "Number of tasks registered: " & numberOfTasks
    
    Dim registeredTask
    For Each registeredTask In taskCollection
        WScript.Echo "Task Name: " & registeredTask.Name
    
        Dim taskState 
        Select Case registeredTask.State 
            Case "0"
                taskState = "Unknown"
            Case "1"
                taskState = "Disabled"
            Case "2"
                taskState = "Queued"
            Case "3"
                taskState = "Ready"
            Case "4"
                taskState = "Running"
        End Select

        WScript.Echo "    Task State: " & taskState
    Next
End If

```



## <a name="related-topics"></a><span data-ttu-id="f8024-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8024-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8024-119">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f8024-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




