---
description: O Windows inclui os novos elementos de programação a seguir para sincronização.
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: O que há de novo na sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702ba10126d9c0eeeb85462195680b074918584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169675"
---
# <a name="whats-new-in-synchronization"></a><span data-ttu-id="38fa5-103">O que há de novo na sincronização</span><span class="sxs-lookup"><span data-stu-id="38fa5-103">What's New in Synchronization</span></span>

<span data-ttu-id="38fa5-104">O Windows inclui os novos elementos de programação a seguir para sincronização.</span><span class="sxs-lookup"><span data-stu-id="38fa5-104">Windows includes the following new programming elements for synchronization.</span></span>

## <a name="windows-8"></a><span data-ttu-id="38fa5-105">Windows 8</span><span class="sxs-lookup"><span data-stu-id="38fa5-105">Windows 8</span></span>

### <a name="new-functions"></a><span data-ttu-id="38fa5-106">Novas funções</span><span class="sxs-lookup"><span data-stu-id="38fa5-106">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="38fa5-107">**DeleteSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="38fa5-107">**DeleteSynchronizationBarrier**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="38fa5-108">Exclui uma barreira de sincronização.</span><span class="sxs-lookup"><span data-stu-id="38fa5-108">Deletes a synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-109">**EnterSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="38fa5-109">**EnterSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="38fa5-110">Faz com que o thread de chamada aguarde em uma barreira de sincronização até que o número máximo de threads tenha inserido a barreira.</span><span class="sxs-lookup"><span data-stu-id="38fa5-110">Causes the calling thread to wait at a synchronization barrier until the maximum number of threads have entered the barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-111">**GetOverlappedResultEx**</span><span class="sxs-lookup"><span data-stu-id="38fa5-111">**GetOverlappedResultEx**</span></span>](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

<span data-ttu-id="38fa5-112">Recupera os resultados de uma operação sobreposta no arquivo especificado, no pipe nomeado ou no dispositivo de comunicação dentro do intervalo de tempo limite especificado.</span><span class="sxs-lookup"><span data-stu-id="38fa5-112">Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device within the specified time-out interval.</span></span> <span data-ttu-id="38fa5-113">O thread de chamada pode executar uma espera de alerta.</span><span class="sxs-lookup"><span data-stu-id="38fa5-113">The calling thread can perform an alertable wait.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-114">**InitializeSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="38fa5-114">**InitializeSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="38fa5-115">Especifica o número máximo de threads e a contagem de rotação para uma nova barreira de sincronização.</span><span class="sxs-lookup"><span data-stu-id="38fa5-115">Specifies the maximum number of threads and spin count for a new synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-116">**WaitOnAddress**</span><span class="sxs-lookup"><span data-stu-id="38fa5-116">**WaitOnAddress**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

<span data-ttu-id="38fa5-117">Aguarda o valor no endereço especificado ser alterado.</span><span class="sxs-lookup"><span data-stu-id="38fa5-117">Waits for the value at the specified address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-118">**WakeByAddressAll**</span><span class="sxs-lookup"><span data-stu-id="38fa5-118">**WakeByAddressAll**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

<span data-ttu-id="38fa5-119">Ativa todos os threads que estão aguardando o valor de um endereço a ser alterado.</span><span class="sxs-lookup"><span data-stu-id="38fa5-119">Wakes all threads that are waiting for the value of an address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-120">**WakeByAddressSingle**</span><span class="sxs-lookup"><span data-stu-id="38fa5-120">**WakeByAddressSingle**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

<span data-ttu-id="38fa5-121">Ativa um thread que está aguardando o valor de um endereço a ser alterado.</span><span class="sxs-lookup"><span data-stu-id="38fa5-121">Wakes one thread that is waiting for the value of an address to change.</span></span>

</dd> </dl>

### <a name="new-interlocked-functions"></a><span data-ttu-id="38fa5-122">Novas funções intercadeados</span><span class="sxs-lookup"><span data-stu-id="38fa5-122">New Interlocked Functions</span></span>

<dl> <dt>

