---
description: Variáveis de condição são primitivos de sincronização que permitem que os threads aguardem até que ocorra uma determinada condição. Variáveis de condição são objetos de modo de usuário que não podem ser compartilhados entre processos.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Variáveis de condição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fad7d80c1c5e06fc6e496198cd298b190daba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754484"
---
# <a name="condition-variables"></a><span data-ttu-id="27154-104">Variáveis de condição</span><span class="sxs-lookup"><span data-stu-id="27154-104">Condition Variables</span></span>

<span data-ttu-id="27154-105">Variáveis de condição são primitivos de sincronização que permitem que os threads aguardem até que ocorra uma determinada condição.</span><span class="sxs-lookup"><span data-stu-id="27154-105">Condition variables are synchronization primitives that enable threads to wait until a particular condition occurs.</span></span> <span data-ttu-id="27154-106">Variáveis de condição são objetos de modo de usuário que não podem ser compartilhados entre processos.</span><span class="sxs-lookup"><span data-stu-id="27154-106">Condition variables are user-mode objects that cannot be shared across processes.</span></span>

<span data-ttu-id="27154-107">Variáveis de condição habilitam threads para liberar atomicamente um bloqueio e entrar no estado de suspensão.</span><span class="sxs-lookup"><span data-stu-id="27154-107">Condition variables enable threads to atomically release a lock and enter the sleeping state.</span></span> <span data-ttu-id="27154-108">Eles podem ser usados com seções críticas ou bloqueios de SRW (leitor/gravador) reduzidos.</span><span class="sxs-lookup"><span data-stu-id="27154-108">They can be used with critical sections or slim reader/writer (SRW) locks.</span></span> <span data-ttu-id="27154-109">Variáveis de condição dão suporte a operações que "Wake One" ou "Wake All" aguardam threads.</span><span class="sxs-lookup"><span data-stu-id="27154-109">Condition variables support operations that "wake one" or "wake all" waiting threads.</span></span> <span data-ttu-id="27154-110">Depois que um thread é ativadosdo, ele adquire novamente o bloqueio liberado quando o thread entrou no estado de suspensão.</span><span class="sxs-lookup"><span data-stu-id="27154-110">After a thread is woken, it re-acquires the lock it released when the thread entered the sleeping state.</span></span>

