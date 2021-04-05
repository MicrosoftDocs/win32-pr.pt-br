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
# <a name="writing-a-secure-rpc-client-or-server"></a><span data-ttu-id="158f7-104">Gravando um cliente ou servidor RPC seguro</span><span class="sxs-lookup"><span data-stu-id="158f7-104">Writing a Secure RPC Client or Server</span></span>

<span data-ttu-id="158f7-105">Esta seção fornece recomendações de práticas recomendadas para a gravação de um cliente ou servidor RPC seguro.</span><span class="sxs-lookup"><span data-stu-id="158f7-105">This section provides best practice recommendations for writing a secure RPC client or server.</span></span>

<span data-ttu-id="158f7-106">As informações contidas nesta seção aplicam-se ao Windows 2000 e ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="158f7-106">The information in this section applies to Windows 2000 and Windows XP.</span></span> <span data-ttu-id="158f7-107">Esta seção se aplica a todas as sequências de protocolo, incluindo [**Ncalrpc**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="158f7-107">This section applies to all protocol sequences, including [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="158f7-108">Os desenvolvedores tendem a acreditar que o **Ncalrpc** não é um alvo provável para um ataque, o que não é verdade em um servidor de terminal no qual potencialmente centenas de usuários têm acesso a um serviço, e a comprometimento ou até mesmo a redução de um serviço pode levar à aquisição de acesso extra.</span><span class="sxs-lookup"><span data-stu-id="158f7-108">Developers tend to think **ncalrpc** is not a probable target for an attack, which is not true on a terminal server where potentially hundreds of users have access to a service, and compromising or even bringing down a service can lead to acquiring extra access.</span></span>

<span data-ttu-id="158f7-109">Esta seção é dividida nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="158f7-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="158f7-110">Qual provedor de segurança usar</span><span class="sxs-lookup"><span data-stu-id="158f7-110">Which Security Provider To Use</span></span>](which-security-provider-to-use.md)
-   [<span data-ttu-id="158f7-111">Controlando a autenticação do cliente</span><span class="sxs-lookup"><span data-stu-id="158f7-111">Controlling Client Authentication</span></span>](controlling-client-authentication.md)
-   [<span data-ttu-id="158f7-112">Escolhendo um nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="158f7-112">Choosing an Authentication Level</span></span>](choosing-an-authentication-level.md)
-   [<span data-ttu-id="158f7-113">Escolhendo as opções de QOS de segurança</span><span class="sxs-lookup"><span data-stu-id="158f7-113">Choosing Security QOS Options</span></span>](choosing-security-qos-options.md)
-   [<span data-ttu-id="158f7-114">Erro comum: supondo que RpcServerRegisterAuthInfo impede que usuários não autorizados chamem seu servidor</span><span class="sxs-lookup"><span data-stu-id="158f7-114">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [<span data-ttu-id="158f7-115">Retornos de chamada</span><span class="sxs-lookup"><span data-stu-id="158f7-115">Callbacks</span></span>](callbacks.md)
-   [<span data-ttu-id="158f7-116">Sessões nulas</span><span class="sxs-lookup"><span data-stu-id="158f7-116">Null Sessions</span></span>](null-sessions.md)
-   [<span data-ttu-id="158f7-117">Usar o sinalizador/robust</span><span class="sxs-lookup"><span data-stu-id="158f7-117">Use the /robust Flag</span></span>](use-the-robust-flag.md)
-   [<span data-ttu-id="158f7-118">Técnicas de IDL para melhor design de interface e de método</span><span class="sxs-lookup"><span data-stu-id="158f7-118">IDL Techniques for Better Interface and Method Design</span></span>](idl-techniques-for-better-interface-and-method-design.md)
-   [<span data-ttu-id="158f7-119">Identificadores de contexto estrito e de tipo estrito</span><span class="sxs-lookup"><span data-stu-id="158f7-119">Strict and Type Strict Context Handles</span></span>](strict-and-type-strict-context-handles.md)
-   [<span data-ttu-id="158f7-120">Não confie no seu par</span><span class="sxs-lookup"><span data-stu-id="158f7-120">Do Not Trust Your Peer</span></span>](do-not-trust-your-peer.md)
-   [<span data-ttu-id="158f7-121">Não usar a segurança do ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="158f7-121">Do Not Use Endpoint Security</span></span>](do-not-use-endpoint-security.md)
-   [<span data-ttu-id="158f7-122">Tenha cuidado com outros pontos de extremidade RPC em execução no mesmo processo</span><span class="sxs-lookup"><span data-stu-id="158f7-122">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [<span data-ttu-id="158f7-123">Verifique se o servidor é quem alega ser</span><span class="sxs-lookup"><span data-stu-id="158f7-123">Verify The Server Is Who It Claims To Be</span></span>](verify-the-server-is-who-it-claims-to-be.md)
-   [<span data-ttu-id="158f7-124">Usar sequências de protocolo principais</span><span class="sxs-lookup"><span data-stu-id="158f7-124">Use Mainstream Protocol Sequences</span></span>](use-mainstream-protocol-sequences.md)
-   [<span data-ttu-id="158f7-125">Qual a segurança do meu servidor RPC agora?</span><span class="sxs-lookup"><span data-stu-id="158f7-125">How Secure is my RPC Server Now?</span></span>](how-secure-is-my-rpc-server-now.md)

 

 