---
description: Os aplicativos podem encontrar problemas quando executados em sistemas de multiprocessadores devido a suposições que eles fazem são válidos somente em sistemas de processador único.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Sincronização e problemas de multiprocessador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896dc240e76f1506bac2a6a2e95f101b05beca7
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/21/2021
ms.locfileid: "105755536"
---
# <a name="synchronization-and-multiprocessor-issues"></a><span data-ttu-id="59023-103">Sincronização e problemas de multiprocessador</span><span class="sxs-lookup"><span data-stu-id="59023-103">Synchronization and Multiprocessor Issues</span></span>

<span data-ttu-id="59023-104">Os aplicativos podem encontrar problemas quando executados em sistemas de multiprocessadores devido a suposições que eles fazem são válidos somente em sistemas de processador único.</span><span class="sxs-lookup"><span data-stu-id="59023-104">Applications may encounter problems when run on multiprocessor systems due to assumptions they make which are valid only on single-processor systems.</span></span>

## <a name="thread-priorities"></a><span data-ttu-id="59023-105">Prioridades do thread</span><span class="sxs-lookup"><span data-stu-id="59023-105">Thread Priorities</span></span>

<span data-ttu-id="59023-106">Considere um programa com dois threads, um com prioridade mais alta do que o outro.</span><span class="sxs-lookup"><span data-stu-id="59023-106">Consider a program with two threads, one with a higher priority than the other.</span></span> <span data-ttu-id="59023-107">Em um sistema de processador único, o thread de prioridade mais alta não cederá o controle ao thread de prioridade mais baixa, pois o Agendador dá preferência a threads de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="59023-107">On a single-processor system, the higher priority thread will not relinquish control to the lower priority thread because the scheduler gives preference to higher priority threads.</span></span> <span data-ttu-id="59023-108">Em um sistema multiprocessador, ambos os threads podem ser executados simultaneamente, cada um em seu próprio processador.</span><span class="sxs-lookup"><span data-stu-id="59023-108">On a multiprocessor system, both threads can run simultaneously, each on its own processor.</span></span>

<span data-ttu-id="59023-109">Os aplicativos devem sincronizar o acesso a estruturas de dados para evitar condições de corrida.</span><span class="sxs-lookup"><span data-stu-id="59023-109">Applications should synchronize access to data structures to avoid race conditions.</span></span> <span data-ttu-id="59023-110">O código que pressupõe que threads de prioridade mais alta sejam executados sem interferência de threads de prioridade inferior falhará em sistemas de multiprocessadores.</span><span class="sxs-lookup"><span data-stu-id="59023-110">Code that assumes that higher priority threads run without interference from lower priority threads will fail on multiprocessor systems.</span></span>

## <a name="memory-ordering"></a><span data-ttu-id="59023-111">Ordenação de memória</span><span class="sxs-lookup"><span data-stu-id="59023-111">Memory Ordering</span></span>

<span data-ttu-id="59023-112">Quando um processador grava em um local de memória, o valor é armazenado em cache para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="59023-112">When a processor writes to a memory location, the value is cached to improve performance.</span></span> <span data-ttu-id="59023-113">Da mesma forma, o processador tenta atender às solicitações de leitura do cache para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="59023-113">Similarly, the processor attempts to satisfy read requests from the cache to improve performance.</span></span> <span data-ttu-id="59023-114">Além disso, os processadores começam a buscar valores da memória antes de serem solicitados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="59023-114">Furthermore, processors begin to fetch values from memory before they are requested by the application.</span></span> <span data-ttu-id="59023-115">Isso pode acontecer como parte da execução especulativa ou devido a problemas de linha de cache.</span><span class="sxs-lookup"><span data-stu-id="59023-115">This can happen as part of speculative execution or due to cache line issues.</span></span>

