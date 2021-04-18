---
title: Sobre o Agendador de Tarefas
description: O serviço Agendador de Tarefas permite que você execute tarefas automatizadas em um computador escolhido.
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- Agendador de Tarefas Agendador de Tarefas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6022546550efe32504dd0a3d12c94163e78214f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105760321"
---
# <a name="about-the-task-scheduler"></a><span data-ttu-id="5a454-104">Sobre o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5a454-104">About the Task Scheduler</span></span>

<span data-ttu-id="5a454-105">O serviço Agendador de Tarefas permite que você execute tarefas automatizadas em um computador escolhido.</span><span class="sxs-lookup"><span data-stu-id="5a454-105">The Task Scheduler service allows you to perform automated tasks on a chosen computer.</span></span> <span data-ttu-id="5a454-106">Com esse serviço, você pode agendar qualquer programa para ser executado em um horário conveniente para você ou quando ocorrer um evento específico.</span><span class="sxs-lookup"><span data-stu-id="5a454-106">With this service, you can schedule any program to run at a convenient time for you or when a specific event occurs.</span></span> <span data-ttu-id="5a454-107">O Agendador de Tarefas monitora os critérios de tempo ou de evento que você escolhe e executa a tarefa quando esses critérios são atendidos.</span><span class="sxs-lookup"><span data-stu-id="5a454-107">The Task Scheduler monitors the time or event criteria that you choose and then executes the task when those criteria are met.</span></span>

## <a name="where-task-scheduler-is-installed"></a><span data-ttu-id="5a454-108">Onde o Agendador de Tarefas está instalado</span><span class="sxs-lookup"><span data-stu-id="5a454-108">Where Task Scheduler is Installed</span></span>

<span data-ttu-id="5a454-109">O Agendador de Tarefas é instalado automaticamente com vários sistemas operacionais da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5a454-109">The Task Scheduler is automatically installed with several Microsoft operating systems.</span></span>

<span data-ttu-id="5a454-110">O Agendador de Tarefas 1,0 é instalado com os sistemas operacionais Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5a454-110">Task Scheduler 1.0 is installed with the Windows Server 2003, Windows XP, and Windows 2000 operating systems.</span></span>

<span data-ttu-id="5a454-111">O Agendador de Tarefas 2,0 é instalado com o Windows Vista e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5a454-111">Task Scheduler 2.0 is installed with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="5a454-112">A API Agendador de Tarefas 2,0 deve ser usada no desenvolvimento de aplicativos que usam o serviço Agendador de Tarefas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a454-112">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="5a454-113">Para obter mais informações, consulte [referência de Agendador de tarefas](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="5a454-113">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="5a454-114">Agendador de Tarefas é iniciado toda vez que o sistema operacional é iniciado.</span><span class="sxs-lookup"><span data-stu-id="5a454-114">Task Scheduler is started each time the operating system is started.</span></span> <span data-ttu-id="5a454-115">Ele pode ser executado por meio da GUI (interface gráfica do usuário) do Agendador de Tarefas ou por meio da API do Agendador de Tarefas descrita neste SDK.</span><span class="sxs-lookup"><span data-stu-id="5a454-115">It can be run either through the Task Scheduler graphical user interface (GUI) or through the Task Scheduler API described in this SDK.</span></span>

## <a name="information-about-tasks"></a><span data-ttu-id="5a454-116">Informações sobre tarefas</span><span class="sxs-lookup"><span data-stu-id="5a454-116">Information about Tasks</span></span>

<span data-ttu-id="5a454-117">As tarefas são o componente principal do Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="5a454-117">Tasks are the main component of the Task Scheduler.</span></span> <span data-ttu-id="5a454-118">Para obter informações sobre quais tarefas são e quais são seus componentes, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="5a454-118">For information on what tasks are and what their components are, see the following topics:</span></span>

-   [<span data-ttu-id="5a454-119">Tarefas</span><span class="sxs-lookup"><span data-stu-id="5a454-119">Tasks</span></span>](tasks.md)
-   [<span data-ttu-id="5a454-120">Ações de tarefas</span><span class="sxs-lookup"><span data-stu-id="5a454-120">Task Actions</span></span>](task-actions.md)
-   [<span data-ttu-id="5a454-121">Gatilhos de tarefa</span><span class="sxs-lookup"><span data-stu-id="5a454-121">Task Triggers</span></span>](task-triggers.md)
-   [<span data-ttu-id="5a454-122">Informações de registro da tarefa</span><span class="sxs-lookup"><span data-stu-id="5a454-122">Task Registration Information</span></span>](task-registration-information.md)
-   [<span data-ttu-id="5a454-123">Condições de ociosidade da tarefa</span><span class="sxs-lookup"><span data-stu-id="5a454-123">Task Idle Conditions</span></span>](task-idle-conditions.md)
-   [<span data-ttu-id="5a454-124">Contextos de segurança para tarefas</span><span class="sxs-lookup"><span data-stu-id="5a454-124">Security Contexts for Tasks</span></span>](security-contexts-for-running-tasks.md)
-   [<span data-ttu-id="5a454-125">Repetindo uma tarefa</span><span class="sxs-lookup"><span data-stu-id="5a454-125">Repeating A Task</span></span>](repeating-a-task.md)
-   [<span data-ttu-id="5a454-126">Manutenção automática</span><span class="sxs-lookup"><span data-stu-id="5a454-126">Automatic Maintenance</span></span>](task-maintenence.md)

<span data-ttu-id="5a454-127">Para obter mais informações e exemplos sobre como usar as interfaces de Agendador de Tarefas, os objetos de script e o XML, consulte [usando o Agendador de tarefas](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="5a454-127">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a454-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a454-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a454-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5a454-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




