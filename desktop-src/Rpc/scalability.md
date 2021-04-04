---
title: Escalabilidade
description: Escalabilidade
ms.assetid: 39327621-b536-4494-9319-9e9d4f534123
keywords:
- Escalabilidade
- RPC de chamada de procedimento remoto, práticas recomendadas, escalabilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0728e35d9c9b27494014363c448be9965e39eea7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822928"
---
# <a name="scalability"></a>Escalabilidade

O termo, escalabilidade, geralmente é usado. Para esta seção, é fornecida uma definição dupla:

-   A escalabilidade é a capacidade de utilizar totalmente a potência de processamento disponível em um sistema multiprocessador (2, 4, 8, 32 ou mais processadores).
-   A escalabilidade é a capacidade de atender a um grande número de clientes.

Essas duas definições relacionadas são comumente conhecidas como *escalar verticalmente*. O fim deste tópico fornece dicas sobre como *escalar* horizontalmente.

Essa discussão se concentra exclusivamente na gravação de servidores escalonáveis, não em clientes escalonáveis, pois os servidores escalonáveis são requisitos mais comuns. Esta seção também aborda a escalabilidade no contexto de servidores RPC e RPC. As práticas recomendadas para escalabilidade, como reduzir a contenção, evitar erros de cache frequentes em locais de memória global ou evitar o falso compartilhamento, não são discutidas aqui.

## <a name="rpc-threading-model"></a>Modelo de Threading RPC

Quando uma chamada RPC é recebida por um servidor, a rotina de servidor (rotina do Gerenciador) é chamada em um thread fornecido pelo RPC. O RPC usa um pool de threads adaptável que aumenta e diminui à medida que a carga de trabalho flutua. A partir do Windows 2000, o núcleo do pool de threads RPC é uma porta de conclusão. A porta de conclusão e seu uso por RPC são ajustados de zero para rotinas de servidor de contenção baixa. Isso significa que o pool de threads RPC aumenta agressivamente o número de threads de serviço se alguns se tornarem bloqueados. Ele opera na pré-continuação de que o bloqueio é raro e, se um thread é bloqueado, essa é uma condição temporária que é rapidamente resolvida. Essa abordagem permite a eficiência para servidores com baixa contenção. Por exemplo, um servidor RPC de chamada void operando em um servidor 550MHz de oito processadores acessado por uma SAN (rede de área do sistema) de alta velocidade serve mais de 30.000 chamadas void por segundo de mais de 200 clientes remotos. Isso representa mais de 108 milhões chamadas por hora.

O resultado é que o pool de threads agressivos realmente fica no caminho quando a contenção no servidor é alta. Para ilustrar, imagine um servidor de imposto pesado usado para acessar os arquivos remotamente. Suponha que o servidor Adote a abordagem mais direta: ele simplesmente lê/grava o arquivo de forma síncrona no thread em que o RPC invoca a rotina do servidor. Além disso, suponha que tenhamos um servidor de quatro processadores servindo muitos clientes.

O servidor será iniciado com cinco threads (isso na verdade varia, mas cinco threads são usados para simplificar). Depois que o RPC pega a primeira chamada RPC, ele despacha a chamada para a rotina do servidor e a rotina do servidor emite a e/s. Raramente, ele perde o cache de arquivos e, em seguida, bloqueia a espera pelo resultado. Assim que ele é bloqueado, o quinto thread é liberado para pegar uma solicitação e um sexto thread é criado como uma espera ativa. Supondo que cada décimo de operação de e/s não seja o cache e bloqueará 100 milissegundos (um valor de tempo arbitrário) e supondo que o servidor de quatro processadores atenda a 20.000 chamadas por segundo (5.000 chamadas por processador), uma modelagem simplista prevê que cada processador gerará aproximadamente 50 threads. Isso pressupõe que uma chamada que bloqueará a cada 2 milissegundos e depois de 100 milissegundos o primeiro thread seja liberado novamente, de modo que o pool se estabilizará em cerca de 200 threads (50 por processador).

O comportamento real é mais complicado, pois o grande número de threads causará opções de contexto extras que tornaram o servidor lento e também reduzirá a taxa de criação de novos threads, mas a ideia básica estará clara. O número de threads aumenta rapidamente à medida que os threads no servidor iniciam o bloqueio e aguardam algo (seja ele uma e/s ou acesso a um recurso).

