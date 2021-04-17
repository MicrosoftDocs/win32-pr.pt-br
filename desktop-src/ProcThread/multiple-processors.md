---
description: 'Computadores com vários processadores são normalmente projetados para uma das duas arquiteturas: o NUMA (acesso não uniforme à memória) ou SMP (multiprocessamento simétrico).'
ms.assetid: 3c9186c8-a54d-4536-8237-bfff78cc7d11
title: Vários processadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0093404a0df653a153823915f1ac72b5e41d50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775665"
---
# <a name="multiple-processors"></a>Vários processadores

Computadores com vários processadores são normalmente projetados para uma das duas arquiteturas: o NUMA (acesso não uniforme à memória) ou SMP (multiprocessamento simétrico).

Em um computador NUMA, cada processador está mais próximo de algumas partes da memória do que outros, tornando o acesso à memória mais rápido para algumas partes da memória do que outras partes. No modelo NUMA, o sistema tenta agendar threads em processadores que estão próximos da memória que está sendo usada. Para obter mais informações sobre o NUMA, consulte [suporte a numa](numa-support.md).

Em um computador SMP, dois ou mais processadores ou núcleos idênticos se conectam a uma única memória principal compartilhada. No modelo SMP, qualquer thread pode ser atribuído a qualquer processador. Portanto, o agendamento de threads em um computador SMP é semelhante ao agendamento de threads em um computador com um único processador. No entanto, o Agendador tem um pool de processadores, para que ele possa agendar a execução simultânea de threads. O agendamento ainda é determinado pela prioridade do thread, mas pode ser influenciado pela definição da afinidade de thread e do processador de thread ideal, conforme discutido neste tópico.

## <a name="thread-affinity"></a>Afinidade de thread

A *afinidade de thread* força um thread a ser executado em um subconjunto específico de processadores. Definir a afinidade de thread geralmente deve ser evitada, pois ela pode interferir na capacidade do Agendador de agendar threads com eficiência nos processadores. Isso pode diminuir os ganhos de desempenho produzidos pelo processamento paralelo. Um uso apropriado da afinidade de thread está testando cada processador.

O sistema representa a afinidade com uma bitmask chamada de máscara de afinidade de processador. A máscara de afinidade é o tamanho do número máximo de processadores no sistema, com bits definidos para identificar um subconjunto de processadores. Inicialmente, o sistema determina o subconjunto de processadores na máscara.

Você pode obter a afinidade de thread atual para todos os threads do processo chamando a função [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) . Use a função [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) para especificar a afinidade de thread para todos os threads do processo. Para definir a afinidade de thread para um único thread, use a função [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) . A afinidade de thread deve ser um subconjunto da afinidade de processo.

Em sistemas com mais de 64 processadores, a máscara de afinidade inicialmente representa os processadores em um único grupo de processador. No entanto, a afinidade de thread pode ser definida como um processador em um grupo diferente, que altera a máscara de afinidade do processo. Para obter mais informações, consulte [grupos de processadores](processor-groups.md).

## <a name="thread-ideal-processor"></a>Processador de thread ideal

Quando você especifica um *processador ideal de thread*, o Agendador executa o thread no processador especificado quando possível. Use a função [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) para especificar um processador preferencial para um thread. Isso não garante que o processador ideal será escolhido, mas fornece uma dica útil ao agendador. Em sistemas com mais de 64 processadores, você pode usar a função [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) para especificar um processador preferencial em um grupo de processador específico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a NUMA](numa-support.md)
</dt> <dt>

[Grupos de processadores](processor-groups.md)
</dt> </dl>

 

 
