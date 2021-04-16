---
description: O serviço de ordenação de threads controla a execução de um ou mais threads de cliente. Ele garante que cada thread de cliente seja executado uma vez durante o período especificado e em ordem relativa.
ms.assetid: 5c37873a-ced4-447e-a6e1-55cfa8ab24b4
title: Serviço de ordenação de threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b3cd12b26124b47d506585425388a4542a70df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754306"
---
# <a name="thread-ordering-service"></a>Serviço de ordenação de threads

O *serviço de ordenação de threads* controla a execução de um ou mais threads de cliente. Ele garante que cada thread de cliente seja executado uma vez durante o período especificado e em ordem relativa.

**Windows Server 2003 e Windows XP:** O serviço de ordenação de threads está disponível a partir do Windows Vista e do Windows Server 2008.

O serviço de ordenação de threads está desativado por padrão e deve ser iniciado pelo usuário. Enquanto o serviço de ordenação de threads está em execução, ele é ativado a cada 5 segundos para verificar se há uma nova solicitação, mesmo que o sistema esteja ocioso. Isso impede que o sistema fique em suspensão por mais de 5 segundos, fazendo com que o sistema consuma mais energia. Se a eficiência de energia for crítica para o aplicativo, é melhor não usar o serviço de ordenação de threads e, em vez disso, permitir que o Agendador do sistema gerencie a execução de threads.

Cada thread de cliente pertence a um *grupo de ordenação de thread*. O *thread pai* cria um ou mais grupos de ordenação de threads chamando a função [**AvRtCreateThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup) . O thread pai usa essa função para especificar o período para o grupo de ordenação de threads e um intervalo de tempo limite.

Threads de cliente adicionais chamam a função [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup) para ingressar em um grupo de ordenação de thread existente. Esses threads indicam se são um predecessor ou um sucessor para o thread pai na ordem de execução. Espera-se que cada thread de cliente conclua uma determinada quantidade de processamento a cada período. Todos os threads dentro do grupo devem concluir sua execução dentro do período mais o intervalo de tempo limite.

Os threads de um grupo de ordenação de threads incluem seu código de processamento dentro de um loop que é controlado pela função [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) . Primeiro, os threads predecessores são executados um de cada vez na ordem em que ingressaram no grupo, enquanto os threads pai e sucessora são bloqueados em suas chamadas para **AvRtWaitOnThreadOrderingGroup**. Quando cada thread de predecessora é concluído com seu processamento, o controle de execução retorna à parte superior de seu loop de processamento e o thread chama **AvRtWaitOnThreadOrderingGroup** novamente para bloquear até a próxima vez. Depois que todos os threads predecessores tiverem chamado essa função, o serviço de ordenação de threads poderá agendar o thread pai. Finalmente, quando o thread pai conclui seu processamento e chama **AvRtWaitOnThreadOrderingGroup** novamente, o serviço de ordenação de threads pode agendar os threads de sucessor um de cada vez na ordem em que ingressaram no grupo. Se todos os threads concluírem sua execução antes do término de um período, todos os threads aguardarão até que o restante do período decorra antes que qualquer um seja executado novamente.

Quando o cliente não precisa mais ser executado como parte do grupo de ordenação de threads, ele chama a função [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup) para se remover do grupo. Observe que o thread pai não deve se remover de um grupo de ordenação de threads. Se um thread não concluir sua execução antes do período mais o intervalo de tempo limite expirar, ele será excluído do grupo.

O thread pai chama a função [**AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup) para excluir o grupo de ordenação de threads. O grupo de ordenação de thread também será destruído se o thread pai não concluir sua execução antes do período mais o intervalo de tempo limite expirar. Quando o grupo de ordenação de threads é destruído, todas as chamadas para [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) de threads desse grupo falham ou expiram.

 

 