<span data-ttu-id="27154-111">Observe que o chamador deve alocar uma estrutura de **\_ variável de condição** e inicializá-la chamando [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (para inicializar a estrutura dinamicamente) ou atribuir a variável de **condição constante \_ \_ init** à variável de estrutura (para inicializar a estrutura estaticamente).</span><span class="sxs-lookup"><span data-stu-id="27154-111">Note that the caller must allocate a **CONDITION\_VARIABLE** structure and initialize it by either calling [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (to initialize the structure dynamically) or assign the constant **CONDITION\_VARIABLE\_INIT** to the structure variable (to initialize the structure statically).</span></span>

<span data-ttu-id="27154-112">**Windows Server 2003 e Windows XP:** Não há suporte para variáveis de condição.</span><span class="sxs-lookup"><span data-stu-id="27154-112">**Windows Server 2003 and Windows XP:** Condition variables are not supported.</span></span>

<span data-ttu-id="27154-113">A seguir estão as funções de variável de condição.</span><span class="sxs-lookup"><span data-stu-id="27154-113">The following are the condition variable functions.</span></span>



| <span data-ttu-id="27154-114">Função de variável de condição</span><span class="sxs-lookup"><span data-stu-id="27154-114">Condition variable function</span></span>                                        | <span data-ttu-id="27154-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="27154-115">Description</span></span>                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27154-116">**InitializeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="27154-116">**InitializeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | <span data-ttu-id="27154-117">Inicializa uma variável de condição.</span><span class="sxs-lookup"><span data-stu-id="27154-117">Initializes a condition variable.</span></span>                                                                              |
| [<span data-ttu-id="27154-118">**SleepConditionVariableCS**</span><span class="sxs-lookup"><span data-stu-id="27154-118">**SleepConditionVariableCS**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | <span data-ttu-id="27154-119">Dorme na variável de condição especificada e libera a seção crítica especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="27154-119">Sleeps on the specified condition variable and releases the specified critical section as an atomic operation.</span></span> |
| [<span data-ttu-id="27154-120">**SleepConditionVariableSRW**</span><span class="sxs-lookup"><span data-stu-id="27154-120">**SleepConditionVariableSRW**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | <span data-ttu-id="27154-121">Dorme na variável de condição especificada e libera o bloqueio de SRW especificado como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="27154-121">Sleeps on the specified condition variable and releases the specified SRW lock as an atomic operation.</span></span>         |
| [<span data-ttu-id="27154-122">**WakeAllConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="27154-122">**WakeAllConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | <span data-ttu-id="27154-123">Ativa todos os threads aguardando a variável de condição especificada.</span><span class="sxs-lookup"><span data-stu-id="27154-123">Wakes all threads waiting on the specified condition variable.</span></span>                                                 |
| [<span data-ttu-id="27154-124">**WakeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="27154-124">**WakeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | <span data-ttu-id="27154-125">Ativa um único thread Aguardando a variável de condição especificada.</span><span class="sxs-lookup"><span data-stu-id="27154-125">Wakes a single thread waiting on the specified condition variable.</span></span>                                             |



 

<span data-ttu-id="27154-126">O pseudocódigo a seguir demonstra o padrão de uso típico de variáveis de condição.</span><span class="sxs-lookup"><span data-stu-id="27154-126">The following pseudocode demonstrates the typical usage pattern of condition variables.</span></span>

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

<span data-ttu-id="27154-127">Por exemplo, em uma implementação de um bloqueio de leitor/gravador, a `TestPredicate` função verificaria se a solicitação de bloqueio atual é compatível com os proprietários existentes.</span><span class="sxs-lookup"><span data-stu-id="27154-127">For example, in an implementation of a reader/writer lock, the `TestPredicate` function would verify that the current lock request is compatible with the existing owners.</span></span> <span data-ttu-id="27154-128">Se for, adquira o bloqueio; caso contrário, Sleep.</span><span class="sxs-lookup"><span data-stu-id="27154-128">If it is, acquire the lock; otherwise, sleep.</span></span> <span data-ttu-id="27154-129">Para obter um exemplo mais detalhado, consulte [usando variáveis de condição](using-condition-variables.md).</span><span class="sxs-lookup"><span data-stu-id="27154-129">For a more detailed example, see [Using Condition Variables](using-condition-variables.md).</span></span>

<span data-ttu-id="27154-130">Variáveis de condição estão sujeitas a ativações falsas (aquelas não associadas a uma ativação explícita) e ativaçãos roubadas (outro thread gerencia a execução antes do thread ativados).</span><span class="sxs-lookup"><span data-stu-id="27154-130">Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread).</span></span> <span data-ttu-id="27154-131">Portanto, você deve verificar novamente um predicado (normalmente em um loop **while** ) depois que uma operação de suspensão retorna.</span><span class="sxs-lookup"><span data-stu-id="27154-131">Therefore, you should recheck a predicate (typically in a **while** loop) after a sleep operation returns.</span></span>

<span data-ttu-id="27154-132">Você pode ativar outros threads usando [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) ou [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) dentro ou fora do bloqueio associado à variável de condição.</span><span class="sxs-lookup"><span data-stu-id="27154-132">You can wake other threads using [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) or [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) either inside or outside the lock associated with the condition variable.</span></span> <span data-ttu-id="27154-133">Geralmente, é melhor liberar o bloqueio antes de ativar outros threads para reduzir o número de alternâncias de contexto.</span><span class="sxs-lookup"><span data-stu-id="27154-133">It is usually better to release the lock before waking other threads to reduce the number of context switches.</span></span>

<span data-ttu-id="27154-134">Geralmente, é conveniente usar mais de uma variável de condição com o mesmo bloqueio.</span><span class="sxs-lookup"><span data-stu-id="27154-134">It is often convenient to use more than one condition variable with the same lock.</span></span> <span data-ttu-id="27154-135">Por exemplo, uma implementação de um bloqueio de leitor/gravador pode usar uma única seção crítica, mas variáveis de condição separadas para leitores e gravadores.</span><span class="sxs-lookup"><span data-stu-id="27154-135">For example, an implementation of a reader/writer lock might use a single critical section but separate condition variables for readers and writers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27154-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27154-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27154-137">Usando variáveis de condição</span><span class="sxs-lookup"><span data-stu-id="27154-137">Using Condition Variables</span></span>](using-condition-variables.md)
</dt> </dl>

 

 