<span data-ttu-id="38fa5-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-124">Executa uma operação de adição atômica nos valores **longos** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-124">Performs an atomic addition operation on the specified **LONG** values.</span></span> <span data-ttu-id="38fa5-125">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-125">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-127">Executa uma operação de adição atômica nos valores de **LONGLONG** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-127">Performs an atomic addition operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="38fa5-128">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-128">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-130">Executa um Atomic e uma operação nos valores **longos** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-130">Performs an atomic AND operation on the specified **LONG** values.</span></span> <span data-ttu-id="38fa5-131">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-131">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-133">Executa um Atomic e uma operação nos valores de **caracteres** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-133">Performs an atomic AND operation on the specified **char** values.</span></span> <span data-ttu-id="38fa5-134">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-134">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-136">Executa uma operação atômica e com os valores **curtos** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-136">Performs an atomic AND operation on the specified **SHORT** values.</span></span> <span data-ttu-id="38fa5-137">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-137">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-139">Executa um Atomic e uma operação nos valores de **LONGLONG** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-139">Performs an atomic AND operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="38fa5-140">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-140">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-142">Testa o bit especificado do valor **LONG64** especificado e o complementa.</span><span class="sxs-lookup"><span data-stu-id="38fa5-142">Tests the specified bit of the specified **LONG64** value and complements it.</span></span> <span data-ttu-id="38fa5-143">A operação é atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-143">The operation is atomic.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-145">Testa o bit especificado do valor **longo** especificado e o define como 0.</span><span class="sxs-lookup"><span data-stu-id="38fa5-145">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="38fa5-146">A operação é atômica e é executada com a semântica de ordenação de memória de aquisição.</span><span class="sxs-lookup"><span data-stu-id="38fa5-146">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-148">Testa o bit especificado do valor **longo** especificado e o define como 0.</span><span class="sxs-lookup"><span data-stu-id="38fa5-148">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="38fa5-149">A operação é atômica e é executada usando a semântica de liberação de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-149">The operation is atomic, and it is performed using memory release semantics.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-151">Testa o bit especificado do valor **longo** especificado e o define como 1.</span><span class="sxs-lookup"><span data-stu-id="38fa5-151">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="38fa5-152">A operação é atômica e é executada com a semântica de ordenação de memória de aquisição.</span><span class="sxs-lookup"><span data-stu-id="38fa5-152">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-154">Testa o bit especificado do valor **longo** especificado e o define como 1.</span><span class="sxs-lookup"><span data-stu-id="38fa5-154">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="38fa5-155">A operação é atômica e é executada com semântica de ordenação de memória de liberação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-155">The operation is atomic, and it is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-157">Executa uma operação atômica de comparação e troca nos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-157">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="38fa5-158">A função compara dois valores de 32 bits especificados e troca com outro valor de 32 bits com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-158">The function compares two specified 32-bit values and exchanges with another 32-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="38fa5-159">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-159">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-160">**InterlockedCompareExchange16**</span><span class="sxs-lookup"><span data-stu-id="38fa5-160">**InterlockedCompareExchange16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

<span data-ttu-id="38fa5-161">Executa uma operação atômica de comparação e troca nos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-161">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="38fa5-162">A função compara dois valores de 16 bits especificados e trocas com outro valor de 16 bits com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-162">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-164">Executa uma operação atômica de comparação e troca nos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-164">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="38fa5-165">A função compara dois valores de 16 bits especificados e trocas com outro valor de 16 bits com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-165">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="38fa5-166">A operação é executada com a semântica de ordenação de memória de aquisição.</span><span class="sxs-lookup"><span data-stu-id="38fa5-166">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-168">Executa uma operação atômica de comparação e troca nos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-168">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="38fa5-169">A função compara dois valores de 16 bits especificados e trocas com outro valor de 16 bits com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-169">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="38fa5-170">O Exchange é executado com semântica de ordenação de memória de liberação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-170">The exchange is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-172">Executa uma operação atômica de comparação e troca nos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-172">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="38fa5-173">A função compara dois valores de 16 bits especificados e trocas com outro valor de 16 bits com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-173">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="38fa5-174">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-174">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-176">Executa uma operação atômica de comparação e troca nos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-176">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="38fa5-177">A função compara dois valores de 64 bits especificados e troca com outro valor de 64 bits com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-177">The function compares two specified 64-bit values and exchanges with another 64-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="38fa5-178">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-178">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-179">**InterlockedCompareExchange128**</span><span class="sxs-lookup"><span data-stu-id="38fa5-179">**InterlockedCompareExchange128**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