<span data-ttu-id="59023-116">Os caches de CPU podem ser particionados em bancos que podem ser acessados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="59023-116">CPU caches can be partitioned into banks that can be accessed in parallel.</span></span> <span data-ttu-id="59023-117">Isso significa que as operações de memória podem ser concluídas fora de ordem.</span><span class="sxs-lookup"><span data-stu-id="59023-117">This means that memory operations can be completed out of order.</span></span> <span data-ttu-id="59023-118">Para garantir que as operações de memória sejam concluídas na ordem, a maioria dos processadores fornece instruções de barreira de memória.</span><span class="sxs-lookup"><span data-stu-id="59023-118">To ensure that memory operations are completed in order, most processors provide memory-barrier instructions.</span></span> <span data-ttu-id="59023-119">Uma *barreira de memória total* garante que as operações de leitura e gravação de memória que aparecem antes da instrução de barreira de memória sejam confirmadas na memória antes de qualquer operação de leitura e gravação de memória que apareça após a instrução de barreira de memória.</span><span class="sxs-lookup"><span data-stu-id="59023-119">A *full memory barrier* ensures that memory read and write operations that appear before the memory barrier instruction are committed to memory before any memory read and write operations that appear after the memory barrier instruction.</span></span> <span data-ttu-id="59023-120">Uma *barreira de leitura de memória* solicita apenas as operações de leitura de memória e uma *barreira de memória de gravação* solicita apenas as operações de gravação de memória.</span><span class="sxs-lookup"><span data-stu-id="59023-120">A *read memory barrier* orders only the memory read operations and a *write memory barrier* orders only the memory write operations.</span></span> <span data-ttu-id="59023-121">Essas instruções também garantem que o compilador desabilite as otimizações que poderiam reordenar as operações de memória entre as barreiras.</span><span class="sxs-lookup"><span data-stu-id="59023-121">These instructions also ensure that the compiler disables any optimizations that could reorder memory operations across the barriers.</span></span>

<span data-ttu-id="59023-122">Os processadores podem dar suporte a instruções para barreiras de memória com semântica de aquisição, liberação e isolamento.</span><span class="sxs-lookup"><span data-stu-id="59023-122">Processors can support instructions for memory barriers with acquire, release, and fence semantics.</span></span> <span data-ttu-id="59023-123">Essas semânticas descrevem a ordem na qual os resultados de uma operação são disponibilizados.</span><span class="sxs-lookup"><span data-stu-id="59023-123">These semantics describe the order in which results of an operation become available.</span></span> <span data-ttu-id="59023-124">Com a semântica de aquisição, os resultados da operação estão disponíveis antes dos resultados de qualquer operação que aparece depois dele no código.</span><span class="sxs-lookup"><span data-stu-id="59023-124">With acquire semantics, the results of the operation are available before the results of any operation that appears after it in code.</span></span> <span data-ttu-id="59023-125">Com a semântica de versão, os resultados da operação estão disponíveis após os resultados de qualquer operação que aparece antes dele no código.</span><span class="sxs-lookup"><span data-stu-id="59023-125">With release semantics, the results of the operation are available after the results of any operation that appears before it in code.</span></span> <span data-ttu-id="59023-126">A semântica de isolamento combina a semântica de aquisição e liberação.</span><span class="sxs-lookup"><span data-stu-id="59023-126">Fence semantics combine acquire and release semantics.</span></span> <span data-ttu-id="59023-127">Os resultados de uma operação com semântica de cerca estão disponíveis antes das de qualquer operação que aparece depois dele no código e após as de qualquer operação que aparece antes dela.</span><span class="sxs-lookup"><span data-stu-id="59023-127">The results of an operation with fence semantics are available before those of any operation that appears after it in code and after those of any operation that appears before it.</span></span>

<span data-ttu-id="59023-128">Em processadores x86 e x64 que dão suporte a SSE2, as instruções são **mfence** (limite de memória), **lfence** (limite de carga) e **sfence** (limite de armazenamento).</span><span class="sxs-lookup"><span data-stu-id="59023-128">On x86 and x64 processors that support SSE2, the instructions are **mfence** (memory fence), **lfence** (load fence), and **sfence** (store fence).</span></span> <span data-ttu-id="59023-129">Em processadores ARM, as instruts são **DMB** e **DSB**.</span><span class="sxs-lookup"><span data-stu-id="59023-129">On ARM processors, the instrutions are **dmb** and **dsb**.</span></span> <span data-ttu-id="59023-130">Para obter mais informações, consulte a documentação do processador.</span><span class="sxs-lookup"><span data-stu-id="59023-130">For more information, see the documentation for the processor.</span></span>

<span data-ttu-id="59023-131">As seguintes funções de sincronização usam as barreiras apropriadas para garantir a ordenação de memória:</span><span class="sxs-lookup"><span data-stu-id="59023-131">The following synchronization functions use the appropriate barriers to ensure memory ordering:</span></span>

