---
title: Representação de cliente (RPC)
description: A representação é útil em um ambiente de computação distribuído quando os servidores devem passar solicitações de clientes para outros processos de servidor ou para o sistema operacional.
ms.assetid: 49d833d8-c61c-4746-91cf-c0753847cd3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03ad3b4d9e2984708e8b274ab9bc57c3235808b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084786"
---
# <a name="client-impersonation"></a>Client Impersonation (em inglês)

A representação é útil em um ambiente de computação distribuído quando os servidores devem passar solicitações de clientes para outros processos de servidor ou para o sistema operacional. Nesse caso, um servidor representa o contexto de segurança do cliente. Outros processos de servidor podem manipular a solicitação como se o cliente original o tiver feito.

![o servidor representa um cliente de chamada ao fazer chamadas subsequentes em nome do cliente](images/impr.png)

Por exemplo, um cliente faz uma solicitação para o servidor A. Se o servidor A precisar consultar o servidor B para concluir a solicitação, o servidor A representará o contexto do Client Security e fará a solicitação para o servidor B em nome do cliente. O servidor B usa o contexto de segurança do cliente original, em vez da identidade de segurança do servidor A, para determinar se a tarefa deve ser concluída.

O servidor chama [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) para substituir a segurança do thread do servidor pelo contexto do Client Security. Depois que a tarefa for concluída, o servidor chamará [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself) ou [**RpcRevertToSelfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoselfex) para restaurar o contexto de segurança definido para o thread do servidor.

Ao associar, o cliente pode especificar informações de qualidade de serviço sobre segurança, que especifica como o servidor pode representar o cliente. Por exemplo, uma das configurações permite que o cliente especifique que o servidor não tem permissão para representá-lo. Para obter mais informações, consulte [Quality of Service](quality-of-service.md).

A capacidade de chamar outros servidores enquanto representa o cliente original é chamada de *delegação*. Quando a delegação é usada, um servidor representando um cliente pode chamar outro servidor e pode fazer chamadas de rede com as credenciais do cliente. Ou seja, da perspectiva do segundo servidor, as solicitações provenientes do primeiro servidor são indistinguíveis de solicitações provenientes do cliente. Nem todos os provedores de segurança dão suporte à delegação. A Microsoft envia apenas um provedor de segurança que dá suporte à delegação: Kerberos.

A delegação pode ser um recurso perigoso devido aos privilégios que o cliente fornece ao servidor durante uma chamada de procedimento remoto. É por isso que o Kerberos permite chamadas com o nível de representação de delegação somente se a autenticação mútua for solicitada. Os administradores de domínio podem limitar os computadores aos quais as chamadas com o nível de representação de delegação são feitas para impedir que clientes insuspeitos façam chamadas para servidores que podem abusam suas credenciais.

Existe uma exceção à regra de delegação: chamadas usando [**Ncalrpc**](/windows/desktop/Midl/ncalrpc). Quando essas chamadas são feitas, o servidor Obtém os direitos de delegação, mesmo se um nível de representação de Impersonate for especificado. Ou seja, um servidor pode chamar outros servidores em nome do cliente. Isso funciona apenas para uma chamada remota. Por exemplo, se o cliente A chamar o servidor local LB usando **Ncalrpc** , o servidor local lb pode representar e chamar o servidor remoto RB. O RB poderá agir em nome do cliente A, mas somente no computador remoto em que o RB está sendo executado. Ele não pode fazer outra chamada de rede para o computador remoto C, a menos que LB especifique um nível de representação de delegate quando ele chamou RB.

> [!Note]  
> A *representação* do termo representa dois significados sobrepostos. O primeiro significado da representação é o processo geral de atuar em nome de um cliente. O segundo significado é o nível de representação específico chamado representação. O contexto do texto geralmente esclarece o significado.

 

 

 