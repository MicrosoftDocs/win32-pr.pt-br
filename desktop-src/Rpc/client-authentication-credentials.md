---
title: Credenciais de autenticação de cliente
description: Cada cliente autenticado deve fornecer credenciais de autenticação para o servidor.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3704663411fc33340a462d8e3b356041b6061468
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006095"
---
# <a name="client-authentication-credentials"></a>Credenciais de autenticação de cliente

Cada cliente autenticado deve fornecer credenciais de autenticação para o servidor. No RPC, o cliente armazena suas credenciais de autenticação na associação entre o cliente e o servidor. Para fazer isso, o cliente chama [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).

Há dois tipos de credenciais — implícita e explícita:

-   Credenciais explícitas existem quando o cliente fornece nome de usuário, senha e domínio.
-   Existem credenciais implícitas quando o cliente usa credenciais do thread ou do token de processo chamando as funções **RpcBindingSetAuthInfo** ou **RpcBindingSetAuthInfoEx** .

Os clientes devem impedir o fornecimento de credenciais explícitas, pois armazenar, manipular e recuperar uma senha de usuário pode introduzir uma vulnerabilidade de segurança em um sistema distribuído se credenciais explícitas forem usadas.

Para usar credenciais implícitas, o cliente chama **RpcBindingSetAuthInfo**(*ex*). O sistema de segurança e RPC obtêm credenciais do thread ou do token de processo para uso na sessão de autenticação.

Se o cliente usar credenciais explícitas, o quinto parâmetro dessas duas funções será do tipo [**\_ identificador de \_ identidade \_ de autenticação RPC**](rpc-auth-identity-handle.md). Esse é um tipo flexível que é um ponteiro para uma estrutura de dados. O conteúdo da estrutura de dados pode ser diferente em cada serviço de autenticação. Atualmente, os SSPs que o RPC dá suporte exigem que seu aplicativo defina o **\_ identificador de \_ identidade \_ de autenticação RPC** para apontar para uma estrutura de [**\_ \_ \_ identidade de autenticação WinNT SEC**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) . A estrutura de **\_ \_ \_ identidade de autenticação WinNT SEC** contém campos para um nome de usuário, domínio e senha.

 

 




