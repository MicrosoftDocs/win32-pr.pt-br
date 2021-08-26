---
title: Escalabilidade
description: Escalabilidade
ms.assetid: 39327621-b536-4494-9319-9e9d4f534123
keywords:
- Escalabilidade
- RPC de Chamada de Procedimento Remoto , práticas recomendadas, escalabilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2a004a5ce3adb0f27e2e31071cac69fc1c34bfc650c618dcf39b3c8ebc954f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018056"
---
# <a name="scalability"></a>Escalabilidade

O termo, escalabilidade, geralmente é usado indevidamente. Para esta seção, uma definição dupla é fornecida:

-   Escalabilidade é a capacidade de utilizar totalmente a capacidade de processamento disponível em um sistema multiprocessador (2, 4, 8, 32 ou mais processadores).
-   Escalabilidade é a capacidade de serviço de um grande número de clientes.

Essas duas definições relacionadas geralmente são conhecidas como *dimensionamento.* O final deste tópico fornece dicas sobre *como escalar.*

Esta discussão se concentra exclusivamente na escrita de servidores escalonáveis, não em clientes escalonáveis, pois os servidores escalonáveis são requisitos mais comuns. Esta seção também aborda a escalabilidade apenas no contexto de servidores RPC e RPC. As práticas recomendadas para escalabilidade, como reduzir a contenção, evitar erros frequentes de cache em locais de memória global ou evitar o compartilhamento falso, não são discutidas aqui.

## <a name="rpc-threading-model"></a>Modelo de threading RPC

Quando uma chamada RPC é recebida por um servidor, a rotina do servidor (rotina de gerente) é chamada em um thread fornecido pelo RPC. O RPC usa um pool de threads adaptável que aumenta e diminui conforme a carga de trabalho flutua. A partir Windows 2000, o núcleo do pool de threads RPC é uma porta de conclusão. A porta de conclusão e seu uso por RPC são ajustados para rotinas de servidor de zero a baixa contenção. Isso significa que o pool de threads RPC aumentará agressivamente o número de threads de manutenção se alguns se tornarem bloqueados. Ele opera com a suposição de que o bloqueio é raro e, se um thread é bloqueado, essa é uma condição temporária que é resolvida rapidamente. Essa abordagem permite eficiência para servidores de baixa contenção. Por exemplo, um servidor RPC de chamada nula operando em um servidor de 550 MHz de oito processadores acessado por uma SAN (rede de área do sistema) de alta velocidade atende a mais de 30.000 chamadas nulas por segundo de mais de 200 clientes remotos. Isso representa mais de 108 milhões de chamadas por hora.

O resultado é que o pool de threads agressivo realmente fica no caminho quando a contenção no servidor é alta. Para ilustrar, imagine um servidor de trabalho pesado usado para acessar arquivos remotamente. Suponha que o servidor adote a abordagem mais simples: ele simplesmente lê/grava o arquivo de forma síncrona no thread no qual esse RPC invoca a rotina do servidor. Além disso, suponha que temos um servidor de quatro processadores que atende a muitos clientes.

O servidor começará com cinco threads (isso realmente varia, mas cinco threads são usados para simplificar). Depois que o RPC escolhe a primeira chamada RPC, ele envia a chamada para a rotina do servidor e a rotina do servidor emite a E/S. Raramente, ele perde o cache de arquivos e, em seguida, bloqueia a espera pelo resultado. Assim que ele é bloco, o quinto thread é liberado para atender a uma solicitação e um sexto thread é criado como uma espera quente. Supondo que cada décimo operação de E/S perca o cache e bloqueie por 100 milissegundos (um valor de tempo arbitrário) e supondo que o servidor de quatro processadores atende a cerca de 20.000 chamadas por segundo (5.000 chamadas por processador), uma modelagem simplista prevê que cada processador gerará aproximadamente 50 threads. Isso pressuém que uma chamada que bloqueará vem a cada 2 milissegundos e, depois de 100 milissegundos, o primeiro thread é liberado novamente para que o pool se estabilizará em cerca de 200 threads (50 por processador).

O comportamento real é mais complicado, pois o alto número de threads causará comutadores de contexto extras que retardam o servidor e também retardam a taxa de criação de novos threads, mas a ideia básica é clara. O número de threads vai para cima rapidamente à medida que os threads no servidor começam a bloquear e esperar por algo (seja uma E/S ou acesso a um recurso).

