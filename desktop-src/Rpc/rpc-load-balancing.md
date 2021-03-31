---
title: Balanceamento de carga RPC
description: Balanceamento de carga RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004961"
---
# <a name="rpc-load-balancing"></a>Balanceamento de carga RPC

O balanceamento de carga RPC da Microsoft destina-se a fornecer uma solução escalonável para cenários que exigem uma alta carga de tráfego [RPC sobre http](remote-procedure-calls-using-rpc-over-http.md) . A principal finalidade do Load Balancer de RPC é garantir que o tráfego RPC/HTTP possa ser atendido por um farm de servidores para melhorar a escalabilidade. Para conseguir isso, o RPC deve garantir que todas as conexões de um processo de cliente sejam atendidas pelo mesmo ponto de extremidade do servidor no farm de servidores. A Load Balancer RPC é implementada como um serviço que é executado em conjunto com o serviço RPC sobre proxy HTTP.

Para habilitar o balanceamento de carga, o serviço de balanceamento de carga RPC em execução em cada um dos servidores se comunica entre si para determinar o servidor preferencial para a conexão inicial do cliente. Esse processo é chamado de arbitragem e ocorre no momento da conexão inicial do cliente. Para reduzir o tráfego entre servidores, o serviço de balanceamento de carga RPC escolhe o ponto de extremidade local para atender à conexão se o cliente ainda não estiver associado a um servidor. Para uma determinada conexão de cliente, o resultado da arbitragem é uma das duas possibilidades:

-   Se o cliente já tiver feito uma conexão, o servidor a receber primeiro a conexão tratará as conexões subsequentes.
-   Se essa for a primeira conexão do cliente, a arbitragem resultará no servidor local que manipula a conexão e, portanto, todas as conexões do cliente. Essas informações, uma vez determinadas, serão confirmadas em outros serviços de Load Balancer de RPC no farm de servidores, informando-os sobre o servidor que lida com todas as solicitações do cliente.

Esta seção fornece uma visão geral do balanceamento de carga RPC nos seguintes tópicos:

-   [Implantando o balanceamento de carga](deploying-load-balancing.md)
-   [Configurando o balanceamento de carga](configuring-load-balancing.md)
-   [Práticas recomendadas de balanceamento de carga](load-balancing-best-practices.md)

## <a name="requirements"></a>Requisitos

O serviço de balanceamento de carga RPC tem suporte em servidores que executam o Windows Server 2008 R2 ou posterior e clientes que executam o Windows 7 ou versões posteriores do Windows.

O serviço de proxy RPC, o serviço de balanceamento de carga RPC e os pontos de extremidade do servidor devem estar em execução no mesmo computador. Além disso, todos os servidores no farm de servidores devem ser capazes de atender ao ponto de extremidade solicitado. Para obter informações sobre como configurar o serviço de proxy RPC e o serviço de balanceamento de carga RPC, consulte [Configurando computadores para RPC sobre http](configuring-computers-for-rpc-over-http.md) e [Configurando o balanceamento de carga](configuring-load-balancing.md), respectivamente.

## <a name="limitations"></a>Limitações

Neste momento, o balanceamento de carga RPC dá suporte a apenas um farm de servidores por recurso. Todos os servidores em todos os farms de servidores também devem ser capazes de atender a todos os recursos.

 

 




