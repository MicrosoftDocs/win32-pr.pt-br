---
title: Enumerando tarefas e exibindo informações de tarefas
description: A exibição de informações sobre uma tarefa, como o nome da tarefa, o estado ou a última vez que a tarefa foi executada, é feita pela enumeração por meio de tarefas em execução ou pelas tarefas em uma pasta de tarefas e pela exibição das informações desejadas.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- Enumerando tarefas Agendador de Tarefas
- Exemplos de Agendador de Tarefas Agendador de Tarefas, enumerando tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634828"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a><span data-ttu-id="9b038-105">Enumerando tarefas e exibindo informações de tarefas</span><span class="sxs-lookup"><span data-stu-id="9b038-105">Enumerating Tasks and Displaying Task Information</span></span>

<span data-ttu-id="9b038-106">A exibição de informações sobre uma tarefa, como o nome da tarefa, o estado ou a última vez que a tarefa foi executada, é feita pela enumeração por meio de tarefas em execução ou pelas tarefas em uma pasta de tarefas e pela exibição das informações desejadas.</span><span class="sxs-lookup"><span data-stu-id="9b038-106">Displaying information about a task, such as the task name, state, or the last time the task was run, is done by enumerating through running tasks or the tasks in a task folder and displaying the desired information.</span></span>

## <a name="accessing-properties-of-registered-tasks"></a><span data-ttu-id="9b038-107">Acessando Propriedades de tarefas registradas</span><span class="sxs-lookup"><span data-stu-id="9b038-107">Accessing Properties of Registered Tasks</span></span>

<span data-ttu-id="9b038-108">Para exibir o valor da propriedade de uma tarefa registrada, você deve se conectar ao serviço de Agendador de Tarefas e obter uma instância da pasta de tarefas que contém as tarefas das quais você deseja obter informações.</span><span class="sxs-lookup"><span data-stu-id="9b038-108">To display a registered task's property value, you must connect to the Task Scheduler service, and then get an instance of the task folder that contains the tasks you want information about.</span></span> <span data-ttu-id="9b038-109">Em seguida, você obtém uma coleção de todas as tarefas registradas na pasta tarefa.</span><span class="sxs-lookup"><span data-stu-id="9b038-109">You then get a collection of all the registered tasks in the task folder.</span></span> <span data-ttu-id="9b038-110">Em seguida, você enumerará cada tarefa registrada e obterá e exibirá um valor de propriedade para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="9b038-110">Then you enumerate through each registered task and get and display a property value for each task.</span></span>

## <a name="accessing-properties-of-running-tasks"></a><span data-ttu-id="9b038-111">Acessando Propriedades de tarefas em execução</span><span class="sxs-lookup"><span data-stu-id="9b038-111">Accessing Properties of Running Tasks</span></span>

<span data-ttu-id="9b038-112">Para exibir o valor da propriedade de uma tarefa em execução, você deve se conectar ao serviço de Agendador de Tarefas e obter uma coleção de todas as tarefas em execução (incluindo ou excluindo tarefas ocultas).</span><span class="sxs-lookup"><span data-stu-id="9b038-112">To display a running task's property value, you must connect to the Task Scheduler service, and then get a collection of all the running tasks (including or excluding hidden tasks).</span></span> <span data-ttu-id="9b038-113">Em seguida, você enumerará cada tarefa em execução e obterá e exibirá um valor de propriedade para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="9b038-113">Then you enumerate through each running task and get and display a property value for each task.</span></span>

## <a name="example"></a><span data-ttu-id="9b038-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9b038-114">Example</span></span>

<span data-ttu-id="9b038-115">Os exemplos a seguir enumeram tarefas e exibem o nome e o estado das tarefas:</span><span class="sxs-lookup"><span data-stu-id="9b038-115">The following examples enumerate tasks and display the name and state of the tasks:</span></span>

-   [<span data-ttu-id="9b038-116">Exibindo nomes e Estados de tarefas (scripts)</span><span class="sxs-lookup"><span data-stu-id="9b038-116">Displaying Task Names and States (Scripting)</span></span>](displaying-task-names-and-state--scripting-.md)
-   [<span data-ttu-id="9b038-117">Exibindo nomes e estado da tarefa (C++)</span><span class="sxs-lookup"><span data-stu-id="9b038-117">Displaying Task Names and State (C++)</span></span>](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a><span data-ttu-id="9b038-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b038-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b038-119">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="9b038-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




