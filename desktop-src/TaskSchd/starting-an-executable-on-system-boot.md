---
title: Iniciando um executável na inicialização do sistema
description: Escrever uma tarefa que inicia um executável quando um sistema é inicializado é feito definindo um gatilho de inicialização e uma ação executável.
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- Exemplos de Agendador de Tarefas Agendador de Tarefas, gatilho de inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636594"
---
# <a name="starting-an-executable-on-system-boot"></a><span data-ttu-id="e1606-104">Iniciando um executável na inicialização do sistema</span><span class="sxs-lookup"><span data-stu-id="e1606-104">Starting an Executable on System Boot</span></span>

<span data-ttu-id="e1606-105">Escrever uma tarefa que inicia um executável quando um sistema é inicializado é feito definindo um gatilho de inicialização e uma ação executável.</span><span class="sxs-lookup"><span data-stu-id="e1606-105">Writing a task that starts an executable when a system is booted is done by defining a boot trigger and an executable action.</span></span>

## <a name="boot-trigger"></a><span data-ttu-id="e1606-106">Gatilho de inicialização</span><span class="sxs-lookup"><span data-stu-id="e1606-106">Boot Trigger</span></span>

<span data-ttu-id="e1606-107">Os gatilhos de inicialização são ativados pelo limite inicial, mas não iniciam o executável até que o sistema seja inicializado.</span><span class="sxs-lookup"><span data-stu-id="e1606-107">Boot triggers are activated by their start boundary but they do not start the executable until the system is booted.</span></span> <span data-ttu-id="e1606-108">Você também pode especificar um tempo de atraso no gatilho de inicialização que especifica a quantidade de tempo entre o momento em que o sistema é inicializado e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="e1606-108">You can also specify a delay time in the boot trigger that specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="e1606-109">Isso é definido pela propriedade [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) na interface [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) (objeto [**BootTrigger**](boottrigger.md) para scripts).</span><span class="sxs-lookup"><span data-stu-id="e1606-109">This is defined by the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property in the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) interface ([**BootTrigger**](boottrigger.md) object for scripting).</span></span>

## <a name="boot-trigger-examples"></a><span data-ttu-id="e1606-110">Exemplos de gatilho de inicialização</span><span class="sxs-lookup"><span data-stu-id="e1606-110">Boot Trigger Examples</span></span>

<span data-ttu-id="e1606-111">Os exemplos a seguir iniciam o bloco de notas depois que o sistema é inicializado:</span><span class="sxs-lookup"><span data-stu-id="e1606-111">The following examples start Notepad after the system is booted:</span></span>

-   [<span data-ttu-id="e1606-112">Exemplo de gatilho de inicialização (script)</span><span class="sxs-lookup"><span data-stu-id="e1606-112">Boot Trigger Example (Scripting)</span></span>](boot-trigger-example--scripting-.md)
-   [<span data-ttu-id="e1606-113">Exemplo de gatilho de inicialização (C++)</span><span class="sxs-lookup"><span data-stu-id="e1606-113">Boot Trigger Example (C++)</span></span>](boot-trigger-example--c---.md)
-   [<span data-ttu-id="e1606-114">Exemplo de gatilho de inicialização (XML)</span><span class="sxs-lookup"><span data-stu-id="e1606-114">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="e1606-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1606-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1606-116">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e1606-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




