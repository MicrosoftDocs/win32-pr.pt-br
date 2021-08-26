---
title: Balanceamento de carga RPC
description: Balanceamento de carga RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7fbace237f6d86ebadf3fadc5f3b376d94799b137153b114bc07fead3d64b09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101646"
---
# <a name="rpc-load-balancing"></a>Balanceamento de carga RPC

O Balanceamento de Carga RPC da Microsoft destina-se a fornecer uma solução escalonável para cenários que exigem uma alta carga [de RPC por tráfego HTTP.](remote-procedure-calls-using-rpc-over-http.md) O RPC Load Balancer principal finalidade do RPC é garantir que o tráfego RPC/HTTP possa ser atendido por um farm de servidores para melhorar a escalabilidade. Para fazer isso, o RPC deve garantir que todas as conexões de um processo de cliente sejam a serviço pelo mesmo ponto de extremidade do servidor no farm de servidores. O RPC Load Balancer é implementado como um serviço que é executado em conjunto com o serviço RPC sobre Proxy HTTP.

Para habilitar o balanceamento de carga, o serviço de Balanceamento de Carga RPC em execução em cada um dos servidores se comunica entre si para determinar o servidor preferencial para a conexão inicial do cliente. Esse processo é chamado de arbitragem e ocorre no momento da conexão inicial do cliente. Para reduzir o tráfego entre servidores, o serviço de Balanceamento de Carga RPC escolherá o ponto de extremidade local para a conexão se o cliente ainda não estiver associado a um servidor. Para uma determinada conexão de cliente, o resultado da mediação é uma das duas possibilidades:

-   Se o cliente já tiver feito uma conexão, o servidor para primeiro receber a conexão manipulará as conexões subsequentes.
-   Se essa for a primeira conexão do cliente, a mediação resultará no servidor local que está tratando a conexão e, portanto, todas as conexões do cliente. Essas informações, uma vez determinadas, serão comprometidas com outros serviços de Load Balancer RPC no farm de servidores, informando assim que o servidor está tratando todas as solicitações do cliente.

Esta seção fornece uma visão geral do Balanceamento de Carga RPC nos seguintes tópicos:

-   [Implantando o balanceamento de carga](deploying-load-balancing.md)
-   [Configurando o balanceamento de carga](configuring-load-balancing.md)
-   [Práticas recomendadas de balanceamento de carga](load-balancing-best-practices.md)

## <a name="requirements"></a>Requisitos

O serviço de Balanceamento de Carga RPC tem suporte em servidores que executam o Windows Server 2008 R2 ou posterior e clientes que executam o Windows 7 ou versões posteriores do Windows.

O serviço proxy RPC, o serviço de Balanceamento de Carga RPC e os pontos de extremidade do servidor devem estar todos em execução no mesmo computador. Além disso, todos os servidores no farm de servidores devem ser capazes de atender ao ponto de extremidade solicitado. Para obter informações sobre como configurar o serviço proxy RPC e o serviço de Balanceamento de Carga RPC, consulte [Configuring Computers for RPC over HTTP](configuring-computers-for-rpc-over-http.md) e [Configuring Load Balancing](configuring-load-balancing.md), respectivamente.

## <a name="limitations"></a>Limitações

Neste momento, o Balanceamento de Carga RPC dá suporte a apenas um farm de servidores por recurso. Todos os servidores em todos os farms de servidores também devem ser capazes de atender a todos os recursos.

 

 




