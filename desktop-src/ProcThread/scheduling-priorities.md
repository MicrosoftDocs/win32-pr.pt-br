---
description: Os threads são agendados para execução com base em sua prioridade de agendamento.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Prioridades de agendamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770130"
---
# <a name="scheduling-priorities"></a>Prioridades de agendamento

Os threads são agendados para execução com base em sua *prioridade de agendamento*. Cada thread recebe uma prioridade de agendamento. Os níveis de prioridade variam de zero (prioridade mais baixa) a 31 (prioridade mais alta). Somente o thread de página zero pode ter uma prioridade zero. (O thread de página zero é um thread do sistema responsável por zerar qualquer página livre quando não há nenhum outro thread que precise ser executado.)

O sistema trata todos os threads com a mesma prioridade igual. O sistema atribui frações de tempo em um modo Round Robin a todos os threads com a prioridade mais alta. Se nenhum desses threads estiver pronto para ser executado, o sistema atribuirá fatias de tempo em um modo Round Robin a todos os threads com a próxima prioridade mais alta. Se um thread de prioridade mais alta se tornar disponível para execução, o sistema deixará de executar o thread de prioridade inferior (sem permitir que ele termine de usar sua fração de tempo) e atribuirá uma fatia de tempo completa ao thread de prioridade mais alta. Para obter mais informações, consulte [alternâncias de contexto](context-switches.md).

A prioridade de cada thread é determinada pelos seguintes critérios:

-   A classe de prioridade de seu processo
-   O nível de prioridade do thread dentro da classe de prioridade de seu processo

A classe de prioridade e o nível de prioridade são combinados para formar a *prioridade base* de um thread. Para obter informações sobre a prioridade dinâmica de um thread, consulte [aumentos de prioridade](priority-boosts.md).

## <a name="priority-class"></a>Classe de prioridade

Cada processo pertence a uma das seguintes classes de prioridade:<dl> \_classe de prioridade ociosa \_  
ABAIXO \_ da \_ classe de prioridade normal \_  
\_classe de prioridade normal \_  
ACIMA \_ da \_ classe de prioridade normal \_  
\_classe de prioridade alta \_  
\_classe de prioridade em tempo real \_  
</dl>

Por padrão, a classe de prioridade de um processo é a \_ classe de prioridade normal \_ . Use a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) para especificar a classe de prioridade de um processo filho ao criá-lo. Se o processo de chamada for \_ uma \_ classe de prioridade ociosa ou abaixo \_ \_ \_ da classe de prioridade normal, o novo processo herdará essa classe. Use a função [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) para determinar a classe de prioridade atual de um processo e a função [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para alterar a classe de prioridade de um processo.

Processos que monitoram o sistema, como proteções de tela ou aplicativos que atualizam periodicamente uma exibição, devem usar a \_ classe de prioridade ociosa \_ . Isso impede que os threads desse processo, que não têm prioridade alta, interfiram com threads de prioridade mais alta.

Use \_ \_ a classe de prioridade alta com cuidado. Se um thread for executado no nível de prioridade mais alto para períodos estendidos, outros threads no sistema não terão tempo de processador. Se vários threads forem definidos com prioridade alta ao mesmo tempo, os threads perderão sua eficácia. A classe de alta prioridade deve ser reservada para threads que devem responder a eventos de tempo crítico. Se seu aplicativo executar uma tarefa que requer a classe de alta prioridade enquanto o restante de suas tarefas for de prioridade normal, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para aumentar a classe de prioridade do aplicativo temporariamente; em seguida, reduza-o após a conclusão da tarefa de tempo crítico. Outra estratégia é criar um processo de alta prioridade que tenha todos os seus threads bloqueados na maior parte do tempo, despertando threads somente quando tarefas críticas forem necessárias. O ponto importante é que um thread de alta prioridade deve ser executado por um curto período e apenas quando ele tem um trabalho de tempo crítico para ser executado.

Você quase nunca deve usar \_ a classe de prioridade em tempo real \_ , pois isso interrompe os threads do sistema que gerenciam a entrada do mouse, a entrada do teclado e a liberação de disco em segundo plano. Essa classe pode ser apropriada para aplicativos que "falam" diretamente com o hardware ou que executam tarefas curtas que devem ter interrupções limitadas.

## <a name="priority-level"></a>Nível de prioridade

A seguir estão os níveis de prioridade dentro de cada classe de prioridade:<dl> prioridade de THREAD \_ \_ ociosa  
\_prioridade \_ mais baixa da thread  
prioridade de THREAD \_ \_ abaixo do \_ normal  
prioridade de THREAD \_ \_ normal  
prioridade de THREAD \_ \_ acima do \_ normal  
prioridade de THREAD \_ \_ mais alta  
tempo de prioridade de THREAD \_ \_ \_ crítico  
</dl>

Todos os threads são criados usando a prioridade de THREAD \_ \_ normal. Isso significa que a prioridade de thread é a mesma que a classe de prioridade de processo. Depois de criar um thread, use a função [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) para ajustar sua prioridade em relação a outros threads no processo.

Uma estratégia típica é usar a prioridade de THREAD acima da prioridade \_ \_ \_ normal ou \_ de thread \_ para o thread de entrada do processo, para garantir que o aplicativo seja responsivo ao usuário. Os threads em segundo plano, especialmente aqueles com uso intensivo de processador, podem ser definidos para prioridade de THREAD \_ \_ abaixo da \_ prioridade normal ou de thread \_ \_ mais baixa, para garantir que eles possam ser admitidos quando necessário. No entanto, se você tiver um thread Aguardando outro thread com uma prioridade mais baixa para concluir alguma tarefa, certifique-se de bloquear a execução do thread de alta prioridade em espera. Para fazer isso, use uma função de [espera](../sync/wait-functions.md), [seção crítica](../sync/critical-section-objects.md)ou a função de [**suspensão**](/windows/win32/api/synchapi/nf-synchapi-sleep) , [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)ou função de [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) . É preferível que o thread execute um loop. Caso contrário, o processo pode ser bloqueado, pois o thread com prioridade mais baixa nunca é agendado.

Para determinar o nível de prioridade atual de um thread, use a função [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) .

## <a name="base-priority"></a>Prioridade de Base

A classe de prioridade de processo e o nível de prioridade de thread são combinados para formar a prioridade base de cada thread.

A tabela a seguir mostra a prioridade base para combinações de classe de prioridade de processo e valor de prioridade de thread.


<table>
<tr>
<th colspan="2">Classe de prioridade de processo</th>
<th>Nível de prioridade do thread</th>
<th>Prioridade básica</th>
</tr>
<tr>
<td rowspan="7" colspan="2">IDLE_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>2</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>3</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">BELOW_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">ABOVE_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">HIGH_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>13</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>14</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>15</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">REALTIME_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>16</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>22</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>23</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>24</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>25</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>26</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>31</td>
</tr>
</table>

 

 

 
