---
description: Os threads são agendados para ser executados com base em sua prioridade de agendamento.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Prioridades de agendamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f86e6ef78ffe1e549045eebbe435674b50f25f25bd30598fce8581c06092a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793308"
---
# <a name="scheduling-priorities"></a>Prioridades de agendamento

Os threads são agendados para ser executados com base em *sua prioridade de agendamento.* Cada thread recebe uma prioridade de agendamento. Os níveis de prioridade variam de zero (prioridade mais baixa) a 31 (prioridade mais alta). Somente o thread de página zero pode ter uma prioridade de zero. (O thread de página zero é um thread do sistema responsável por zerar todas as páginas livres quando não há outros threads que precisem ser executados.)

O sistema trata todos os threads com a mesma prioridade que igual. O sistema atribui fatias de tempo de forma round robin a todos os threads com a prioridade mais alta. Se nenhum desses threads estiver pronto para ser executado, o sistema atribuirá fatias de tempo de forma round robin a todos os threads com a próxima prioridade mais alta. Se um thread de prioridade mais alta ficar disponível para execução, o sistema deixará de executar o thread de prioridade mais baixa (sem permitir que ele termine de usar sua fatia de tempo) e atribuirá uma fatia de tempo integral ao thread de prioridade mais alta. Para obter mais informações, consulte [Opções de contexto](context-switches.md).

A prioridade de cada thread é determinada pelos seguintes critérios:

-   A classe de prioridade de seu processo
-   O nível de prioridade do thread dentro da classe de prioridade de seu processo

A classe de prioridade e o nível de prioridade são combinados para formar a *prioridade base* de um thread. Para obter informações sobre a prioridade dinâmica de um thread, consulte [Priority Boosts](priority-boosts.md).

## <a name="priority-class"></a>Classe Priority

Cada processo pertence a uma das seguintes classes de prioridade:<dl> CLASSE PRIORITY \_ \_ IDLE  
ABAIXO \_ DA CLASSE DE PRIORIDADE \_ \_ NORMAL  
CLASSE \_ DE PRIORIDADE \_ NORMAL  
ACIMA \_ DA CLASSE DE PRIORIDADE \_ \_ NORMAL  
CLASSE \_ DE ALTA \_ PRIORIDADE  
CLASSE \_ PRIORITY EM TEMPO \_ REAL  
</dl>

Por padrão, a classe de prioridade de um processo é NORMAL \_ PRIORITY \_ CLASS. Use a [**função CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) para especificar a classe de prioridade de um processo filho quando você a criar. Se o processo de chamada for IDLE \_ PRIORITY CLASS ou BELOW NORMAL PRIORITY \_ \_ \_ \_ CLASS, o novo processo herdará essa classe. Use a [**função GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) para determinar a classe de prioridade atual de um processo e a [**função SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para alterar a classe de prioridade de um processo.

Processos que monitoram o sistema, como savers de tela ou aplicativos que atualizem periodicamente uma exibição, devem usar IDLE \_ PRIORITY \_ CLASS. Isso impede que os threads desse processo, que não têm alta prioridade, interfiram em threads de prioridade mais alta.

Use HIGH \_ PRIORITY \_ CLASS com cuidado. Se um thread for executado no nível de prioridade mais alta por períodos estendidos, outros threads no sistema não obterão o tempo do processador. Se vários threads são definidos com alta prioridade ao mesmo tempo, os threads perdem sua eficácia. A classe de alta prioridade deve ser reservada para threads que devem responder a eventos críticos de tempo. Se seu aplicativo executar uma tarefa que requer a classe de alta prioridade enquanto o restante de suas tarefas for prioridade normal, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para aumentar temporariamente a classe de prioridade do aplicativo; em seguida, reduza-o depois que a tarefa de tempo crítico tiver sido concluída. Outra estratégia é criar um processo de alta prioridade que tenha todos os threads bloqueados na maioria das vezes, criando threads somente quando tarefas críticas são necessárias. O ponto importante é que um thread de alta prioridade deve ser executado por um breve período e somente quando ele tem um trabalho crítico de tempo a ser executado.

Você quase nunca deve usar a CLASSE PRIORITY EM TEMPO REAL, pois isso interrompe os threads do sistema que gerenciam a entrada do mouse, a entrada do teclado e a liberação \_ do disco em segundo \_ plano. Essa classe pode ser apropriada para aplicativos que "conversam" diretamente com o hardware ou que executam tarefas breves que devem ter interrupções limitadas.

## <a name="priority-level"></a>Nível de prioridade

A seguir estão os níveis de prioridade em cada classe de prioridade:<dl> THREAD \_ PRIORITY \_ IDLE  
PRIORIDADE DE THREAD \_ \_ MAIS BAIXA  
PRIORIDADE \_ DO THREAD ABAIXO DO \_ \_ NORMAL  
PRIORIDADE \_ DE \_ THREAD NORMAL  
PRIORIDADE \_ DE THREAD ACIMA DO \_ \_ NORMAL  
PRIORIDADE DE THREAD \_ \_ MAIS ALTA  
TEMPO CRÍTICO \_ DE \_ PRIORIDADE DO \_ THREAD  
</dl>

Todos os threads são criados usando THREAD \_ PRIORITY \_ NORMAL. Isso significa que a prioridade do thread é a mesma que a classe de prioridade do processo. Depois de criar um thread, use a [**função SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) para ajustar sua prioridade em relação a outros threads no processo.

Uma estratégia típica é usar THREAD PRIORITY ABOVE NORMAL ou THREAD PRIORITY HIGHEST para o thread de entrada do processo, para garantir que o aplicativo seja responsivo \_ \_ ao \_ \_ \_ usuário. Threads em segundo plano, especialmente aqueles que fazem uso intensivo de processador, podem ser definidos como THREAD PRIORITY BELOW NORMAL ou THREAD PRIORITY LOWEST, para garantir que eles possam ser \_ \_ \_ \_ \_ preempção quando necessário. No entanto, se você tiver um thread aguardando outro thread com prioridade mais baixa para concluir alguma tarefa, bloqueie a execução do thread de alta prioridade em espera. Para fazer isso, use uma função [wait](../sync/wait-functions.md), [a](../sync/critical-section-objects.md)seção crítica ou a função [**Sleep,**](/windows/win32/api/synchapi/nf-synchapi-sleep) [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)ou [**SwitchToThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) Isso é preferível para que o thread execute um loop. Caso contrário, o processo pode se tornar deadlock, porque o thread com prioridade mais baixa nunca é agendado.

Para determinar o nível de prioridade atual de um thread, use a [**função GetThreadPriority.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority)

## <a name="base-priority"></a>Prioridade de Base

A classe de prioridade do processo e o nível de prioridade do thread são combinados para formar a prioridade base de cada thread.

A tabela a seguir mostra a prioridade base para combinações de classe de prioridade de processo e valor de prioridade de thread.


<table>
<tr>
<th colspan="2">Classe de prioridade de processo</th>
<th>Nível de prioridade do thread</th>
<th>Prioridade base</th>
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
<td>Thread_priority_highest</td>
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
<td>Thread_priority_highest</td>
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

 

 

 
