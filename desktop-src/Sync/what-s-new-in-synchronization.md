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
# <a name="whats-new-in-synchronization"></a>O que há de novo na sincronização

O Windows inclui os novos elementos de programação a seguir para sincronização.

## <a name="windows-8"></a>Windows 8

### <a name="new-functions"></a>Novas funções

<dl> <dt>

[**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

Exclui uma barreira de sincronização.

</dd> <dt>

[**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

Faz com que o thread de chamada aguarde em uma barreira de sincronização até que o número máximo de threads tenha inserido a barreira.

</dd> <dt>

[**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

Recupera os resultados de uma operação sobreposta no arquivo especificado, no pipe nomeado ou no dispositivo de comunicação dentro do intervalo de tempo limite especificado. O thread de chamada pode executar uma espera de alerta.

</dd> <dt>

[**InitializeSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

Especifica o número máximo de threads e a contagem de rotação para uma nova barreira de sincronização.

</dd> <dt>

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

Aguarda o valor no endereço especificado ser alterado.

</dd> <dt>

[**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

Ativa todos os threads que estão aguardando o valor de um endereço a ser alterado.

</dd> <dt>

[**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

Ativa um thread que está aguardando o valor de um endereço a ser alterado.

</dd> </dl>

### <a name="new-interlocked-functions"></a>Novas funções intercadeados

<dl> <dt>

[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))
</dt> <dd>

Executa uma operação de adição atômica nos valores **longos** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))
</dt> <dd>

Executa uma operação de adição atômica nos valores de **LONGLONG** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))
</dt> <dd>

Executa um Atomic e uma operação nos valores **longos** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))
</dt> <dd>

Executa um Atomic e uma operação nos valores de **caracteres** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))
</dt> <dd>

Executa uma operação atômica e com os valores **curtos** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))
</dt> <dd>

Executa um Atomic e uma operação nos valores de **LONGLONG** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))
</dt> <dd>

Testa o bit especificado do valor **LONG64** especificado e o complementa. A operação é atômica.

</dd> <dt>

[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))
</dt> <dd>

Testa o bit especificado do valor **longo** especificado e o define como 0. A operação é atômica e é executada com a semântica de ordenação de memória de aquisição.

</dd> <dt>

[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))
</dt> <dd>

Testa o bit especificado do valor **longo** especificado e o define como 0. A operação é atômica e é executada usando a semântica de liberação de memória.

</dd> <dt>

[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))
</dt> <dd>

Testa o bit especificado do valor **longo** especificado e o define como 1. A operação é atômica e é executada com a semântica de ordenação de memória de aquisição.

</dd> <dt>

[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))
</dt> <dd>

Testa o bit especificado do valor **longo** especificado e o define como 1. A operação é atômica e é executada com semântica de ordenação de memória de liberação.

</dd> <dt>

[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))
</dt> <dd>

Executa uma operação atômica de comparação e troca nos valores especificados. A função compara dois valores de 32 bits especificados e troca com outro valor de 32 bits com base no resultado da comparação. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedCompareExchange16**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

Executa uma operação atômica de comparação e troca nos valores especificados. A função compara dois valores de 16 bits especificados e trocas com outro valor de 16 bits com base no resultado da comparação.

</dd> <dt>

[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))
</dt> <dd>

Executa uma operação atômica de comparação e troca nos valores especificados. A função compara dois valores de 16 bits especificados e trocas com outro valor de 16 bits com base no resultado da comparação. A operação é executada com a semântica de ordenação de memória de aquisição.

</dd> <dt>

[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))
</dt> <dd>

Executa uma operação atômica de comparação e troca nos valores especificados. A função compara dois valores de 16 bits especificados e trocas com outro valor de 16 bits com base no resultado da comparação. O Exchange é executado com semântica de ordenação de memória de liberação.

</dd> <dt>

[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))
</dt> <dd>

Executa uma operação atômica de comparação e troca nos valores especificados. A função compara dois valores de 16 bits especificados e trocas com outro valor de 16 bits com base no resultado da comparação. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))
</dt> <dd>

Executa uma operação atômica de comparação e troca nos valores especificados. A função compara dois valores de 64 bits especificados e troca com outro valor de 64 bits com base no resultado da comparação. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedCompareExchange128**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

Executa uma operação atômica de comparação e troca nos valores especificados. A função compara dois valores de 128 bits especificados e troca com outro valor de 128 bits com base no resultado da comparação.

</dd> <dt>

[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))
</dt> <dd>

Executa uma operação atômica de comparação e troca nos valores especificados. A função compara dois valores de ponteiro especificados e troca com outro valor de ponteiro com base no resultado da comparação. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))
</dt> <dd>

