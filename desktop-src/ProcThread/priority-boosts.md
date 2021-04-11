---
description: Cada thread tem uma prioridade dinâmica.
ms.assetid: bcc6cec7-2d85-4810-98d0-7d99486f4924
title: Aumentos de prioridade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f463f30b0abffb24daadb4241ad32c5b51f123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169502"
---
# <a name="priority-boosts"></a>Aumentos de prioridade

Cada thread tem uma *prioridade dinâmica*. Essa é a prioridade que o Agendador usa para determinar qual thread executar. Inicialmente, a prioridade dinâmica de um thread é igual à prioridade base. O sistema pode aumentar e diminuir a prioridade dinâmica para garantir que ela seja responsiva e que nenhum thread fique sem falta de tempo do processador. O sistema não aumenta a prioridade de threads com um nível de prioridade base entre 16 e 31. Somente os threads com uma prioridade básica entre 0 e 15 recebem aumentos de prioridade dinâmica.

O sistema aumenta a prioridade dinâmica de um thread para melhorar sua capacidade de resposta da seguinte maneira.

-   Quando um processo que usa \_ \_ a classe de prioridade normal é trazido para o primeiro plano, o Agendador aumenta a classe de prioridade do processo associado à janela em primeiro plano, para que seja maior ou igual à classe de prioridade de qualquer processo em segundo plano. A classe Priority retorna à sua configuração original quando o processo não está mais em primeiro plano.
-   Quando uma janela recebe entrada, como mensagens de temporizador, mensagens de mouse ou entrada de teclado, o Agendador aumenta a prioridade do thread que possui a janela.
-   Quando as condições de espera de um thread bloqueado são satisfeitas, o Agendador aumenta a prioridade do thread. Por exemplo, quando uma operação de espera associada ao disco ou a e/s de teclado for concluída, o thread receberá um aumento de prioridade.

    Você pode desabilitar o recurso de aumento de prioridade chamando a função [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost) ou [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost) . Para determinar se esse recurso foi desabilitado, chame a função [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost) ou [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost) .

Depois de gerar a prioridade dinâmica de um thread, o Agendador reduz essa prioridade em um nível cada vez que o thread conclui uma fração de tempo, até que o thread retorne para sua prioridade base. A prioridade dinâmica de um thread nunca é menor que sua prioridade base.

 

 
