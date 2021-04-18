---
description: Os threads são agendados para execução com base em sua prioridade de agendamento.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Prioridades de agendamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770130"
---
# <a name="scheduling-priorities"></a><span data-ttu-id="9a826-103">Prioridades de agendamento</span><span class="sxs-lookup"><span data-stu-id="9a826-103">Scheduling Priorities</span></span>

<span data-ttu-id="9a826-104">Os threads são agendados para execução com base em sua *prioridade de agendamento*.</span><span class="sxs-lookup"><span data-stu-id="9a826-104">Threads are scheduled to run based on their *scheduling priority*.</span></span> <span data-ttu-id="9a826-105">Cada thread recebe uma prioridade de agendamento.</span><span class="sxs-lookup"><span data-stu-id="9a826-105">Each thread is assigned a scheduling priority.</span></span> <span data-ttu-id="9a826-106">Os níveis de prioridade variam de zero (prioridade mais baixa) a 31 (prioridade mais alta).</span><span class="sxs-lookup"><span data-stu-id="9a826-106">The priority levels range from zero (lowest priority) to 31 (highest priority).</span></span> <span data-ttu-id="9a826-107">Somente o thread de página zero pode ter uma prioridade zero.</span><span class="sxs-lookup"><span data-stu-id="9a826-107">Only the zero-page thread can have a priority of zero.</span></span> <span data-ttu-id="9a826-108">(O thread de página zero é um thread do sistema responsável por zerar qualquer página livre quando não há nenhum outro thread que precise ser executado.)</span><span class="sxs-lookup"><span data-stu-id="9a826-108">(The zero-page thread is a system thread responsible for zeroing any free pages when there are no other threads that need to run.)</span></span>

<span data-ttu-id="9a826-109">O sistema trata todos os threads com a mesma prioridade igual.</span><span class="sxs-lookup"><span data-stu-id="9a826-109">The system treats all threads with the same priority as equal.</span></span> <span data-ttu-id="9a826-110">O sistema atribui frações de tempo em um modo Round Robin a todos os threads com a prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="9a826-110">The system assigns time slices in a round-robin fashion to all threads with the highest priority.</span></span> <span data-ttu-id="9a826-111">Se nenhum desses threads estiver pronto para ser executado, o sistema atribuirá fatias de tempo em um modo Round Robin a todos os threads com a próxima prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="9a826-111">If none of these threads are ready to run, the system assigns time slices in a round-robin fashion to all threads with the next highest priority.</span></span> <span data-ttu-id="9a826-112">Se um thread de prioridade mais alta se tornar disponível para execução, o sistema deixará de executar o thread de prioridade inferior (sem permitir que ele termine de usar sua fração de tempo) e atribuirá uma fatia de tempo completa ao thread de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="9a826-112">If a higher-priority thread becomes available to run, the system ceases to execute the lower-priority thread (without allowing it to finish using its time slice) and assigns a full time slice to the higher-priority thread.</span></span> <span data-ttu-id="9a826-113">Para obter mais informações, consulte [alternâncias de contexto](context-switches.md).</span><span class="sxs-lookup"><span data-stu-id="9a826-113">For more information, see [Context Switches](context-switches.md).</span></span>

<span data-ttu-id="9a826-114">A prioridade de cada thread é determinada pelos seguintes critérios:</span><span class="sxs-lookup"><span data-stu-id="9a826-114">The priority of each thread is determined by the following criteria:</span></span>

-   <span data-ttu-id="9a826-115">A classe de prioridade de seu processo</span><span class="sxs-lookup"><span data-stu-id="9a826-115">The priority class of its process</span></span>
-   <span data-ttu-id="9a826-116">O nível de prioridade do thread dentro da classe de prioridade de seu processo</span><span class="sxs-lookup"><span data-stu-id="9a826-116">The priority level of the thread within the priority class of its process</span></span>

<span data-ttu-id="9a826-117">A classe de prioridade e o nível de prioridade são combinados para formar a *prioridade base* de um thread.</span><span class="sxs-lookup"><span data-stu-id="9a826-117">The priority class and priority level are combined to form the *base priority* of a thread.</span></span> <span data-ttu-id="9a826-118">Para obter informações sobre a prioridade dinâmica de um thread, consulte [aumentos de prioridade](priority-boosts.md).</span><span class="sxs-lookup"><span data-stu-id="9a826-118">For information on the dynamic priority of a thread, see [Priority Boosts](priority-boosts.md).</span></span>

## <a name="priority-class"></a><span data-ttu-id="9a826-119">Classe de prioridade</span><span class="sxs-lookup"><span data-stu-id="9a826-119">Priority Class</span></span>

