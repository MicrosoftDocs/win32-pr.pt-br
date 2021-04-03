---
title: Iniciando um executável em um horário específico
description: Escrever uma tarefa que inicia um executável em um horário específico é feito definindo um gatilho de tempo e uma ação executável.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Exemplos de Agendador de Tarefas Agendador de Tarefas, gatilho de tempo
- Exemplos de Agendador de Tarefas Agendador de Tarefas, iniciando um executável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822810"
---
# <a name="starting-an-executable-at-a-specific-time"></a><span data-ttu-id="24711-105">Iniciando um executável em um horário específico</span><span class="sxs-lookup"><span data-stu-id="24711-105">Starting an Executable at a Specific Time</span></span>

<span data-ttu-id="24711-106">Escrever uma tarefa que inicia um executável em um horário específico é feito definindo um gatilho de tempo e uma ação executável.</span><span class="sxs-lookup"><span data-stu-id="24711-106">Writing a task that starts an executable at a specific time is done by defining a time trigger and an executable action.</span></span>

## <a name="start-boundary"></a><span data-ttu-id="24711-107">Limite de início</span><span class="sxs-lookup"><span data-stu-id="24711-107">Start Boundary</span></span>

<span data-ttu-id="24711-108">É importante observar que um gatilho de tempo é diferente de outros gatilhos baseados em tempo, pois é acionado quando o gatilho é ativado por seu limite inicial.</span><span class="sxs-lookup"><span data-stu-id="24711-108">It is important to note that a time trigger is different from other time-based triggers in that it is fired when the trigger is activated by its start boundary.</span></span> <span data-ttu-id="24711-109">Outros gatilhos baseados em tempo são ativados pelo limite inicial, mas não começam a executar suas ações (nesse caso, iniciando um executável) até que uma data agendada seja atingida.</span><span class="sxs-lookup"><span data-stu-id="24711-109">Other time-based triggers are activated by their start boundary, but they do not start performing their actions (in this case starting an executable) until a scheduled date is reached.</span></span>

## <a name="time-trigger-examples"></a><span data-ttu-id="24711-110">Exemplos de gatilho de tempo</span><span class="sxs-lookup"><span data-stu-id="24711-110">Time Trigger Examples</span></span>

<span data-ttu-id="24711-111">Os exemplos a seguir iniciam o bloco de notas 30 segundos depois que a tarefa é ativada:</span><span class="sxs-lookup"><span data-stu-id="24711-111">The following examples start Notepad 30 seconds after the task is activated:</span></span>

-   [<span data-ttu-id="24711-112">Exemplo de gatilho de tempo (C++)</span><span class="sxs-lookup"><span data-stu-id="24711-112">Time Trigger Example (C++)</span></span>](time-trigger-example--c---.md)
-   [<span data-ttu-id="24711-113">Exemplo de gatilho de tempo (script)</span><span class="sxs-lookup"><span data-stu-id="24711-113">Time Trigger Example (Scripting)</span></span>](time-trigger-example--scripting-.md)
-   [<span data-ttu-id="24711-114">Exemplo de gatilho de tempo (XML)</span><span class="sxs-lookup"><span data-stu-id="24711-114">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="24711-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24711-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24711-116">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="24711-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




