---
title: Qual provedor de segurança usar
description: Todas as outras coisas são iguais, use RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635925"
---
# <a name="which-security-provider-to-use"></a><span data-ttu-id="0acd3-103">Qual provedor de segurança usar</span><span class="sxs-lookup"><span data-stu-id="0acd3-103">Which Security Provider to Use</span></span>

<span data-ttu-id="0acd3-104">Todas as outras coisas são iguais, use RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate.</span><span class="sxs-lookup"><span data-stu-id="0acd3-104">All other things being equal, use RPC\_C\_AUTHN\_GSS\_KERBEROS or RPC\_C\_AUTHN\_GSS\_NEGOTIATE.</span></span> <span data-ttu-id="0acd3-105">Cada um fornece o serviço mais escalonável e seguro.</span><span class="sxs-lookup"><span data-stu-id="0acd3-105">Each provides the most scalable and secure service.</span></span> <span data-ttu-id="0acd3-106">Se você usar RPC \_ C \_ Authn \_ GSS \_ Negotiate no servidor, isso permitirá que clientes de nível inferior, como clientes NTLM, se conectem ao seu servidor.</span><span class="sxs-lookup"><span data-stu-id="0acd3-106">If you use RPC\_C\_AUTHN\_GSS\_NEGOTIATE on the server, this allows down-level clients, such as NTLM clients, to connect to your server.</span></span> <span data-ttu-id="0acd3-107">Se isso for indesejável, limite a escolha somente para RPC \_ C \_ Authn \_ GSS \_ Kerberos ou chame [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) para determinar qual provedor de segurança o cliente está usando e negar acesso a clientes usando NTLM.</span><span class="sxs-lookup"><span data-stu-id="0acd3-107">If that is undesirable, either limit the choice to RPC\_C\_AUTHN\_GSS\_KERBEROS only, or call [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to determine which security provider the client is using, and deny access to clients using NTLM.</span></span> <span data-ttu-id="0acd3-108">O método preferencial para estabelecer qual provedor de segurança o cliente está usando é a função [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .</span><span class="sxs-lookup"><span data-stu-id="0acd3-108">The preferred method of establishing which security provider the client is using is the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function.</span></span>

 

 




