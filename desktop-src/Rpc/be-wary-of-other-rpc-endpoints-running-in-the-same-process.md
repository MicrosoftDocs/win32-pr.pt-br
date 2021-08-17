---
title: Tenha cuidado com outros pontos de extremidade RPC em execução no mesmo processo
description: Quando um aplicativo reside em um processo com outros servidores RPC, todos os aplicativos escutam em todos os protocolos.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e2044b83de96a352546d90c45cd54879fc87923786b7852133ffeb28dbf9cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932347"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a>Tenha cuidado com outros pontos de extremidade RPC em execução no mesmo processo

Quando um aplicativo reside em um processo com outros servidores RPC, todos os aplicativos escutam em todos os protocolos. Dessa forma, se um componente chamar [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* apenas para o LRPC, ele não estará necessariamente acessível apenas pelo LRPC. Ele pode estar acessível em outros protocolos, já que outros servidores RPC no processo podem estar escutando em pipes ou soquetes (por exemplo).

Semelhante a identificadores estritos de contexto, não colocar outro ponto de extremidade no processo não significa que não exista outro ponto de extremidade. Independentemente de como você registra seu servidor, não há nenhuma associação especial entre sua interface e seu ponto de extremidade; todas as interfaces podem ser chamadas em todos os pontos de extremidade nesse processo. Essa é outra razão pela qual o modelo de segurança do ponto de extremidade é ineficaz; se um descritor de segurança for colocado em um ponto de extremidade, os invasores poderão chamar a interface em outro ponto de extremidade.

Para garantir que um processo seja chamado somente em uma sequência de protocolo específica, registre uma função de retorno de chamada de segurança e, nessa função, verifique em qual sequência de protocolo a chamada é feita.

 

 




