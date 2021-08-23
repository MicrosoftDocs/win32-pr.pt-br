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
ms.openlocfilehash: f6f3ec036b1d9d61c387495b48874bf742a9479ae0608f0e5c728a029df24709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002484"
---
# <a name="displaying-task-names-and-states-scripting"></a>Exibindo nomes e Estados de tarefas (scripts)

Este exemplo de script mostra como enumerar tarefas em uma pasta de tarefas e exibir valores de propriedade de cada tarefa.

O procedimento a seguir descreve como exibir nomes de tarefas e Estados de todas as tarefas em uma pasta de tarefas.

**Para exibir nomes de tarefas e o estado de todas as tarefas em uma pasta de tarefas**

1.  Crie o objeto [**TaskService**](taskservice.md) .

    Esse objeto permite que você se conecte ao serviço de Agendador de Tarefas e acesse uma pasta de tarefas específica.

2.  Obtenha uma pasta de tarefas que contém as tarefas sobre as quais você deseja obter informações.

    Use o método [**TaskService. GetFolder**](taskservice-getfolder.md) para obter a pasta.

3.  Obtenha a coleção de tarefas da pasta.

    Use o método [**TaskFolder.**](taskfolder-gettasks.md) gettasks para obter a coleção de tarefas ([**RegisteredTaskCollection**](registeredtaskcollection.md)).

4.  Obtenha o número de tarefas na coleção e Enumere-as em cada tarefa na coleção.

    Use a coleção [**RegisteredTaskCollection**](registeredtaskcollection.md) de objetos para obter uma instância de objeto [**RegisteredTask**](registeredtask.md) . Cada instância conterá uma tarefa na coleção. Em seguida, você pode exibir as informações (valores de propriedade) de cada tarefa registrada.

O exemplo de VBScript a seguir mostra como enumerar por meio de uma coleção de tarefas registradas na pasta de tarefas raiz e exibir o nome e o estado de cada tarefa.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




