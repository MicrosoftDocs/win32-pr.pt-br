---
title: Enumerando tarefas
description: Agendador de Tarefas 1,0 fornece um objeto de enumeração para enumerar as tarefas na pasta tarefas agendadas.
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- Enumerando tarefas Agendador de Tarefas
- Enumerando tarefas Agendador de Tarefas, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005813"
---
# <a name="enumerating-tasks"></a><span data-ttu-id="ea662-105">Enumerando tarefas</span><span class="sxs-lookup"><span data-stu-id="ea662-105">Enumerating Tasks</span></span>

<span data-ttu-id="ea662-106">Agendador de Tarefas 1,0 fornece um objeto de enumeração para enumerar as tarefas na [*pasta tarefas agendadas*](s.md).</span><span class="sxs-lookup"><span data-stu-id="ea662-106">Task Scheduler 1.0 provides an enumeration object for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>

> [!Note]  
> <span data-ttu-id="ea662-107">Para um computador com Windows Server 2003, Windows XP ou Windows 2000 para criar, monitorar ou controlar tarefas em um computador com Windows Vista, determinadas operações devem ser concluídas no computador com Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ea662-107">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, certain operations must be completed on the Windows Vista computer.</span></span> <span data-ttu-id="ea662-108">Para obter mais informações, consulte [Tarefas](tasks.md).</span><span class="sxs-lookup"><span data-stu-id="ea662-108">For more information, see [Tasks](tasks.md).</span></span>

 

## <a name="using-the-enumeration-object"></a><span data-ttu-id="ea662-109">Usando o objeto de enumeração</span><span class="sxs-lookup"><span data-stu-id="ea662-109">Using the Enumeration Object</span></span>

<span data-ttu-id="ea662-110">A interface [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) desse objeto fornece métodos para enumerar as tarefas na pasta, redefinir a sequência de enumeração para o início da lista, ignorar tarefas e fazer uma cópia do objeto de enumeração atual para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="ea662-110">The [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface of this object provides methods for enumerating the tasks in the folder, resetting the enumeration sequence to the start of the list, skipping tasks, and making a copy of the current enumeration object for later use.</span></span>

<span data-ttu-id="ea662-111">Para obter informações sobre como enumerar as tarefas na pasta tarefas agendadas, consulte [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span><span class="sxs-lookup"><span data-stu-id="ea662-111">For information about enumerating the tasks in the Scheduled tasks folder, see [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span></span>

<span data-ttu-id="ea662-112">Para obter informações sobre como redefinir a enumeração para o início da lista, consulte [**IEnumWorkItems:: Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span><span class="sxs-lookup"><span data-stu-id="ea662-112">For information about resetting the enumeration to the start of the list, see [**IEnumWorkItems::Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span></span>

<span data-ttu-id="ea662-113">Para obter informações sobre como ignorar tarefas, consulte [**IEnumWorkItems:: Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span><span class="sxs-lookup"><span data-stu-id="ea662-113">For information about skipping tasks, see [**IEnumWorkItems::Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span></span>

<span data-ttu-id="ea662-114">Para obter informações sobre como fazer uma cópia do objeto de enumeração atual, consulte [**IEnumWorkItems:: clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span><span class="sxs-lookup"><span data-stu-id="ea662-114">For information about making a copy of the current enumeration object, see [**IEnumWorkItems::Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span></span>

<span data-ttu-id="ea662-115">Para obter um exemplo de como enumerar as tarefas na pasta tarefas agendadas, consulte o [exemplo enumerando tarefas](enumerating-tasks-example.md).</span><span class="sxs-lookup"><span data-stu-id="ea662-115">For an example of enumerating the tasks in the Scheduled Tasks folder, see [Enumerating Tasks Example](enumerating-tasks-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea662-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea662-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ea662-117">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ea662-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ea662-118">Informações da tarefa Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="ea662-118">Task Scheduler 1.0 Task Information</span></span>](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




