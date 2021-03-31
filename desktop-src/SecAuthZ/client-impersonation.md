---
description: Representação é a capacidade de um thread ser executado usando diferentes informações de segurança do que o processo que possui o thread.
ms.assetid: a3f74372-bdc9-43eb-b72f-7d00a43e78a8
title: Representação do cliente (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e72abb17c9f5f6271f55fbfc77da4f6b93ca2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921151"
---
# <a name="client-impersonation-authorization"></a>Representação do cliente (autorização)

[*Representação*](/windows/desktop/SecGloss/i-gly) é a capacidade de um thread ser executado usando diferentes informações de segurança do que o processo que possui o thread. Normalmente, um thread em um aplicativo de servidor representa um cliente. Isso permite que o thread do servidor atue em nome desse cliente para acessar objetos no servidor ou validar o acesso aos próprios objetos do cliente.

A API do Microsoft Windows fornece as seguintes funções para iniciar uma representação:

-   Um aplicativo de servidor DDE pode chamar a função [**DdeImpersonateClient**](/windows/win32/api/ddeml/nf-ddeml-ddeimpersonateclient) para representar um cliente.
-   Um servidor de pipe nomeado pode chamar a função [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) .
-   Você pode chamar a função [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) para representar o contexto de segurança de um [*token de acesso*](/windows/desktop/SecGloss/a-gly)do usuário conectado.
-   A função [**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself) permite que um thread gere uma cópia de seu próprio token de acesso. Isso é útil quando um aplicativo precisa alterar o contexto de segurança de um único thread. Por exemplo, às vezes, apenas um thread de um processo precisa habilitar um [*privilégio*](/windows/desktop/SecGloss/p-gly).
-   Você pode chamar a função [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken) para fazer com que o thread de destino seja executado no contexto de segurança de um [*token de representação*](/windows/desktop/SecGloss/i-gly)especificado.
-   Um aplicativo de servidor RPC (chamada de procedimento remoto) da Microsoft pode chamar a função [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) para representar um cliente.
-   Um [*pacote de segurança*](/windows/desktop/SecGloss/s-gly) ou servidor de aplicativos pode chamar a função [**ImpersonateSecurityContext**](/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext) para representar um cliente.

Para a maioria dessas impessoas, o thread de representação pode reverter para seu próprio contexto de segurança chamando a função [**RevertToSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) . A exceção é a representação de RPC, na qual o aplicativo do servidor RPC chama [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) ou [**RpcRevertToSelfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex) para reverter para seu próprio contexto de segurança.

 

 