<span data-ttu-id="9a826-120">Cada processo pertence a uma das seguintes classes de prioridade:</span><span class="sxs-lookup"><span data-stu-id="9a826-120">Each process belongs to one of the following priority classes:</span></span><dl> <span data-ttu-id="9a826-121">\_classe de prioridade ociosa \_</span><span class="sxs-lookup"><span data-stu-id="9a826-121">IDLE\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="9a826-122">ABAIXO \_ da \_ classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="9a826-122">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="9a826-123">\_classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="9a826-123">NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="9a826-124">ACIMA \_ da \_ classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="9a826-124">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="9a826-125">\_classe de prioridade alta \_</span><span class="sxs-lookup"><span data-stu-id="9a826-125">HIGH\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="9a826-126">\_classe de prioridade em tempo real \_</span><span class="sxs-lookup"><span data-stu-id="9a826-126">REALTIME\_PRIORITY\_CLASS</span></span>  
</dl>

<span data-ttu-id="9a826-127">Por padrão, a classe de prioridade de um processo é a \_ classe de prioridade normal \_ .</span><span class="sxs-lookup"><span data-stu-id="9a826-127">By default, the priority class of a process is NORMAL\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="9a826-128">Use a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) para especificar a classe de prioridade de um processo filho ao criá-lo.</span><span class="sxs-lookup"><span data-stu-id="9a826-128">Use the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function to specify the priority class of a child process when you create it.</span></span> <span data-ttu-id="9a826-129">Se o processo de chamada for \_ uma \_ classe de prioridade ociosa ou abaixo \_ \_ \_ da classe de prioridade normal, o novo processo herdará essa classe.</span><span class="sxs-lookup"><span data-stu-id="9a826-129">If the calling process is IDLE\_PRIORITY\_CLASS or BELOW\_NORMAL\_PRIORITY\_CLASS, the new process will inherit this class.</span></span> <span data-ttu-id="9a826-130">Use a função [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) para determinar a classe de prioridade atual de um processo e a função [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para alterar a classe de prioridade de um processo.</span><span class="sxs-lookup"><span data-stu-id="9a826-130">Use the [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) function to determine the current priority class of a process and the [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) function to change the priority class of a process.</span></span>

<span data-ttu-id="9a826-131">Processos que monitoram o sistema, como proteções de tela ou aplicativos que atualizam periodicamente uma exibição, devem usar a \_ classe de prioridade ociosa \_ .</span><span class="sxs-lookup"><span data-stu-id="9a826-131">Processes that monitor the system, such as screen savers or applications that periodically update a display, should use IDLE\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="9a826-132">Isso impede que os threads desse processo, que não têm prioridade alta, interfiram com threads de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="9a826-132">This prevents the threads of this process, which do not have high priority, from interfering with higher priority threads.</span></span>

<span data-ttu-id="9a826-133">Use \_ \_ a classe de prioridade alta com cuidado.</span><span class="sxs-lookup"><span data-stu-id="9a826-133">Use HIGH\_PRIORITY\_CLASS with care.</span></span> <span data-ttu-id="9a826-134">Se um thread for executado no nível de prioridade mais alto para períodos estendidos, outros threads no sistema não terão tempo de processador.</span><span class="sxs-lookup"><span data-stu-id="9a826-134">If a thread runs at the highest priority level for extended periods, other threads in the system will not get processor time.</span></span> <span data-ttu-id="9a826-135">Se vários threads forem definidos com prioridade alta ao mesmo tempo, os threads perderão sua eficácia.</span><span class="sxs-lookup"><span data-stu-id="9a826-135">If several threads are set at high priority at the same time, the threads lose their effectiveness.</span></span> <span data-ttu-id="9a826-136">A classe de alta prioridade deve ser reservada para threads que devem responder a eventos de tempo crítico.</span><span class="sxs-lookup"><span data-stu-id="9a826-136">The high-priority class should be reserved for threads that must respond to time-critical events.</span></span> <span data-ttu-id="9a826-137">Se seu aplicativo executar uma tarefa que requer a classe de alta prioridade enquanto o restante de suas tarefas for de prioridade normal, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para aumentar a classe de prioridade do aplicativo temporariamente; em seguida, reduza-o após a conclusão da tarefa de tempo crítico.</span><span class="sxs-lookup"><span data-stu-id="9a826-137">If your application performs one task that requires the high-priority class while the rest of its tasks are normal priority, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) to raise the priority class of the application temporarily; then reduce it after the time-critical task has been completed.</span></span> <span data-ttu-id="9a826-138">Outra estratégia é criar um processo de alta prioridade que tenha todos os seus threads bloqueados na maior parte do tempo, despertando threads somente quando tarefas críticas forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="9a826-138">Another strategy is to create a high-priority process that has all of its threads blocked most of the time, awakening threads only when critical tasks are needed.</span></span> <span data-ttu-id="9a826-139">O ponto importante é que um thread de alta prioridade deve ser executado por um curto período e apenas quando ele tem um trabalho de tempo crítico para ser executado.</span><span class="sxs-lookup"><span data-stu-id="9a826-139">The important point is that a high-priority thread should execute for a brief time, and only when it has time-critical work to perform.</span></span>

