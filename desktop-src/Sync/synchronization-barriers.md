---
description: Uma barreira de sincronização permite que vários threads aguardem até que todos os threads tenham atingido um ponto específico de execução antes de qualquer thread continuar.
ms.assetid: 3A76E6F7-C38B-4843-9496-36F3C78B700C
title: Barreiras de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4276f0bbc5a10eef391c12cc51ebd475e563bd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171472"
---
# <a name="synchronization-barriers"></a>Barreiras de sincronização

Uma barreira de sincronização permite que vários threads aguardem até que todos os threads tenham atingido um ponto específico de execução antes de qualquer thread continuar. As barreiras de sincronização não podem ser compartilhadas entre processos.

As barreiras de sincronização são úteis para cálculos em fases, em que os threads que executam o mesmo código em paralelo devem todos concluir uma fase antes de passar para o próximo.

Para criar uma barreira de sincronização, chame a função [**InitializeSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) e especifique um número máximo de threads e quantas vezes um thread deve ser girado antes de ser bloqueado. Em seguida, inicie os threads que usarão a barreira. Depois que cada thread conclui seu trabalho, ele chama [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) para aguardar na barreira. A função **EnterSynchronizationBarrier** bloqueia cada thread até que o número de threads bloqueados na barreira atinja a contagem máxima de threads para a barreira, ponto em que o **EnterSynchronizationBarrier** desbloqueia todos os threads. A função **EnterSynchronizationBarrier** retorna **true** para exatamente um dos threads que inseriu a barreira e retorna **false** para todos os outros threads.

Para liberar uma barreira de sincronização quando ela não for mais necessária, chame [**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier). É seguro chamar essa função imediatamente após chamar [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) porque essa função garante que todos os threads concluíram o uso da barreira antes de serem liberados.

Se uma barreira de sincronização nunca for excluída, os threads poderão especificar o sinalizador de **\_ \_ \_ não \_ exclusão de sinalizadores de barreira de sincronização** quando inserirem a barreira. Todos os threads que usam a barreira devem especificar esse sinalizador; Se qualquer thread não tiver, o sinalizador será ignorado. Esse sinalizador faz com que a função ignore o trabalho extra necessário para a segurança de exclusão, o que pode melhorar o desempenho. Observe que a exclusão de uma barreira enquanto esse sinalizador está em vigor pode resultar em um acesso de identificador inválido e em um ou mais threads bloqueados permanentemente.

 

 



