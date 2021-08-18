---
title: Escrevendo um cliente ou servidor RPC seguro
description: Esta seção fornece recomendações de melhores práticas para escrever um cliente ou servidor RPC seguro.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- RPC de Chamada de Procedimento Remoto , práticas recomendadas, escrevendo um cliente ou servidor seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b752d8dab216691105e428833c83bce28b974f121ddcc77861fbb6671d72dd22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010384"
---
# <a name="writing-a-secure-rpc-client-or-server"></a>Escrevendo um cliente ou servidor RPC seguro

Esta seção fornece recomendações de melhores práticas para escrever um cliente ou servidor RPC seguro.

As informações nesta seção se aplica ao Windows 2000 e Windows XP. Esta seção se aplica a todas as sequências de protocolo, incluindo [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Os desenvolvedores tendem a pensar que **ncalrpc** não é um destino provável para um ataque, o que não é verdadeiro em um servidor terminal em que potencialmente centenas de usuários têm acesso a um serviço e comprometer ou até mesmo colocar um serviço para baixo pode levar à aquisição de acesso extra.

Esta seção é dividida nos seguintes tópicos:

-   [Qual provedor de segurança usar](which-security-provider-to-use.md)
-   [Controlando a autenticação do cliente](controlling-client-authentication.md)
-   [Escolhendo um nível de autenticação](choosing-an-authentication-level.md)
-   [Escolhendo opções de QOS de segurança](choosing-security-qos-options.md)
-   [Erro comum: supondo que RpcServerRegisterAuthInfo impeça usuários não autorizados de chamar seu servidor](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [Retornos de chamada](callbacks.md)
-   [Sessões nulas](null-sessions.md)
-   [Usar o sinalizador /robust](use-the-robust-flag.md)
-   [Técnicas de IDL para melhor interface e design de método](idl-techniques-for-better-interface-and-method-design.md)
-   [Identificador de contexto estrito e de tipo estrito](strict-and-type-strict-context-handles.md)
-   [Não confiar em seu par](do-not-trust-your-peer.md)
-   [Não usar a segurança do ponto de extremidade](do-not-use-endpoint-security.md)
-   [Seja cuidado com outros pontos de extremidade RPC em execução no mesmo processo](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [Verifique se o servidor está Who ele declara ser](verify-the-server-is-who-it-claims-to-be.md)
-   [Usar sequências de protocolo base](use-mainstream-protocol-sequences.md)
-   [Qual é a segurança do meu servidor RPC agora?](how-secure-is-my-rpc-server-now.md)

 

 