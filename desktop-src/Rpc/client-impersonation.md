---
title: Representação de cliente (RPC)
description: A representação é útil em um ambiente de computação distribuído quando os servidores devem passar solicitações de cliente para outros processos de servidor ou para o sistema operacional.
ms.assetid: 49d833d8-c61c-4746-91cf-c0753847cd3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73061a35c61a22a4d238e902c3dcb298e3ac0affaf4b0929c83311145a684f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022816"
---
# <a name="client-impersonation"></a>Client Impersonation (em inglês)

A representação é útil em um ambiente de computação distribuído quando os servidores devem passar solicitações de cliente para outros processos de servidor ou para o sistema operacional. Nesse caso, um servidor representa o contexto de segurança do cliente. Outros processos de servidor podem lidar com a solicitação como se o cliente original tivesse feito isso.

![O servidor representa um cliente de chamada ao fazer chamadas subsequentes em nome do cliente](images/impr.png)

Por exemplo, um cliente faz uma solicitação ao Servidor A. Se o Servidor A deve consultar o Servidor B para concluir a solicitação, o Servidor A representará o contexto de segurança do cliente e fará a solicitação ao Servidor B em nome do cliente. O servidor B usa o contexto de segurança do cliente original, em vez da identidade de segurança do Servidor A, para determinar se a tarefa deve ser concluída.

O servidor chama [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) para substituir a segurança do thread do servidor pelo contexto de segurança do cliente. Depois que a tarefa for concluída, o servidor [**chamará RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself) ou [**RpcRevertToSelfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoselfex) para restaurar o contexto de segurança definido para o thread do servidor.

Ao vincular, o cliente pode especificar informações de qualidade de serviço sobre segurança que especifica como o servidor pode representar o cliente. Por exemplo, uma das configurações permite que o cliente especifique que o servidor não tem permissão para representá-lo. Para obter mais informações, consulte [Qualidade de serviço.](quality-of-service.md)

A capacidade de chamar outros servidores ao representar o cliente original é chamada de *delegação*. Quando a delegação é usada, um servidor que representa um cliente pode chamar outro servidor e pode fazer chamadas de rede com as credenciais do cliente. Ou seja, da perspectiva do segundo servidor, as solicitações provenientes do primeiro servidor são indistinguíveis de solicitações provenientes do cliente. Nem todos os provedores de segurança suportam a delegação. A Microsoft envia apenas um provedor de segurança que dá suporte à delegação: Kerberos.

A delegação pode ser uma funcionalidade perigosa devido aos privilégios que o cliente concede ao servidor durante uma chamada de procedimento remoto. É por isso que o Kerberos permite chamadas com o nível de representação de delegação somente se a autenticação mútua for solicitada. Os administradores de domínio podem limitar os computadores aos quais as chamadas com o nível de representação de delegação são feitas para impedir que clientes não suspeitos fazem chamadas a servidores que poderiam violar suas credenciais.

Existe uma exceção para a regra de delegação: chamadas usando [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Quando essas chamadas são feitas, o servidor obtém direitos de delegação, mesmo que um nível de representação de representação seja especificado. Ou seja, um servidor pode chamar outros servidores em nome do cliente. Isso funciona apenas para uma chamada remota. Por exemplo, se o cliente A chamar LB do servidor local usando **ncalrpc,** o LB do servidor local poderá representar e chamar o RB do servidor remoto. O RB poderá agir em nome do cliente A, mas somente no computador remoto em que o RB está sendo executado. Ele não pode fazer outra chamada de rede para o computador remoto C, a menos que LB especifique um nível de representação de delegado quando ele chamou RB.

> [!Note]  
> O termo *representação representa* dois significados sobrepostos. O primeiro significado da representação é o processo geral de agir em nome de um cliente. O segundo significado é o nível de representação específico chamado representação. O contexto do texto geralmente esclarece o significado.

 

 

 