---
title: Segurança de transporte
description: Embora esse não seja o método preferencial, você pode usar as configurações de segurança que o transporte de pipe nomeado oferece para adicionar recursos de segurança ao seu aplicativo distribuído.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d129b5a373ed7304c142c66dd0e8b2d4e9035416
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292558"
---
# <a name="transport-security"></a><span data-ttu-id="46f57-103">Segurança de transporte</span><span class="sxs-lookup"><span data-stu-id="46f57-103">Transport Security</span></span>

<span data-ttu-id="46f57-104">Embora esse não seja o método preferencial, você pode usar as configurações de segurança que o transporte de pipe nomeado oferece para adicionar recursos de segurança ao seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="46f57-104">Although this is not the preferred method, you can use the security settings that the named-pipe transport offers to add security features to your distributed application.</span></span> <span data-ttu-id="46f57-105">Essas configurações de segurança são usadas com as funções RPC da Microsoft que começam com os prefixos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) e [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), e as funções [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span><span class="sxs-lookup"><span data-stu-id="46f57-105">These security settings are used with the Microsoft RPC functions that start with the prefixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) and [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), and the functions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span></span>

> [!Note]  
> <span data-ttu-id="46f57-106">Se você estiver executando um aplicativo que é um serviço e estiver usando NTLM para segurança, deverá adicionar uma dependência de serviço explícita para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46f57-106">If you are running an application that is a service and you are using NTLM for security, you must add an explicit service dependency for your application.</span></span> <span data-ttu-id="46f57-107">O Secur32.dll chamará o Gerenciador de controle de serviço (SCM) para iniciar o serviço de pacote de segurança NTLM.</span><span class="sxs-lookup"><span data-stu-id="46f57-107">The Secur32.dll will call the Service Control Manager (SCM) to begin the NTLM security package service.</span></span> <span data-ttu-id="46f57-108">No entanto, um aplicativo RPC que é um serviço e está sendo executado como um sistema, também deve entrar em contato com o SC, a menos que ele esteja se conectando a outro serviço no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="46f57-108">However, an RPC application that is a service and is running as a system, must also contact the SC unless it is connecting to another service on the same computer.</span></span>

 

 

 