Decrementa (diminui em um) o valor da variável de bits de 32 especificada como uma operação atômica. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedDecrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

Decrementa (diminui em um) o valor da variável de 16 bits especificada como uma operação atômica.

</dd> <dt>

[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))
</dt> <dd>

Decrementa (diminui em um) o valor da variável de 16 bits especificada como uma operação atômica. A operação é executada com a semântica de ordenação de memória de aquisição.

</dd> <dt>

[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))
</dt> <dd>

Decrementa (diminui em um) o valor da variável de 16 bits especificada como uma operação atômica. A operação é executada com semântica de ordenação de memória de liberação.

</dd> <dt>

[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))
</dt> <dd>

Decrementa (diminui em um) o valor da variável de 16 bits especificada como uma operação atômica. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))
</dt> <dd>

Decrementa (diminui em um) o valor da variável de bits de 64 especificada como uma operação atômica. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))
</dt> <dd>

Define uma variável de 64 bits para o valor especificado como uma operação atômica. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedExchange8**](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

Define uma variável de 8 bits para o valor especificado como uma operação atômica.

</dd> <dt>

[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))
</dt> <dd>

Define uma variável de 16 bits para o valor especificado como uma operação atômica. A operação é executada usando a semântica de ordenação de memória de aquisição.

</dd> <dt>

[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))
</dt> <dd>

Define uma variável de 16 bits para o valor especificado como uma operação atômica. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))
</dt> <dd>

Define uma variável de 64 bits para o valor especificado como uma operação atômica. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))
</dt> <dd>

Troca atomicamente um par de endereços. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))
</dt> <dd>

Executa uma adição atômica de valores de 2 32 bits. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))
</dt> <dd>

Executa uma adição atômica de valores de 2 64 bits. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))
</dt> <dd>

Incrementa (aumenta em um) o valor da variável de bits de 32 especificada como uma operação atômica. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedIncrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

Incrementa (aumenta em um) o valor da variável de 16 bits especificada como uma operação atômica.

</dd> <dt>

[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))
</dt> <dd>

Incrementa (aumenta em um) o valor da variável de 16 bits especificada como uma operação atômica. A operação é executada usando a semântica de ordenação de memória de aquisição.

</dd> <dt>

[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))
</dt> <dd>

Incrementa (aumenta em um) o valor da variável de 16 bits especificada como uma operação atômica. A operação é executada usando a semântica de ordenação de memória de liberação.

</dd> <dt>

[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))
</dt> <dd>

Incrementa (aumenta em um) o valor da variável de 16 bits especificada como uma operação atômica. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))
</dt> <dd>

Incrementa (aumenta em um) o valor da variável de bits de 64 especificada como uma operação atômica. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))
</dt> <dd>

Executa uma operação atômica ou com os valores **longos** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))
</dt> <dd>

Executa uma operação atômica ou em valores de **caracteres** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))
</dt> <dd>

Executa uma operação atômica ou com os valores **curtos** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))
</dt> <dd>

Executa uma operação atômica ou em valores **LONGLONG** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedPushListSListEx**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

Insere uma lista vinculada individualmente na frente de outra lista vinculada individualmente. O acesso às listas é sincronizado em um sistema multiprocessador. Esta versão do método não usa a Convenção de chamada [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) .

</dd> <dt>

[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))
</dt> <dd>

Executa uma operação de XOR atômico nos valores **longos** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))
</dt> <dd>

Executa uma operação de XOR atômico nos valores de **caracteres** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))
</dt> <dd>

Executa uma operação de XOR atômico nos valores **curtos** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> <dt>

[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))
</dt> <dd>

Executa uma operação de XOR atômico nos valores de **LONGLONG** especificados. A operação é executada atomicamente, mas sem usar barreiras de memória.

</dd> </dl>

## <a name="windows-7"></a>Windows 7

### <a name="new-functions"></a>Novas funções

<dl> <dt>

[**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

Ativa o temporizador waited especificado e fornece informações de contexto para o temporizador.

</dd> <dt>

[**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

Tenta adquirir um bloqueio de SRW (leitor/gravador) reduzido no modo exclusivo. Se a chamada for bem-sucedida, o thread de chamada assumirá a propriedade do bloqueio.

</dd> <dt>

[**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

Tenta adquirir um bloqueio de SRW (leitor/gravador) reduzido no modo compartilhado. Se a chamada for bem-sucedida, o thread de chamada assumirá a propriedade do bloqueio.

</dd> </dl>

### <a name="new-structures"></a>Novas estruturas

<dl> <dt>

[**contexto do motivo \_**](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

Contém informações de contexto para um temporizador ativado com [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).

</dd> </dl>

 

 
