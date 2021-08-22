---
title: Dicas de desempenho de RPC diversos
description: Esta seção aborda diversas dicas de desempenho para o desenvolvimento de servidores RPC de alto desempenho. Esta seção fornece muitas dicas que se referem ao cliente RPC. Desenvolver um cliente RPC corretamente permite que o servidor RPC execute menos trabalho.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0946b83aae296f7b908babca9135c35a0afe8dbe7588a8292ad66bc19dc6488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928065"
---
# <a name="miscellaneous-rpc-performance-tips"></a>Dicas de desempenho de RPC diversos

Esta seção aborda diversas dicas de desempenho para o desenvolvimento de servidores RPC de alto desempenho. Esta seção fornece muitas dicas que se referem ao cliente RPC. Desenvolver um cliente RPC corretamente permite que o servidor RPC execute menos trabalho.

## <a name="use-kerberos"></a>Usar Kerberos

Se a segurança for usada, use o Kerberos. No lado do servidor, o Kerberos não requer acesso ao KDC. Isso move a carga de trabalho do servidor para o cliente, que fornece servidores de melhor desempenho.

## <a name="use-static-identity-tracking"></a>Usar o rastreamento de identidade estático

Se a segurança for usada, tente usar o rastreamento de identidade estático. O rastreamento de identidade estático é mais barato em termos de uso de recursos do que o controle de identidade dinâmico. Se a identidade do cliente for alterada e o servidor não estiver ciente da alteração, use o controle dinâmico em vez de criar um identificador de associação diferente para cada identidade. Mas se a identidade for a mesma, verifique se a RPC está ciente desse fato para evitar que o RPC faça verificações de identidades alteradas a cada vez.

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a>Usar a função RpcGetAuthorizationContextForClient

se você precisar verificar o acesso no Windows XP, use a função [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) . Os contextos de Authz resultantes permitem verificações de acesso muito rápidas, que são armazenadas em cache de forma eficiente pelo tempo de execução de RPC.

## <a name="do-not-modify-the-token-unless-necessary"></a>Não modifique o token, a menos que seja necessário

Se o controle de identidade dinâmico for usado, não modifique o token de thread/processo, a menos que seja absolutamente necessário. Mesmo que ele seja modificado para as configurações que tinha anteriormente, o token geralmente é suficientemente diferente para o sistema de segurança disparar o estabelecimento de um novo contexto de segurança.

## <a name="consider-mixed-mode-serialization-for-context-handles"></a>Considere a serialização de modo misto para identificadores de contexto

O modo de serialização padrão para o identificador de contexto é serializado (exclusivo). Considere fazer todas as chamadas que não modificam o estado do identificador de contexto no modo de serialização compartilhado. Consulte [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) para obter mais informações.

 

 