O RPC e a porta de conclusão que se aproximam das solicitações de entrada tentarão manter o número de threads RPC usáveis no servidor para serem iguais ao número de processadores no computador. Isso significa que, em um servidor de quatro processadores, depois que um thread retornar ao RPC, se houver quatro ou mais threads RPC usáveis, o quinto thread não terá permissão para escolher uma nova solicitação e, em vez disso, ficará em um estado de espera quente no caso de um dos blocos de threads atualmente usáveis. Se o quinto thread aguardar tempo suficiente como uma espera quente sem o número de threads RPC usáveis que estão abaixo do número de processadores, ele será liberado, ou seja, o pool de threads diminuirá.

Imagine um servidor com muitos threads. Conforme explicado anteriormente, um servidor RPC termina com muitos threads, mas somente se os threads são bloqueados com frequência. Em um servidor em que os threads geralmente bloqueiam, um thread que retorna ao RPC é retirado da lista de espera frequente, porque todos os threads atualmente em uso bloqueiam e recebe uma solicitação para processar. Quando um thread é bloco, o dispatcher de thread no kernel alterna o contexto para outro thread. Essa opção de contexto por si só consome ciclos de CPU. O próximo thread executará código diferente, acessará diferentes estruturas de dados e terá uma pilha diferente, o que significa que a taxa de acertos do cache de memória (os caches L1 e L2) será muito menor, resultando em uma execução mais lenta. Os vários threads em execução simultaneamente aumentam a contenção para recursos existentes, como heap, seções críticas no código do servidor e assim por diante. Isso aumenta ainda mais a contenção conforme os comboios no formulário de recursos. Se a memória for baixa, a pressão de memória pressionada pelo grande e crescente número de threads causará falhas de página, o que aumentará ainda mais a taxa na qual os threads são bloqueados e fará com que ainda mais threads sejam criados. Dependendo da frequência com que ele bloqueia e de quanto memória física está disponível, o servidor pode se estabilizar em algum nível inferior de desempenho com uma alta taxa de alternância de contexto ou pode chegar ao ponto em que está acessando apenas repetidamente o disco rígido e a alternância de contexto sem executar nenhum trabalho real. Essa situação não será demonstrada sob carga de trabalho leve, é claro, mas uma carga de trabalho pesada rapidamente traz o problema à superfície.

Como isso pode ser evitado? Se espera-se que os threads bloqueiem, declarem chamadas como assíncronas e, depois que a solicitação entrar na rotina do servidor, enfileiram-os em um pool de threads de trabalho que usam as funcionalidades assíncronas do sistema de E/S e/ou RPC. Se o servidor estiver, por sua vez, fazendo chamadas RPC, as tornarão assíncronas e certifique-se de que a fila não cresça muito grande. Se a rotina do servidor estiver executando E/S de arquivo, use a E/S de arquivo assíncrona para enfileirar várias solicitações para o sistema de E/S e ter apenas alguns threads enfileirando-os e pegar os resultados. Se a rotina do servidor estiver fazendo E/S de rede, novamente, use os recursos assíncronos do sistema para emitir as solicitações e pegar as respostas de forma assíncrona e usar o máximo possível de threads. Quando a E/S for concluída ou a chamada RPC feita pelo servidor estiver concluída, conclua a chamada RPC assíncrona que recebeu a solicitação. Isso permitirá que o servidor seja executado com o menor número possível de threads, o que aumenta o desempenho e o número de clientes que um servidor pode realizar.

## <a name="scale-out"></a>Escalonamento horizontal

O RPC pode ser configurado para funcionar com o NLB (Balanceamento de Carga de Rede) se o NLB estiver configurado, de modo que todas as solicitações de um determinado endereço de cliente vão para o mesmo servidor. Como cada cliente RPC abre um pool de conexões (para obter mais informações, consulte [RPC](rpc-and-the-network.md)e a Rede ), é essencial que todas as conexões do pool do cliente determinado terminem no mesmo computador servidor. Desde que essa condição seja atendida, um cluster NLB pode ser configurado para funcionar como um servidor RPC grande com escalabilidade potencialmente excelente.

 

 