<span data-ttu-id="9a826-140">Você quase nunca deve usar \_ a classe de prioridade em tempo real \_ , pois isso interrompe os threads do sistema que gerenciam a entrada do mouse, a entrada do teclado e a liberação de disco em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9a826-140">You should almost never use REALTIME\_PRIORITY\_CLASS, because this interrupts system threads that manage mouse input, keyboard input, and background disk flushing.</span></span> <span data-ttu-id="9a826-141">Essa classe pode ser apropriada para aplicativos que "falam" diretamente com o hardware ou que executam tarefas curtas que devem ter interrupções limitadas.</span><span class="sxs-lookup"><span data-stu-id="9a826-141">This class can be appropriate for applications that "talk" directly to hardware or that perform brief tasks that should have limited interruptions.</span></span>

## <a name="priority-level"></a><span data-ttu-id="9a826-142">Nível de prioridade</span><span class="sxs-lookup"><span data-stu-id="9a826-142">Priority Level</span></span>

<span data-ttu-id="9a826-143">A seguir estão os níveis de prioridade dentro de cada classe de prioridade:</span><span class="sxs-lookup"><span data-stu-id="9a826-143">The following are priority levels within each priority class:</span></span><dl> <span data-ttu-id="9a826-144">prioridade de THREAD \_ \_ ociosa</span><span class="sxs-lookup"><span data-stu-id="9a826-144">THREAD\_PRIORITY\_IDLE</span></span>  
<span data-ttu-id="9a826-145">\_prioridade \_ mais baixa da thread</span><span class="sxs-lookup"><span data-stu-id="9a826-145">THREAD\_PRIORITY\_LOWEST</span></span>  
<span data-ttu-id="9a826-146">prioridade de THREAD \_ \_ abaixo do \_ normal</span><span class="sxs-lookup"><span data-stu-id="9a826-146">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  
<span data-ttu-id="9a826-147">prioridade de THREAD \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="9a826-147">THREAD\_PRIORITY\_NORMAL</span></span>  
<span data-ttu-id="9a826-148">prioridade de THREAD \_ \_ acima do \_ normal</span><span class="sxs-lookup"><span data-stu-id="9a826-148">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  
<span data-ttu-id="9a826-149">prioridade de THREAD \_ \_ mais alta</span><span class="sxs-lookup"><span data-stu-id="9a826-149">THREAD\_PRIORITY\_HIGHEST</span></span>  
<span data-ttu-id="9a826-150">tempo de prioridade de THREAD \_ \_ \_ crítico</span><span class="sxs-lookup"><span data-stu-id="9a826-150">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span>  
</dl>

<span data-ttu-id="9a826-151">Todos os threads são criados usando a prioridade de THREAD \_ \_ normal.</span><span class="sxs-lookup"><span data-stu-id="9a826-151">All threads are created using THREAD\_PRIORITY\_NORMAL.</span></span> <span data-ttu-id="9a826-152">Isso significa que a prioridade de thread é a mesma que a classe de prioridade de processo.</span><span class="sxs-lookup"><span data-stu-id="9a826-152">This means that the thread priority is the same as the process priority class.</span></span> <span data-ttu-id="9a826-153">Depois de criar um thread, use a função [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) para ajustar sua prioridade em relação a outros threads no processo.</span><span class="sxs-lookup"><span data-stu-id="9a826-153">After you create a thread, use the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function to adjust its priority relative to other threads in the process.</span></span>

