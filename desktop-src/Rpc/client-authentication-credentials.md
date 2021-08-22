---
title: Credenciais de autenticação do cliente
description: Cada cliente autenticado deve fornecer credenciais de autenticação para o servidor.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2410b073886ffd70409cd749ea90305faa8d4635754e8f9596547c47bb976800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932182"
---
# <a name="client-authentication-credentials"></a>Credenciais de autenticação do cliente

Cada cliente autenticado deve fornecer credenciais de autenticação para o servidor. Em RPC, o cliente armazena suas credenciais de autenticação na associação entre o cliente e o servidor. Para fazer isso, o cliente chama [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)

Há dois tipos de credenciais – implícitas e explícitas:

-   As credenciais explícitas existem quando o cliente fornece nome de usuário, senha e domínio.
-   As credenciais implícitas existem quando o cliente usa credenciais do token de thread ou processo chamando as funções **RpcBindingSetAuthInfo** ou **RpcBindingSetAuthInfoEx.**

Os clientes devem evitar fornecer credenciais explícitas porque armazenar, manipular e recuperar uma senha de usuário poderá introduzir uma vulnerabilidade de segurança em um sistema distribuído se as credenciais explícitas são usadas.

Para usar credenciais implícitas, o cliente **chama RpcBindingSetAuthInfo**(*ex).* O sistema de segurança e o RPC obtém credenciais do token de thread ou processo para uso na sessão de autenticação.

Se o cliente usar credenciais explícitas, o quinto parâmetro dessas duas funções será do tipo [**RPC \_ AUTH \_ IDENTITY \_ HANDLE**](rpc-auth-identity-handle.md). Esse é um tipo flexível que é um ponteiro para uma estrutura de dados. O conteúdo da estrutura de dados pode ser diferente com cada serviço de autenticação. Atualmente, os SSPs compatíveis com RPC exigem que seu aplicativo de conjunto **RPC \_ AUTH \_ IDENTITY \_ HANDLE** aponte para uma estrutura DE IDENTIDADE DE [**\_ AUTH WINNT \_ \_ SEC.**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) A **estrutura \_ SEC WINNT \_ AUTH \_ IDENTITY** contém campos para um nome de usuário, domínio e senha.

 

 




