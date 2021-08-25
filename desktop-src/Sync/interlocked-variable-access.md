---
description: Os aplicativos devem sincronizar o acesso a variáveis que são compartilhadas por vários threads.
ms.assetid: 729c0e68-ef52-4d6c-b771-a89043a937e6
title: Acesso de variável interbloqueada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b298dffe45d1a0de655e225c8a240dd72be15a0fff7e4d6eac25ebb0a1130ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126316"
---
# <a name="interlocked-variable-access"></a>Acesso de variável interbloqueada

Os aplicativos devem sincronizar o acesso a variáveis que são compartilhadas por vários threads. Os aplicativos também devem garantir que as operações nessas variáveis sejam executadas atomicamente (executadas em sua totalidade ou não).

Leituras e gravações simples para variáveis de 32 bits alinhadas corretamente são operações atômicas. Em outras palavras, você não acabará com apenas uma parte da variável atualizada; todos os bits são atualizados de maneira atômica. No entanto, não há garantia de que o acesso seja sincronizado. Se dois threads estiverem lendo e gravando da mesma variável, você não poderá determinar se um thread executará sua operação de leitura antes que o outro execute sua operação de gravação.

Leituras e gravações simples para as variáveis de 64 bits alinhadas corretamente são atômicas no Windows de 64 bits. Leituras e gravações em valores de 64 bits não têm garantia de serem atômicas em Windows de 32 bits. Leituras e gravações em variáveis de outros tamanhos não têm garantia de serem atômicas em qualquer plataforma.

## <a name="the-interlocked-api"></a>A API intercadeado

As funções intercadeados fornecem um mecanismo simples para sincronizar o acesso a uma variável que é compartilhada por vários threads. Eles também executam operações em variáveis de maneira atômica. Os threads de processos diferentes podem usar essas funções se a variável estiver na memória compartilhada.

As funções [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) e [**InterlockedDecrement**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement) combinam as etapas envolvidas em incrementar ou decrementar uma variável em uma operação atômica. Esse recurso é útil em um sistema operacional multitarefa, no qual o sistema pode interromper a execução de um thread para conceder uma fatia do tempo do processador a outro thread. Sem essa sincronização, dois threads podiam ler o mesmo valor, incrementar a ti em 1 e armazenar o novo valor para um aumento total de 1 em vez de 2. As funções de acesso a variáveis interbloqueadas protegem contra esse tipo de erro.

As funções [**InterlockedExchange**](/windows/win32/api/winnt/nf-winnt-interlockedexchange) e [**InterlockedExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer) , de forma atômica, trocam os valores das variáveis especificadas. A função [**InterlockedExchangeAdd**](/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd) combina duas operações: adicionar duas variáveis juntas e armazenar o resultado em uma das variáveis.

As funções [**InterlockedCompareExchange**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange), [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))e [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) combinam duas operações: comparando dois valores e armazenando um terceiro valor em uma das variáveis, com base no resultado da comparação.

As funções [**InterlockedAnd**](/windows/win32/api/winnt/nf-winnt-interlockedand), [**interbloqueador**](/windows/win32/api/winnt/nf-winnt-interlockedor)e [**InterlockedXor**](/windows/win32/api/winnt/nf-winnt-interlockedxor) executam atomicamente as operações and, or e XOR, respectivamente.

Há funções que são projetadas especificamente para executar acesso de variável intercadeado em valores e endereços de memória de 64 bits e são otimizadas para uso em Windows de 64 bits. Cada uma dessas funções contém "64" no nome; por exemplo, [**InterlockedDecrement64**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement64) e [**InterlockedCompareExchangeAcquire64**](/previous-versions/windows/desktop/legacy/ms683566(v=vs.85)).

a maioria das funções intercadeados fornece barreiras de memória total em todas as plataformas Windows. Também há funções que combinam as operações de acesso de variável interbloqueada básica com a semântica de ordenação de memória de aquisição e liberação suportada por determinados processadores. Cada uma dessas funções contém a palavra "adquirir" ou "Release" em seus nomes; por exemplo, [**InterlockedDecrementAcquire**](/previous-versions/windows/desktop/legacy/ms683583(v=vs.85)) e [**InterlockedDecrementRelease**](/previous-versions/windows/desktop/legacy/ms683586(v=vs.85)). Adquirir a semântica de memória especifique que a operação de memória que está sendo executada pelo thread atual ficará visível antes de qualquer operação de memória ser tentada. Semântica de memória de liberação especifique que a operação de memória que está sendo executada pelo thread atual ficará visível depois que todas as outras operações de memória forem concluídas. Essas semânticas permitem que você force as operações de memória a serem executadas em uma ordem específica. Use a semântica de aquisição ao inserir uma região protegida e a semântica de liberação ao deixá-la.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Intrínsecos do compilador](/cpp/intrinsics/compiler-intrinsics?view=vs-2019)
</dt> <dt>

[Sincronização e problemas de multiprocessador](synchronization-and-multiprocessor-issues.md)
</dt> </dl>

 

 