O RPC e a porta de conclusão que solicita solicitações de entrada tentarão manter o número de threads RPC utilizáveis no servidor para ser igual ao número de processadores no computador. Isso significa que em um servidor de quatro processadores, uma vez que um thread retorna para RPC, se houver quatro ou mais threads de RPC utilizáveis, o quinto thread não terá permissão para pegar uma nova solicitação e, em vez disso, ficará em um estado de espera ativa no caso de um dos blocos de threads utilizáveis no momento. Se o quinto thread aguardar tempo suficiente como uma espera ativa sem o número de threads de RPC utilizáveis cair abaixo do número de processadores, ele será liberado, ou seja, o pool de threads será reduzido.

Imagine um servidor com vários threads. Como explicado anteriormente, um servidor RPC termina com vários threads, mas somente se os threads forem bloqueados com frequência. Em um servidor em que os threads geralmente são bloqueados, um thread que retorna para o RPC é retirado da lista de espera ativa, porque todos os threads utilizáveis atualmente são bloqueados e recebem uma solicitação para processar. Quando um thread é bloqueado, o Dispatcher do thread no kernel alterna o contexto para outro thread. Esse contexto alterna por si só consome ciclos de CPU. O próximo Thread executará código diferente, acessando diferentes estruturas de dados e terá uma pilha diferente, o que significa que a taxa de acesso ao cache de memória (os caches L1 e L2) será muito menor, resultando em uma execução mais lenta. Os inúmeros threads que executam simultaneamente aumenta a contenção de recursos existentes, como heap, seções críticas no código do servidor e assim por diante. Isso aumenta ainda mais a contenção como comboios no formulário de recursos. Se a memória for baixa, a demanda de memória exercida pelo número grande e crescente de threads causará falhas de página, o que aumentará ainda mais a taxa na qual os threads são bloqueados e fará com que ainda mais threads sejam criados. Dependendo da frequência com que ele é bloqueado e da quantidade de memória física disponível, o servidor pode se estabilizar em algum nível inferior de desempenho com uma taxa alta de alternância de contexto, ou pode deteriorar-se até o ponto em que ele está acessando apenas repetidamente o disco rígido e a alternância de contexto sem executar nenhum trabalho real. Essa situação não será mostrada sob carga de trabalho leve, é claro, mas uma carga de trabalho pesada rapidamente traz o problema para a superfície.

Como isso pode ser impedido? Se os threads devem ser bloqueados, declare chamadas como assíncronas e, depois que a solicitação entrar na rotina do servidor, enfileirar-a para um pool de threads de trabalho que usam os recursos assíncronos do sistema de e/s e/ou RPC. Se o servidor estiver, por sua vez, fazendo com que as chamadas RPC tornem as assíncronas e certifique-se de que a fila não se expanda muito grande. Se a rotina de servidor estiver executando a e/s de arquivo, use a e/s de arquivo assíncrono para enfileirar várias solicitações para o sistema de e/s e ter apenas alguns threads em fila e obter os resultados. Se a rotina de servidor estiver fazendo a e/s de rede, use os recursos assíncronos do sistema para emitir as solicitações e selecionar as respostas de forma assíncrona e usar o menor número possível de threads. Quando a e/s for concluída ou a chamada RPC que o servidor fez estiver concluída, conclua a chamada RPC assíncrona que forneceu a solicitação. Isso permitirá que o servidor seja executado com o mínimo de threads possível, o que aumenta o desempenho e o número de clientes que um servidor pode atender.

## <a name="scale-out"></a>Escalonamento horizontal

O RPC pode ser configurado para funcionar com o NLB (balanceamento de carga de rede) se o NLB estiver configurado de modo que todas as solicitações de um determinado endereço de cliente vá para o mesmo servidor. Como cada cliente RPC abre um pool de conexões (para obter mais informações, consulte [RPC e a rede](rpc-and-the-network.md)), é essencial que todas as conexões do pool do cliente em questão terminem no mesmo computador do servidor. Desde que essa condição seja atendida, um cluster NLB pode ser configurado para funcionar como um servidor RPC grande com escalabilidade potencialmente excelente.

 

 




