---
description: 'Computadores com vários processadores normalmente são projetados para uma das duas arquiteturas: NUMA (acesso não uniforme à memória) ou SMP (multiprocessamento simétrico).'
ms.assetid: 3c9186c8-a54d-4536-8237-bfff78cc7d11
title: Vários processadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28b381faaceb5a171ddcf33c0705fee144f98952c4d473c0db8c7d99050deb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032406"
---
# <a name="multiple-processors"></a>Vários processadores

Computadores com vários processadores normalmente são projetados para uma das duas arquiteturas: NUMA (acesso não uniforme à memória) ou SMP (multiprocessamento simétrico).

Em um computador NUMA, cada processador está mais próximo de algumas partes da memória do que outras, tornando o acesso à memória mais rápido para algumas partes da memória do que outras partes. No modelo NUMA, o sistema tenta agendar threads em processadores próximos à memória que está sendo usada. Para obter mais informações sobre NUMA, consulte [Suporte a NUMA](numa-support.md).

Em um computador SMP, dois ou mais processadores ou núcleos idênticos se conectam a uma única memória principal compartilhada. No modelo SMP, qualquer thread pode ser atribuído a qualquer processador. Portanto, o agendamento de threads em um computador SMP é semelhante ao agendamento de threads em um computador com um único processador. No entanto, o agendador tem um pool de processadores, para que ele possa agendar threads para executar simultaneamente. O agendamento ainda é determinado pela prioridade do thread, mas pode ser influenciado pela definição da afinidade de thread e do processador ideal do thread, conforme discutido neste tópico.

## <a name="thread-affinity"></a>Afinidade de thread

*A afinidade de thread força* um thread a ser executado em um subconjunto específico de processadores. A definição da afinidade de thread geralmente deve ser evitada, pois pode interferir na capacidade do agendador de agendar threads efetivamente entre processadores. Isso pode diminuir os ganhos de desempenho produzidos pelo processamento paralelo. Um uso apropriado da afinidade de thread é testar cada processador.

O sistema representa a afinidade com uma máscara de bits chamada máscara de afinidade do processador. A máscara de afinidade é o tamanho do número máximo de processadores no sistema, com bits definidos para identificar um subconjunto de processadores. Inicialmente, o sistema determina o subconjunto de processadores na máscara.

Você pode obter a afinidade de thread atual para todos os threads do processo chamando a [**função GetProcessAffinityMask.**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) Use a [**função SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) para especificar a afinidade de thread para todos os threads do processo. Para definir a afinidade de thread para um único thread, use a [**função SetThreadAffinityMask.**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) A afinidade de thread deve ser um subconjunto da afinidade de processo.

Em sistemas com mais de 64 processadores, a máscara de afinidade inicialmente representa processadores em um único grupo de processadores. No entanto, a afinidade de thread pode ser definida como um processador em um grupo diferente, o que altera a máscara de afinidade para o processo. Para obter mais informações, consulte [Grupos de Processadores](processor-groups.md).

## <a name="thread-ideal-processor"></a>Processador ideal de thread

Quando você especifica um *processador ideal de thread,* o agendador executa o thread no processador especificado quando possível. Use a [**função SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) para especificar um processador preferencial para um thread. Isso não garante que o processador ideal será escolhido, mas fornece uma dica útil para o agendador. Em sistemas com mais de 64 processadores, você pode usar a função [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) para especificar um processador preferencial em um grupo de processadores específico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte ao NUMA](numa-support.md)
</dt> <dt>

[Grupos de processadores](processor-groups.md)
</dt> </dl>

 

 
