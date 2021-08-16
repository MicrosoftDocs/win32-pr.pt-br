---
title: Impedindo travamentos do lado do cliente
description: Há duas maneiras pelas quais o cliente pode desligar a conectividade de rede pode fazer com que as solicitações de servidor se tornem perdidas ou o próprio servidor pode falhar. Com as opções padrão, o RPC nunca fará uma chamada e o thread do cliente aguardará uma resposta para sempre.
ms.assetid: 2c201e29-9d9c-48e6-b0b5-68e4b25c3fb7
keywords:
- RPC de Chamada de Procedimento Remoto , práticas recomendadas, impedindo travamentos do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da79573e59e30c58a7c236b35293b678c93dde6bf999b477de054d6f3c62971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927291"
---
# <a name="preventing-client-side-hangs"></a>Impedindo travamentos do lado do cliente

Há duas maneiras pelas quais o cliente pode falhar: a conectividade de rede pode fazer com que as solicitações de servidor se tornem perdidas ou o próprio servidor pode falhar. Com as opções padrão, o RPC nunca fará uma chamada e o thread do cliente aguardará uma resposta para sempre.

Há dois métodos para evitar isso: keep alives e time-outs.

## <a name="tcp-keep-alives"></a>TCP Keep Alives

O cliente pode ser definido para executar ping periodicamente no servidor para garantir que o servidor esteja em execução. Os pings são keep alives TCP para as sequências de protocolo http [**\_ ncacn ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) e [**ncacn \_**](/windows/desktop/Midl/ncacn-http) e, como tal, são eficientes na utilização da CPU e na largura de banda de rede. Para habilitar keep alives em uma determinada chamada de procedimento remoto, use a [**função RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) antes que a chamada seja iniciada. Essa função assume um alça de associação e um tempo-out como argumentos. Cada chamada de procedimento remoto nesse alça de associação após **RpcMgmtSetComTimeout** usa o tempo de tempo de execução fornecido.

O parâmetro Timeout para a [**função RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) especifica por quanto tempo o tempo de execução RPC aguarda antes de ser ativas. O tempo máximo é um valor entre 0 e 10, em que 0 é o tempo máximo mínimo e 10 é um tempo máximo infinito (sem tempo máximo). O tempo em si não é em segundos; A conversão do valor de tempo-máximo fornecido para a **função RpcMgmtSetComTimeout** em segundos é feita pelo tempo de execução RPC e é específica da implementação.

A tabela a seguir fornece a conversão em segundos Windows 2000 e Windows XP. As versões futuras Windows podem alterar o mapeamento entre o parâmetro Timeout e o valor de tempo-máximo em segundos:

| Parâmetro timeout                       | Tempo real em segundos |
|-----------------------------------------|----------------------------|
| 0 (RPC \_ C \_ BINDING MIN \_ \_ TIMEOUT)       | 120                        |
| 1                                       | 240                        |
| 2                                       | 360                        |
| 3                                       | 480                        |
| 4                                       | 600                        |
| 5 (RPC \_ C \_ BINDING DEFAULT \_ \_ TIMEOUT)   | 720                        |
| 6                                       | 840                        |
| 7                                       | 960                        |
| 8                                       | 1080                       |
| 9 (TEMPO MÁXIMO DE \_ ASSOCIAÇÃO DE RPC \_ \_ \_ C)       | 1200                       |
| 10 (RPC \_ C \_ BINDING INFINITE \_ \_ TIMEOUT) | Tempo infinito          |



 

Depois que os keep alives são ligado, o cliente envia um keep alive pacote a cada segundo. Se não houver nenhuma confirmação do servidor para três ou mais keep alives, o cliente declarará a conexão inossa e falhará na chamada de procedimento remoto. Se o servidor enviar uma resposta dentro do tempo de vida especificado, keep alives não será ligado. Se o servidor responder a keep alives, mas não responder à chamada de procedimento remoto, o cliente continuará enviando keep alives. Depois que o servidor responder à chamada RPC, os keep alives serão desligados. Por Windows 2000, keep alives são ativas somente para chamadas RPC síncronas. Por Windows XP, keep alives também são ativas para chamadas RPC assíncronas.