<span data-ttu-id="38fa5-180">Executa uma operação atômica de comparação e troca nos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-180">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="38fa5-181">A função compara dois valores de 128 bits especificados e troca com outro valor de 128 bits com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-181">The function compares two specified 128-bit values and exchanges with another 128-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-183">Executa uma operação atômica de comparação e troca nos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-183">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="38fa5-184">A função compara dois valores de ponteiro especificados e troca com outro valor de ponteiro com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-184">The function compares two specified pointer values and exchanges with another pointer value based on the outcome of the comparison.</span></span> <span data-ttu-id="38fa5-185">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-185">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-187">Decrementa (diminui em um) o valor da variável de bits de 32 especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-187">Decrements (decreases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="38fa5-188">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-188">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-189">**InterlockedDecrement16**</span><span class="sxs-lookup"><span data-stu-id="38fa5-189">**InterlockedDecrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

<span data-ttu-id="38fa5-190">Decrementa (diminui em um) o valor da variável de 16 bits especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-190">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-192">Decrementa (diminui em um) o valor da variável de 16 bits especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-192">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="38fa5-193">A operação é executada com a semântica de ordenação de memória de aquisição.</span><span class="sxs-lookup"><span data-stu-id="38fa5-193">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-195">Decrementa (diminui em um) o valor da variável de 16 bits especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-195">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="38fa5-196">A operação é executada com semântica de ordenação de memória de liberação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-196">The operation is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-198">Decrementa (diminui em um) o valor da variável de 16 bits especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-198">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="38fa5-199">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-199">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-201">Decrementa (diminui em um) o valor da variável de bits de 64 especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-201">Decrements (decreases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="38fa5-202">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-202">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-204">Define uma variável de 64 bits para o valor especificado como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-204">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="38fa5-205">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-205">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-206">**InterlockedExchange8**</span><span class="sxs-lookup"><span data-stu-id="38fa5-206">**InterlockedExchange8**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

<span data-ttu-id="38fa5-207">Define uma variável de 8 bits para o valor especificado como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-207">Sets an 8-bit variable to the specified value as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-209">Define uma variável de 16 bits para o valor especificado como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-209">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="38fa5-210">A operação é executada usando a semântica de ordenação de memória de aquisição.</span><span class="sxs-lookup"><span data-stu-id="38fa5-210">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-212">Define uma variável de 16 bits para o valor especificado como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-212">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="38fa5-213">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-213">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-215">Define uma variável de 64 bits para o valor especificado como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-215">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="38fa5-216">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-216">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-218">Troca atomicamente um par de endereços.</span><span class="sxs-lookup"><span data-stu-id="38fa5-218">Atomically exchanges a pair of addresses.</span></span> <span data-ttu-id="38fa5-219">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-219">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-221">Executa uma adição atômica de valores de 2 32 bits.</span><span class="sxs-lookup"><span data-stu-id="38fa5-221">Performs an atomic addition of two 32-bit values.</span></span> <span data-ttu-id="38fa5-222">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-222">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-224">Executa uma adição atômica de valores de 2 64 bits.</span><span class="sxs-lookup"><span data-stu-id="38fa5-224">Performs an atomic addition of two 64-bit values.</span></span> <span data-ttu-id="38fa5-225">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-225">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-227">Incrementa (aumenta em um) o valor da variável de bits de 32 especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-227">Increments (increases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="38fa5-228">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-228">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-229">**InterlockedIncrement16**</span><span class="sxs-lookup"><span data-stu-id="38fa5-229">**InterlockedIncrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

<span data-ttu-id="38fa5-230">Incrementa (aumenta em um) o valor da variável de 16 bits especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-230">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-232">Incrementa (aumenta em um) o valor da variável de 16 bits especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-232">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="38fa5-233">A operação é executada usando a semântica de ordenação de memória de aquisição.</span><span class="sxs-lookup"><span data-stu-id="38fa5-233">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-235">Incrementa (aumenta em um) o valor da variável de 16 bits especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-235">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="38fa5-236">A operação é executada usando a semântica de ordenação de memória de liberação.</span><span class="sxs-lookup"><span data-stu-id="38fa5-236">The operation is performed using release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-238">Incrementa (aumenta em um) o valor da variável de 16 bits especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-238">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="38fa5-239">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-239">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-241">Incrementa (aumenta em um) o valor da variável de bits de 64 especificada como uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="38fa5-241">Increments (increases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="38fa5-242">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-242">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-244">Executa uma operação atômica ou com os valores **longos** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-244">Performs an atomic OR operation on the specified **LONG** values.</span></span> <span data-ttu-id="38fa5-245">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-245">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-247">Executa uma operação atômica ou em valores de **caracteres** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-247">Performs an atomic OR operation on the specified **char** values.</span></span> <span data-ttu-id="38fa5-248">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-248">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-250">Executa uma operação atômica ou com os valores **curtos** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-250">Performs an atomic OR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="38fa5-251">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-251">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-253">Executa uma operação atômica ou em valores **LONGLONG** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-253">Performs an atomic OR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="38fa5-254">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-254">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-255">**InterlockedPushListSListEx**</span><span class="sxs-lookup"><span data-stu-id="38fa5-255">**InterlockedPushListSListEx**</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

<span data-ttu-id="38fa5-256">Insere uma lista vinculada individualmente na frente de outra lista vinculada individualmente.</span><span class="sxs-lookup"><span data-stu-id="38fa5-256">Inserts a singly-linked list at the front of another singly linked list.</span></span> <span data-ttu-id="38fa5-257">O acesso às listas é sincronizado em um sistema multiprocessador.</span><span class="sxs-lookup"><span data-stu-id="38fa5-257">Access to the lists is synchronized on a multiprocessor system.</span></span> <span data-ttu-id="38fa5-258">Esta versão do método não usa a Convenção de chamada [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) .</span><span class="sxs-lookup"><span data-stu-id="38fa5-258">This version of the method does not use the [\_\_fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) calling convention.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-260">Executa uma operação de XOR atômico nos valores **longos** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-260">Performs an atomic XOR operation on the specified **LONG** values.</span></span> <span data-ttu-id="38fa5-261">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-261">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-263">Executa uma operação de XOR atômico nos valores de **caracteres** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-263">Performs an atomic XOR operation on the specified **char** values.</span></span> <span data-ttu-id="38fa5-264">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-264">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-266">Executa uma operação de XOR atômico nos valores **curtos** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-266">Performs an atomic XOR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="38fa5-267">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-267">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="38fa5-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38fa5-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="38fa5-269">Executa uma operação de XOR atômico nos valores de **LONGLONG** especificados.</span><span class="sxs-lookup"><span data-stu-id="38fa5-269">Performs an atomic XOR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="38fa5-270">A operação é executada atomicamente, mas sem usar barreiras de memória.</span><span class="sxs-lookup"><span data-stu-id="38fa5-270">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> </dl>

## <a name="windows-7"></a><span data-ttu-id="38fa5-271">Windows 7</span><span class="sxs-lookup"><span data-stu-id="38fa5-271">Windows 7</span></span>

### <a name="new-functions"></a><span data-ttu-id="38fa5-272">Novas funções</span><span class="sxs-lookup"><span data-stu-id="38fa5-272">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="38fa5-273">**SetWaitableTimerEx**</span><span class="sxs-lookup"><span data-stu-id="38fa5-273">**SetWaitableTimerEx**</span></span>](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

<span data-ttu-id="38fa5-274">Ativa o temporizador waited especificado e fornece informações de contexto para o temporizador.</span><span class="sxs-lookup"><span data-stu-id="38fa5-274">Activates the specified waitable timer and provides context information for the timer.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-275">**TryAcquireSRWLockExclusive**</span><span class="sxs-lookup"><span data-stu-id="38fa5-275">**TryAcquireSRWLockExclusive**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

<span data-ttu-id="38fa5-276">Tenta adquirir um bloqueio de SRW (leitor/gravador) reduzido no modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="38fa5-276">Attempts to acquire a slim reader/writer (SRW) lock in exclusive mode.</span></span> <span data-ttu-id="38fa5-277">Se a chamada for bem-sucedida, o thread de chamada assumirá a propriedade do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="38fa5-277">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> <dt>

[<span data-ttu-id="38fa5-278">**TryAcquireSRWLockShared**</span><span class="sxs-lookup"><span data-stu-id="38fa5-278">**TryAcquireSRWLockShared**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

<span data-ttu-id="38fa5-279">Tenta adquirir um bloqueio de SRW (leitor/gravador) reduzido no modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="38fa5-279">Attempts to acquire a slim reader/writer (SRW) lock in shared mode.</span></span> <span data-ttu-id="38fa5-280">Se a chamada for bem-sucedida, o thread de chamada assumirá a propriedade do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="38fa5-280">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> </dl>

### <a name="new-structures"></a><span data-ttu-id="38fa5-281">Novas estruturas</span><span class="sxs-lookup"><span data-stu-id="38fa5-281">New Structures</span></span>

<dl> <dt>

[<span data-ttu-id="38fa5-282">**contexto do motivo \_**</span><span class="sxs-lookup"><span data-stu-id="38fa5-282">**REASON\_CONTEXT**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

<span data-ttu-id="38fa5-283">Contém informações de contexto para um temporizador ativado com [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span><span class="sxs-lookup"><span data-stu-id="38fa5-283">Contains context information for a timer activated with [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span></span>

</dd> </dl>

 

 