-   <span data-ttu-id="59023-132">Funções que inserem ou deixam seções críticas</span><span class="sxs-lookup"><span data-stu-id="59023-132">Functions that enter or leave critical sections</span></span>
-   <span data-ttu-id="59023-133">Funções que adquirem ou liberam bloqueios de SRW</span><span class="sxs-lookup"><span data-stu-id="59023-133">Functions that acquire or release SRW locks</span></span>
-   <span data-ttu-id="59023-134">Início e conclusão de inicialização única</span><span class="sxs-lookup"><span data-stu-id="59023-134">One-time initialization begin and completion</span></span>
-   <span data-ttu-id="59023-135">Função **EnterSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="59023-135">**EnterSynchronizationBarrier** function</span></span>
-   <span data-ttu-id="59023-136">Funções que sinalizam objetos de sincronização</span><span class="sxs-lookup"><span data-stu-id="59023-136">Functions that signal synchronization objects</span></span>
-   <span data-ttu-id="59023-137">Funções de espera</span><span class="sxs-lookup"><span data-stu-id="59023-137">Wait functions</span></span>
-   <span data-ttu-id="59023-138">Funções interbloqueadas (exceto funções com sufixo _nolimite_ ou intrínsecos com sufixo de _\_ NF_ )</span><span class="sxs-lookup"><span data-stu-id="59023-138">Interlocked functions (except functions with _NoFence_ suffix, or intrinsics with _\_nf_ suffix)</span></span>

## <a name="fixing-a-race-condition"></a><span data-ttu-id="59023-139">Corrigindo uma condição de corrida</span><span class="sxs-lookup"><span data-stu-id="59023-139">Fixing a Race Condition</span></span>

<span data-ttu-id="59023-140">O código a seguir tem uma condição de corrida em sistemas de multiprocessadores porque o processador que é executado `CacheComputedValue` pela primeira vez pode gravar na `fValueHasBeenComputed` memória principal antes `iValue` de gravar na memória principal.</span><span class="sxs-lookup"><span data-stu-id="59023-140">The following code has a race condition on a multiprocessor systems because the processor that executes `CacheComputedValue` the first time may write `fValueHasBeenComputed` to main memory before writing `iValue` to main memory.</span></span> <span data-ttu-id="59023-141">Consequentemente, um segundo processador `FetchComputedValue` em execução ao mesmo tempo `fValueHasBeenComputed` é lido como **verdadeiro**, mas o novo valor de `iValue` ainda está no cache do primeiro processador e não foi gravado na memória.</span><span class="sxs-lookup"><span data-stu-id="59023-141">Consequently, a second processor executing `FetchComputedValue` at the same time reads `fValueHasBeenComputed` as **TRUE**, but the new value of `iValue` is still in the first processor's cache and has not been written to memory.</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="59023-142">Essa condição de corrida acima pode ser reparada usando a palavra-chave **volatile** ou a função [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) para garantir que o valor de `iValue` seja atualizado para todos os processadores antes que o valor de `fValueHasBeenComputed` seja definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="59023-142">This race condition above can be repaired by using the **volatile** keyword or the [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) function to ensure that the value of `iValue` is updated for all processors before the value of `fValueHasBeenComputed` is set to **TRUE**.</span></span>

<span data-ttu-id="59023-143">Iniciando o Visual Studio 2005, se compilado em **/volatile: MS** Mode, o compilador usa a semântica de aquisição para operações de leitura em variáveis **voláteis** e semântica de liberação para operações de gravação em variáveis **voláteis** (quando há suporte pela CPU).</span><span class="sxs-lookup"><span data-stu-id="59023-143">Starting Visual Studio 2005, if compiled in **/volatile:ms** mode, the compiler uses acquire semantics for read operations on **volatile** variables and release semantics for write operations on **volatile** variables (when supported by the CPU).</span></span> <span data-ttu-id="59023-144">Portanto, você pode corrigir o exemplo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="59023-144">Therefore, you can correct the example as follows:</span></span>

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="59023-145">Com o Visual Studio 2003, as referências **voláteis** a **volátil** são ordenadas; o compilador não solicitará o acesso à variável **volátil** novamente.</span><span class="sxs-lookup"><span data-stu-id="59023-145">With Visual Studio 2003, **volatile** to **volatile** references are ordered; the compiler will not re-order **volatile** variable access.</span></span> <span data-ttu-id="59023-146">No entanto, essas operações podem ser reordenadas pelo processador.</span><span class="sxs-lookup"><span data-stu-id="59023-146">However, these operations could be re-ordered by the processor.</span></span> <span data-ttu-id="59023-147">Portanto, você pode corrigir o exemplo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="59023-147">Therefore, you can correct the example as follows:</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a><span data-ttu-id="59023-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="59023-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59023-149">Objetos de seção crítica</span><span class="sxs-lookup"><span data-stu-id="59023-149">Critical Section Objects</span></span>](critical-section-objects.md)
</dt> <dt>

[<span data-ttu-id="59023-150">Acesso de variável interbloqueada</span><span class="sxs-lookup"><span data-stu-id="59023-150">Interlocked Variable Access</span></span>](interlocked-variable-access.md)
</dt> <dt>

[<span data-ttu-id="59023-151">Funções de espera</span><span class="sxs-lookup"><span data-stu-id="59023-151">Wait Functions</span></span>](wait-functions.md)
</dt> </dl>

 

 



