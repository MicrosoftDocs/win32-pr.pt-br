---
title: Gravando um cliente ou servidor RPC seguro
description: Esta seção fornece recomendações de práticas recomendadas para a gravação de um cliente ou servidor RPC seguro.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, gravando um cliente ou servidor seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007911"
---
# <a name="writing-a-secure-rpc-client-or-server"></a>Gravando um cliente ou servidor RPC seguro

Esta seção fornece recomendações de práticas recomendadas para a gravação de um cliente ou servidor RPC seguro.

As informações contidas nesta seção aplicam-se ao Windows 2000 e ao Windows XP. Esta seção se aplica a todas as sequências de protocolo, incluindo [**Ncalrpc**](/windows/desktop/Midl/ncalrpc). Os desenvolvedores tendem a acreditar que o **Ncalrpc** não é um alvo provável para um ataque, o que não é verdade em um servidor de terminal no qual potencialmente centenas de usuários têm acesso a um serviço, e a comprometimento ou até mesmo a redução de um serviço pode levar à aquisição de acesso extra.

Esta seção é dividida nos seguintes tópicos:

-   [Qual provedor de segurança usar](which-security-provider-to-use.md)
-   [Controlando a autenticação do cliente](controlling-client-authentication.md)
-   [Escolhendo um nível de autenticação](choosing-an-authentication-level.md)
-   [Escolhendo as opções de QOS de segurança](choosing-security-qos-options.md)
-   [Erro comum: supondo que RpcServerRegisterAuthInfo impede que usuários não autorizados chamem seu servidor](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [Retornos de chamada](callbacks.md)
-   [Sessões nulas](null-sessions.md)
-   [Usar o sinalizador/robust](use-the-robust-flag.md)
-   [Técnicas de IDL para melhor design de interface e de método](idl-techniques-for-better-interface-and-method-design.md)
-   [Identificadores de contexto estrito e de tipo estrito](strict-and-type-strict-context-handles.md)
-   [Não confie no seu par](do-not-trust-your-peer.md)
-   [Não usar a segurança do ponto de extremidade](do-not-use-endpoint-security.md)
-   [Tenha cuidado com outros pontos de extremidade RPC em execução no mesmo processo](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [Verifique se o servidor é quem alega ser](verify-the-server-is-who-it-claims-to-be.md)
-   [Usar sequências de protocolo principais](use-mainstream-protocol-sequences.md)
-   [Qual a segurança do meu servidor RPC agora?](how-secure-is-my-rpc-server-now.md)

 

 