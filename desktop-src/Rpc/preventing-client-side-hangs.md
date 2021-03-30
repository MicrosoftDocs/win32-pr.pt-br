---
title: Prevenção de suspensões do lado do cliente
description: Há duas maneiras pelas quais o cliente pode interromper a conectividade de rede pode fazer com que as solicitações do servidor se tornem perdidas ou o próprio servidor pode falhar. Com as opções padrão, o RPC nunca atingirá o tempo limite de uma chamada e o thread do cliente aguardará para uma resposta de forma contínua.
ms.assetid: 2c201e29-9d9c-48e6-b0b5-68e4b25c3fb7
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, impedindo o travamento do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d4b5fc92ca18b575d081cd7b5abf90929e7df5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641221"
---
# <a name="preventing-client-side-hangs"></a>Prevenção de suspensões do lado do cliente

Há duas maneiras pelas quais o cliente pode travar: a conectividade de rede pode fazer com que as solicitações do servidor se tornem perdidas ou o próprio servidor pode falhar. Com as opções padrão, o RPC nunca atingirá o tempo limite de uma chamada e o thread do cliente aguardará para uma resposta de forma contínua.

Há dois métodos para evitar isso: Mantenha alives e tempos limite.

## <a name="tcp-keep-alives"></a>TCP Keep Alive

O cliente pode ser configurado para executar ping no servidor periodicamente para garantir que o servidor esteja ativo e em execução. Os pings são TCP Keep-Alive para as sequências de protocolo [**\_ http**](/windows/desktop/Midl/ncacn-http) TCP e ncacn de [**\_ \_ IP ncacn**](/windows/desktop/Midl/ncacn-ip-tcp) e, dessa forma, são eficientes na utilização da CPU e na largura de banda da rede. Para habilitar o Keep Alive em uma determinada chamada de procedimento remoto, use a função [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) antes de a chamada ser iniciada. Essa função usa um identificador de associação e um tempo limite como argumentos. Cada chamada de procedimento remoto nesse identificador de ligação após **RpcMgmtSetComTimeout** usa o tempo limite fornecido.

O parâmetro Timeout para a função [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) especifica por quanto tempo a execução de RPC espera antes de ativar Keep Alive. O tempo limite é um valor entre 0 e 10, em que 0 é o tempo limite mínimo e 10 é o tempo limite infinito (sem tempo limite). O tempo limite em si não é em segundos; a conversão do valor de tempo limite fornecido para a função **RpcMgmtSetComTimeout** para segundos é feita pelo tempo de execução de RPC e é específica da implementação.

A tabela a seguir fornece a tradução para segundos para o Windows 2000 e o Windows XP. Versões futuras do Windows podem alterar o mapeamento entre o parâmetro Timeout e o valor de tempo limite em segundos:

| Parâmetro Timeout                       | Tempo limite real em segundos |
|-----------------------------------------|----------------------------|
| 0 ( \_ \_ \_ tempo limite mínimo de associação RPC C \_ )       | 120                        |
| 1                                       | 240                        |
| 2                                       | 360                        |
| 3                                       | 480                        |
| 4                                       | 600                        |
| 5 ( \_ \_ \_ tempo limite padrão de associação RPC C \_ )   | 720                        |
| 6                                       | 840                        |
| 7                                       | 960                        |
| 8                                       | 1080                       |
| 9 ( \_ \_ \_ tempo limite máximo de associação RPC C \_ )       | 1200                       |
| 10 ( \_ \_ \_ tempo limite infinito de associação RPC C \_ ) | Tempo limite infinito          |



 

Quando os keep alives são ativados, o cliente envia um pacote Keep Alive a cada segundo. Se não houver nenhuma confirmação do servidor para três ou mais Keep Alive, o cliente declara a conexão inativa e falha na chamada de procedimento remoto. Se o servidor enviar uma resposta dentro do tempo limite especificado, o Keep Alive não será ativado. Se o servidor responder ao Keep Alive, mas não responder à chamada de procedimento remoto, o cliente continuará enviando Keep Alive. Depois que o servidor responde à chamada RPC, as keep alives são desativadas. Para o Windows 2000, Keep Alives são ativados apenas para chamadas RPC síncronas. Para o Windows XP, os keep alives também são ativados para chamadas RPC assíncronas.

