---
title: Disponibilizando o servidor na rede
description: Antes que um aplicativo de servidor possa aceitar chamadas de procedimento remotos, ele deve estar disponível na rede.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- RPC de chamada de procedimento remoto, tarefas, disponibilizando o servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005726"
---
# <a name="making-the-server-available-on-the-network"></a>Disponibilizando o servidor na rede

Antes que um aplicativo de servidor possa aceitar chamadas de procedimento remotos, ele deve estar disponível na rede. Para fazer isso, o servidor indica para o tempo de execução RPC que está disposto a aceitar chamadas em uma ou mais sequências de protocolo. Escolhendo as sequências de protocolo que um aplicativo de servidor dá suporte é uma decisão importante; sequências de protocolo diferentes têm recursos muito diferentes. Os servidores que esperam que as chamadas sejam recebidas localmente devem usar **Ncalrpc**. Os servidores que aceitam chamadas remotas devem usar o **\_ \_ TCP IP ncacn**. Os servidores não devem verificar se a sequência de protocolo na qual eles recebem chamadas é a sequência de protocolos na qual eles esperam receber chamadas. Confira cuidado com outros pontos de extremidade RPC em execução no mesmo processo nas melhores práticas de programação RPC para obter mais informações.

O exemplo a seguir usa **ncacn \_ IP \_ TCP**.

A maioria dos programas de servidor usa todas as sequências de protocolo disponíveis na rede. Para fazer isso, eles invocam a função [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) , conforme mostrado no fragmento de código a seguir:


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



O primeiro parâmetro para a função [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) é a sequência de protocolo. O segundo parâmetro depende da sequência de protocolo. Conforme ilustrado no fragmento de código, a maioria dos programas de servidor define esse parâmetro como **RPC \_ C \_ PROTSEQ \_ Max \_ requisitos \_ Default**. Esse valor define a Biblioteca RPC para usar o valor padrão. O terceiro parâmetro é um descritor de segurança e não deve ser usado em aplicativos. Para obter mais informações, consulte [**segurança**](security.md).

Você também pode usar as funções [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)ou [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) .

Depois que um aplicativo de servidor seleciona pelo menos uma sequência de protocolo, os servidores que usam pontos de extremidade dinâmicos devem criar informações de associação para cada sequência de protocolo usada por ele. O servidor armazena as informações de associação em um vetor de associação que pode então exportar para o serviço mapeador de ponto de extremidade.

Use a função [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) para obter um vetor de associação para o aplicativo de servidor, conforme mostrado no exemplo a seguir:


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



O único parâmetro passado para a função [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) é um ponteiro para um ponteiro para uma estrutura de [**\_ \_ vetor de associação RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) . A biblioteca de tempo de execução RPC aloca dinamicamente uma matriz de vetores de ligação e armazena o endereço da matriz na variável de parâmetro (nesse caso, **rpcBindingVector**). Cada aplicativo de servidor é responsável por liberar esse vetor de ligação usando a função [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) depois que ele termina de usá-lo (por exemplo, depois de transmiti-lo para as funções apropriadas).

 

 