É uma tentação definir keep alives com o valor mais baixo para garantir que o aplicativo cliente responda a problemas de rede em tempo hábil. Deve-se ter uma consideração cuidadosa quanto a tal tentação e aplicar-se a um valor agressivo. Um servidor que perde temporariamente a conectividade pode se encontrar inundado com keep alives de vários clientes depois que a conectividade for restaurada. Além disso, tarefas computacionais longas podem levar mais de dois minutos, e o servidor pode se achar gasto mais tempo de CPU respondendo a keep alives do que executando um trabalho útil. Portanto, keep alives deve ser usado com moderação. Se o cliente não puder tolerar o thread que está sendo vinculado por longos períodos, o RPC assíncrono deverá ser considerado.

Outras sequências de protocolo podem implementar mecanismos diferentes para detectar servidores sem resposta, dependendo de qual transporte é usado. O [**transporte ncalrpc**](/windows/desktop/Midl/ncalrpc) não usa keep alives. Como todas as comunicações no **ncalrpc** são locais, se o servidor ficar sem resposta enquanto uma chamada estiver em andamento, o tempo de executar RPC no cliente falhará imediatamente na chamada.

## <a name="call-time-outs"></a>Tempos de saída de chamada

Os keep alives do TCP são bons se a conectividade de rede for perdida ou se o servidor falhar. Mas se os deadlocks do servidor no modo de usuário, os keep alives do TCP retornarão com êxito, mas a chamada nunca retornará. Para lidar com esse cenário, foi adicionada uma nova opção de tempo de Windows XP: RPC \_ C \_ OPT CALL \_ \_ TIMEOUT. Essa opção instrui o tempo de executar RPC a configurar um temporizador sempre que ele envia uma solicitação para o servidor. Se o temporizador expirar, a chamada será cancelada automaticamente e será concluída com RPC \_ S \_ CALL \_ CANCELLED. Desde que o servidor responda dentro do limite de tempo especificado, o cliente não cancelará a chamada. Isso significa que uma chamada multifragment pode levar mais do que o período de tempo de conclusão, pois cada resposta do servidor é recebida dentro do período de tempo-tempo, mesmo que o período de tempo para todas as respostas chegar seja maior do que o período de tempo-fora.

Além disso, quando uma chamada é cancelada, o servidor não é notificado sobre o cancelamento. O servidor, portanto, provavelmente executará a chamada em algum momento e o cliente simplesmente ignorará a resposta do servidor.

A armadilha mais perigosa com tempos de saída de chamada é estabelecer um curto tempo e repetir a chamada no mesmo servidor. O cenário a seguir ilustra os riscos dessa abordagem:

Imagine um servidor que opera perto da capacidade. Ele tem um número de clientes com tempos decoros muito curtos, como cinco segundos. Uma perda temporária de conectividade de rede ou congestionamento em um roteador causa um desacordo nas respostas do servidor por alguns segundos. Em redes Ethernet, essa situação pode ser facilmente causada por um estouro de atividade em um link que o servidor compartilha com outro computador. O servidor não gerencia o envio de todas as respostas antes do tempo de cinco segundos. Os clientes têm suas chamadas canceladas e tentarão novamente imediatamente. O servidor não está ciente de que as chamadas são recuperações e as executa também. Portanto, em vez de executar sua carga de trabalho normal de chamadas, ele executa de 30 a 50% mais chamadas, dependendo de quantos clientes se foram. Se isso exceder sua capacidade e o servidor não puder responder a todos os clientes dentro de cinco segundos, outra rodada de chamadas será enviada ao servidor. Os clientes continuam emitando as mesmas chamadas e, como o servidor está sobrecarregado processando chamadas anteriores, não é possível responder dentro do tempo-out. Depois de responder, os clientes atingiram o tempo atingido, emitiram uma nova chamada e descartaram a resposta. Na pior das hipóteses, o servidor não será recuperado até a reinicialização e, dependendo do padrão de acesso do cliente, poderá não se recuperar até que um número suficiente de clientes seja interrompido.

> [!Note]  
> Os tempos de tempo de chamada funcionam somente nas sequências de protocolo [**\_ ncacn ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) e [**ncacn \_ http.**](/windows/desktop/Midl/ncacn-http)

 

 

 