É tentador definir keep alives para o valor mais baixo para garantir que o aplicativo cliente responda a problemas de rede em tempo hábil. Uma consideração cuidadosa deve ser dada a essa tentação e fiscalização aplicada a se um valor agressivo é garantido. Um servidor que perde temporariamente a conectividade pode se encontrar inundado com Keep Alive de vários clientes quando a conectividade é restaurada. Além disso, tarefas computacionais longas podem levar mais de dois minutos, e o servidor pode se perder mais tempo de CPU respondendo manter ativos do que a execução de um trabalho útil. Portanto, Keep Alives devem ser usados com moderação. Se o cliente não puder tolerar seu thread sendo ligado por longos períodos, o RPC assíncrono deverá ser considerado.

Outras sequências de protocolo podem implementar diferentes mecanismos para detectar servidores sem resposta, dependendo de qual transporte é usado. O transporte [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) não usa keep alives. Como todas as comunicações em **Ncalrpc** são locais, se o servidor ficar sem resposta enquanto uma chamada estiver em andamento, o tempo de execução de RPC no cliente falhará imediatamente na chamada.

## <a name="call-time-outs"></a>Tempo limite de chamada

O TCP Keep Alive será suficiente se a conectividade de rede for perdida ou se o servidor falhar. Mas se o servidor tiver deadlocks no modo de usuário, o TCP Keep Alives retornará com êxito, mas a chamada nunca será retornada. Para lidar com esse cenário, uma nova opção de tempo de execução foi adicionada ao Windows XP: \_ tempo limite de chamada de aceitação de RPC C \_ \_ \_ . Essa opção instrui o tempo de execução de RPC a configurar um temporizador sempre que ele envia uma solicitação ao servidor. Se o temporizador expirar, a chamada será automaticamente cancelada e concluída com a \_ chamada RPC S \_ \_ cancelada. Desde que o servidor responda dentro do limite de tempo especificado, o cliente não cancelará a chamada. Isso significa que uma chamada de multifrags pode levar mais do que o período de tempo limite para ser concluída, uma vez que cada resposta do servidor é recebida dentro do período de tempo limite, mesmo que o período para que todas as respostas cheguem seja maior que o período de tempo limite.

Além disso, quando uma chamada é cancelada, o servidor não é notificado do cancelamento. O servidor, portanto, provavelmente executará a chamada em algum momento, e o cliente simplesmente irá ignorar a resposta do servidor.

A armadilha mais perigosa com tempos limite de chamada é estabelecer um curto tempo limite e repetir a chamada no mesmo servidor. O cenário a seguir ilustra os perigos dessa abordagem:

Imagine um servidor que opere perto da capacidade. Ele tem vários clientes com tempo limite muito curto, como cinco segundos. Uma perda temporária de conectividade de rede ou congestionamento em um roteador faz com que um lapso no servidor responda por alguns segundos. Em redes Ethernet, essa situação pode ser facilmente causada por uma intermitência de atividade em um link que o servidor compartilha com outra máquina. O servidor não é gerenciado para enviar todas as respostas antes do tempo limite de cinco segundos. Os clientes obtêm suas chamadas canceladas e imediatamente tentam novamente. O servidor não está ciente de que as chamadas são repetições e as executa também. Portanto, em vez de executar sua carga de trabalho normal de chamadas, ele executa 30-50% mais chamadas, dependendo de quantos clientes atingiram o tempo limite. Se isso exceder sua capacidade e o servidor não puder responder a todos os clientes em cinco segundos, outra rodada de chamadas será enviada ao servidor. Os clientes continuam reemitindo as mesmas chamadas e, como o servidor está sobrecarregado processando chamadas anteriores, não é possível responder dentro do tempo limite. Depois de responder, os clientes atingiram o tempo limite, emitiram uma nova chamada e descartaram a resposta. Em um cenário de pior caso, o servidor não será recuperado até a reinicialização e, dependendo do padrão de acesso do cliente, poderá não se recuperar até que um número suficiente de clientes seja interrompido.

> [!Note]  
> O tempo limite de chamada funciona apenas nas sequências de [**protocolo \_ http**](/windows/desktop/Midl/ncacn-http) TCP e ncacn de [**\_ \_ IP ncacn**](/windows/desktop/Midl/ncacn-ip-tcp) .

 

 

 