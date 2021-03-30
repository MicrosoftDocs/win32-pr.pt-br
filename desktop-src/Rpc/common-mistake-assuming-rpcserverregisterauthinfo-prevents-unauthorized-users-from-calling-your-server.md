---
title: Erro comum supondo que RpcServerRegisterAuthInfo impede que usuários não autorizados chamem seu servidor
description: Quando os provedores de segurança são registrados no servidor com a função RpcServerRegisterAuthInfo, uma opção é adicionada, não um requisito.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636848"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a><span data-ttu-id="a6c1a-103">Erro comum: supondo que RpcServerRegisterAuthInfo impede que usuários não autorizados chamem seu servidor</span><span class="sxs-lookup"><span data-stu-id="a6c1a-103">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>

<span data-ttu-id="a6c1a-104">Quando os provedores de segurança são registrados no servidor com a função [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) , uma opção é adicionada, não um requisito.</span><span class="sxs-lookup"><span data-stu-id="a6c1a-104">When security providers are registered on the server with the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function, an option is added, not a requirement.</span></span> <span data-ttu-id="a6c1a-105">Isso significa que os registros anteriores com **RpcServerRegisterAuthInfo** não são substituídos.</span><span class="sxs-lookup"><span data-stu-id="a6c1a-105">This means previous registrations with **RpcServerRegisterAuthInfo** are not replaced.</span></span> <span data-ttu-id="a6c1a-106">Isso também significa que clientes não autenticados ainda podem se conectar.</span><span class="sxs-lookup"><span data-stu-id="a6c1a-106">This also means unauthenticated clients still can connect.</span></span> <span data-ttu-id="a6c1a-107">Chamando a função **RpcServerRegisterAuthInfo** , os clientes não autenticados não são permitidos da conexão; Eles ainda podem se conectar, mas chamadas de função, como [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) , falharão.</span><span class="sxs-lookup"><span data-stu-id="a6c1a-107">By calling the **RpcServerRegisterAuthInfo** function, unauthenticated clients are not disallowed from connecting; they can still connect, but function calls such as [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) will fail.</span></span> <span data-ttu-id="a6c1a-108">Assim, quando a função **RpcServerRegisterAuthInfo** é chamada, os invasores potenciais não foram desfeitos — em vez disso, os clientes que precisam ter acesso têm a oportunidade de provar sua identidade.</span><span class="sxs-lookup"><span data-stu-id="a6c1a-108">So when the **RpcServerRegisterAuthInfo** function is called, potential attackers have not been weeded out—rather, clients that ought to have access are given a chance to prove their identity.</span></span> <span data-ttu-id="a6c1a-109">As verificações ainda devem estar em vigor para determinar se os invasores potenciais estão tentando se conectar.</span><span class="sxs-lookup"><span data-stu-id="a6c1a-109">Checks must still be in place to determine whether potential attackers are attempting to connect.</span></span>

 

 




