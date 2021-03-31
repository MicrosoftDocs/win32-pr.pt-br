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
# <a name="client-authentication-credentials"></a><span data-ttu-id="7ac2a-103">Credenciais de autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="7ac2a-103">Client Authentication Credentials</span></span>

<span data-ttu-id="7ac2a-104">Cada cliente autenticado deve fornecer credenciais de autenticação para o servidor.</span><span class="sxs-lookup"><span data-stu-id="7ac2a-104">Each authenticated client must provide authentication credentials to the server.</span></span> <span data-ttu-id="7ac2a-105">No RPC, o cliente armazena suas credenciais de autenticação na associação entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="7ac2a-105">Under RPC, the client stores its authentication credentials in the binding between the client and the server.</span></span> <span data-ttu-id="7ac2a-106">Para fazer isso, o cliente chama [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span><span class="sxs-lookup"><span data-stu-id="7ac2a-106">To do this, the client calls [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span></span>

<span data-ttu-id="7ac2a-107">Há dois tipos de credenciais — implícita e explícita:</span><span class="sxs-lookup"><span data-stu-id="7ac2a-107">There are two types of credentials—implicit and explicit:</span></span>

-   <span data-ttu-id="7ac2a-108">Credenciais explícitas existem quando o cliente fornece nome de usuário, senha e domínio.</span><span class="sxs-lookup"><span data-stu-id="7ac2a-108">Explicit credentials exist when the client supplies username, password, and domain.</span></span>
-   <span data-ttu-id="7ac2a-109">Existem credenciais implícitas quando o cliente usa credenciais do thread ou do token de processo chamando as funções **RpcBindingSetAuthInfo** ou **RpcBindingSetAuthInfoEx** .</span><span class="sxs-lookup"><span data-stu-id="7ac2a-109">Implicit credentials exist when the client uses credentials from the thread or process token calling the **RpcBindingSetAuthInfo** or **RpcBindingSetAuthInfoEx** functions.</span></span>

<span data-ttu-id="7ac2a-110">Os clientes devem impedir o fornecimento de credenciais explícitas, pois armazenar, manipular e recuperar uma senha de usuário pode introduzir uma vulnerabilidade de segurança em um sistema distribuído se credenciais explícitas forem usadas.</span><span class="sxs-lookup"><span data-stu-id="7ac2a-110">Clients should refrain from supplying explicit credentials because storing, manipulating, and retrieving a user password can introduce a security vulnerability into a distributed system if explicit credentials are used.</span></span>

<span data-ttu-id="7ac2a-111">Para usar credenciais implícitas, o cliente chama **RpcBindingSetAuthInfo**(*ex*).</span><span class="sxs-lookup"><span data-stu-id="7ac2a-111">To use implicit credentials, the client calls **RpcBindingSetAuthInfo**(*Ex*).</span></span> <span data-ttu-id="7ac2a-112">O sistema de segurança e RPC obtêm credenciais do thread ou do token de processo para uso na sessão de autenticação.</span><span class="sxs-lookup"><span data-stu-id="7ac2a-112">The security system and RPC obtain credentials from the thread or process token for use in the authentication session.</span></span>

<span data-ttu-id="7ac2a-113">Se o cliente usar credenciais explícitas, o quinto parâmetro dessas duas funções será do tipo [**\_ identificador de \_ identidade \_ de autenticação RPC**](rpc-auth-identity-handle.md).</span><span class="sxs-lookup"><span data-stu-id="7ac2a-113">If the client uses explicit credentials, the fifth parameter of these two functions is of type [**RPC\_AUTH\_IDENTITY\_HANDLE**](rpc-auth-identity-handle.md).</span></span> <span data-ttu-id="7ac2a-114">Esse é um tipo flexível que é um ponteiro para uma estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="7ac2a-114">This is a flexible type that is a pointer to a data structure.</span></span> <span data-ttu-id="7ac2a-115">O conteúdo da estrutura de dados pode ser diferente em cada serviço de autenticação.</span><span class="sxs-lookup"><span data-stu-id="7ac2a-115">The contents of the data structure can differ with each authentication service.</span></span> <span data-ttu-id="7ac2a-116">Atualmente, os SSPs que o RPC dá suporte exigem que seu aplicativo defina o **\_ identificador de \_ identidade \_ de autenticação RPC** para apontar para uma estrutura de [**\_ \_ \_ identidade de autenticação WinNT SEC**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) .</span><span class="sxs-lookup"><span data-stu-id="7ac2a-116">Currently, the SSPs that RPC supports require that your application set **RPC\_AUTH\_IDENTITY\_HANDLE** to point to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) structure.</span></span> <span data-ttu-id="7ac2a-117">A estrutura de **\_ \_ \_ identidade de autenticação WinNT SEC** contém campos para um nome de usuário, domínio e senha.</span><span class="sxs-lookup"><span data-stu-id="7ac2a-117">The **SEC\_WINNT\_AUTH\_IDENTITY** structure contains fields for a user name, domain, and password.</span></span>

 

 