<span data-ttu-id="9a826-154">Uma estratégia típica é usar a prioridade de THREAD acima da prioridade \_ \_ \_ normal ou \_ de thread \_ para o thread de entrada do processo, para garantir que o aplicativo seja responsivo ao usuário.</span><span class="sxs-lookup"><span data-stu-id="9a826-154">A typical strategy is to use THREAD\_PRIORITY\_ABOVE\_NORMAL or THREAD\_PRIORITY\_HIGHEST for the process's input thread, to ensure that the application is responsive to the user.</span></span> <span data-ttu-id="9a826-155">Os threads em segundo plano, especialmente aqueles com uso intensivo de processador, podem ser definidos para prioridade de THREAD \_ \_ abaixo da \_ prioridade normal ou de thread \_ \_ mais baixa, para garantir que eles possam ser admitidos quando necessário.</span><span class="sxs-lookup"><span data-stu-id="9a826-155">Background threads, particularly those that are processor intensive, can be set to THREAD\_PRIORITY\_BELOW\_NORMAL or THREAD\_PRIORITY\_LOWEST, to ensure that they can be preempted when necessary.</span></span> <span data-ttu-id="9a826-156">No entanto, se você tiver um thread Aguardando outro thread com uma prioridade mais baixa para concluir alguma tarefa, certifique-se de bloquear a execução do thread de alta prioridade em espera.</span><span class="sxs-lookup"><span data-stu-id="9a826-156">However, if you have a thread waiting for another thread with a lower priority to complete some task, be sure to block the execution of the waiting high-priority thread.</span></span> <span data-ttu-id="9a826-157">Para fazer isso, use uma função de [espera](../sync/wait-functions.md), [seção crítica](../sync/critical-section-objects.md)ou a função de [**suspensão**](/windows/win32/api/synchapi/nf-synchapi-sleep) , [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)ou função de [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) .</span><span class="sxs-lookup"><span data-stu-id="9a826-157">To do this, use a [wait function](../sync/wait-functions.md), [critical section](../sync/critical-section-objects.md), or the [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function, [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function.</span></span> <span data-ttu-id="9a826-158">É preferível que o thread execute um loop.</span><span class="sxs-lookup"><span data-stu-id="9a826-158">This is preferable to having the thread execute a loop.</span></span> <span data-ttu-id="9a826-159">Caso contrário, o processo pode ser bloqueado, pois o thread com prioridade mais baixa nunca é agendado.</span><span class="sxs-lookup"><span data-stu-id="9a826-159">Otherwise, the process may become deadlocked, because the thread with lower priority is never scheduled.</span></span>

<span data-ttu-id="9a826-160">Para determinar o nível de prioridade atual de um thread, use a função [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) .</span><span class="sxs-lookup"><span data-stu-id="9a826-160">To determine the current priority level of a thread, use the [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) function.</span></span>

## <a name="base-priority"></a><span data-ttu-id="9a826-161">Prioridade de Base</span><span class="sxs-lookup"><span data-stu-id="9a826-161">Base Priority</span></span>

<span data-ttu-id="9a826-162">A classe de prioridade de processo e o nível de prioridade de thread são combinados para formar a prioridade base de cada thread.</span><span class="sxs-lookup"><span data-stu-id="9a826-162">The process priority class and thread priority level are combined to form the base priority of each thread.</span></span>

<span data-ttu-id="9a826-163">A tabela a seguir mostra a prioridade base para combinações de classe de prioridade de processo e valor de prioridade de thread.</span><span class="sxs-lookup"><span data-stu-id="9a826-163">The following table shows the base priority for combinations of process priority class and thread priority value.</span></span>


<table>
<tr>
<th colspan="2"><span data-ttu-id="9a826-164">Classe de prioridade de processo</span><span class="sxs-lookup"><span data-stu-id="9a826-164">Process priority class</span></span></th>
<th><span data-ttu-id="9a826-165">Nível de prioridade do thread</span><span class="sxs-lookup"><span data-stu-id="9a826-165">Thread priority level</span></span></th>
<th><span data-ttu-id="9a826-166">Prioridade básica</span><span class="sxs-lookup"><span data-stu-id="9a826-166">Base priority</span></span></th>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="9a826-167">IDLE_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="9a826-167">IDLE_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="9a826-168">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="9a826-168">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="9a826-169">1</span><span class="sxs-lookup"><span data-stu-id="9a826-169">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-170">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="9a826-170">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="9a826-171">2</span><span class="sxs-lookup"><span data-stu-id="9a826-171">2</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-172">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-172">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-173">3</span><span class="sxs-lookup"><span data-stu-id="9a826-173">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-174">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-174">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-175">4</span><span class="sxs-lookup"><span data-stu-id="9a826-175">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-176">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-176">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-177">5</span><span class="sxs-lookup"><span data-stu-id="9a826-177">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-178">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="9a826-178">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="9a826-179">6</span><span class="sxs-lookup"><span data-stu-id="9a826-179">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-180">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="9a826-180">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="9a826-181">15</span><span class="sxs-lookup"><span data-stu-id="9a826-181">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="9a826-182">BELOW_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="9a826-182">BELOW_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="9a826-183">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="9a826-183">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="9a826-184">1</span><span class="sxs-lookup"><span data-stu-id="9a826-184">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-185">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="9a826-185">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="9a826-186">4</span><span class="sxs-lookup"><span data-stu-id="9a826-186">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-187">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-187">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-188">5</span><span class="sxs-lookup"><span data-stu-id="9a826-188">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-189">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-189">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-190">6</span><span class="sxs-lookup"><span data-stu-id="9a826-190">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-191">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-191">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-192">7</span><span class="sxs-lookup"><span data-stu-id="9a826-192">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-193">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="9a826-193">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="9a826-194">8</span><span class="sxs-lookup"><span data-stu-id="9a826-194">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-195">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="9a826-195">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="9a826-196">15</span><span class="sxs-lookup"><span data-stu-id="9a826-196">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="9a826-197">NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="9a826-197">NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="9a826-198">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="9a826-198">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="9a826-199">1</span><span class="sxs-lookup"><span data-stu-id="9a826-199">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-200">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="9a826-200">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="9a826-201">6</span><span class="sxs-lookup"><span data-stu-id="9a826-201">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-202">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-202">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-203">7</span><span class="sxs-lookup"><span data-stu-id="9a826-203">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-204">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-204">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-205">8</span><span class="sxs-lookup"><span data-stu-id="9a826-205">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-206">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-206">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-207">9</span><span class="sxs-lookup"><span data-stu-id="9a826-207">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-208">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="9a826-208">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="9a826-209">10</span><span class="sxs-lookup"><span data-stu-id="9a826-209">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-210">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="9a826-210">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="9a826-211">15</span><span class="sxs-lookup"><span data-stu-id="9a826-211">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="9a826-212">ABOVE_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="9a826-212">ABOVE_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="9a826-213">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="9a826-213">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="9a826-214">1</span><span class="sxs-lookup"><span data-stu-id="9a826-214">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-215">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="9a826-215">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="9a826-216">8</span><span class="sxs-lookup"><span data-stu-id="9a826-216">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-217">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-217">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-218">9</span><span class="sxs-lookup"><span data-stu-id="9a826-218">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-219">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-219">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-220">10</span><span class="sxs-lookup"><span data-stu-id="9a826-220">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-221">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-221">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-222">11</span><span class="sxs-lookup"><span data-stu-id="9a826-222">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-223">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="9a826-223">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="9a826-224">12</span><span class="sxs-lookup"><span data-stu-id="9a826-224">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-225">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="9a826-225">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="9a826-226">15</span><span class="sxs-lookup"><span data-stu-id="9a826-226">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="9a826-227">HIGH_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="9a826-227">HIGH_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="9a826-228">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="9a826-228">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="9a826-229">1</span><span class="sxs-lookup"><span data-stu-id="9a826-229">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-230">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="9a826-230">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="9a826-231">11</span><span class="sxs-lookup"><span data-stu-id="9a826-231">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-232">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-232">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-233">12</span><span class="sxs-lookup"><span data-stu-id="9a826-233">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-234">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-234">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-235">13</span><span class="sxs-lookup"><span data-stu-id="9a826-235">13</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-236">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-236">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-237">14</span><span class="sxs-lookup"><span data-stu-id="9a826-237">14</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-238">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="9a826-238">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="9a826-239">15</span><span class="sxs-lookup"><span data-stu-id="9a826-239">15</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-240">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="9a826-240">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="9a826-241">15</span><span class="sxs-lookup"><span data-stu-id="9a826-241">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="9a826-242">REALTIME_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="9a826-242">REALTIME_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="9a826-243">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="9a826-243">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="9a826-244">16</span><span class="sxs-lookup"><span data-stu-id="9a826-244">16</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-245">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="9a826-245">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="9a826-246">22</span><span class="sxs-lookup"><span data-stu-id="9a826-246">22</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-247">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-247">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-248">23</span><span class="sxs-lookup"><span data-stu-id="9a826-248">23</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-249">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-249">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-250">24</span><span class="sxs-lookup"><span data-stu-id="9a826-250">24</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-251">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9a826-251">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="9a826-252">25</span><span class="sxs-lookup"><span data-stu-id="9a826-252">25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-253">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="9a826-253">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="9a826-254">26</span><span class="sxs-lookup"><span data-stu-id="9a826-254">26</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9a826-255">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="9a826-255">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="9a826-256">31</span><span class="sxs-lookup"><span data-stu-id="9a826-256">31</span></span></td>
</tr>
</table>

 

 

 
