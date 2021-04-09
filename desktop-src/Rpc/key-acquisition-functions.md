---
title: Funções de aquisição de chave
description: Por padrão, o SSP fornece chaves de criptografia para programas de servidor que os solicitam. Cada SSP implementa seu próprio sistema de geração de chaves. O formato das chaves que o SSP gera são específicos para o SSP.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8c8e8cfb2f3b4f8f241b2401878576cbe7f90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822933"
---
# <a name="key-acquisition-functions"></a><span data-ttu-id="095f1-105">Funções de aquisição de chave</span><span class="sxs-lookup"><span data-stu-id="095f1-105">Key Acquisition Functions</span></span>

<span data-ttu-id="095f1-106">Por padrão, o SSP fornece chaves de criptografia para programas de servidor que os solicitam.</span><span class="sxs-lookup"><span data-stu-id="095f1-106">By default, the SSP supplies encryption keys to server programs that request them.</span></span> <span data-ttu-id="095f1-107">Cada SSP implementa seu próprio sistema de geração de chaves.</span><span class="sxs-lookup"><span data-stu-id="095f1-107">Each SSP implements its own system of generating keys.</span></span> <span data-ttu-id="095f1-108">O formato das chaves que o SSP gera são específicos para o SSP.</span><span class="sxs-lookup"><span data-stu-id="095f1-108">The format of the keys that the SSP generates are specific to the SSP.</span></span>

<span data-ttu-id="095f1-109">O RPC fornece a capacidade de substituir o método padrão de geração de chaves de criptografia.</span><span class="sxs-lookup"><span data-stu-id="095f1-109">RPC provides you with the ability to override the default method of generating encryption keys.</span></span> <span data-ttu-id="095f1-110">Seu aplicativo pode chamar a função [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) e passá-la para um ponteiro para uma função de aquisição de chave.</span><span class="sxs-lookup"><span data-stu-id="095f1-110">Your application can call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function and pass it a pointer to a key acquisition function.</span></span> <span data-ttu-id="095f1-111">Você pode escrever a função de aquisição de chave para que ela gere chaves usando qualquer método escolhido.</span><span class="sxs-lookup"><span data-stu-id="095f1-111">You can write the key acquisition function so that it generates keys using any method you choose.</span></span> <span data-ttu-id="095f1-112">No entanto, a chave que ele passa para o programa do servidor deve corresponder ao formato exigido pelo SSP.</span><span class="sxs-lookup"><span data-stu-id="095f1-112">However, the key it passes to the server program must match the format that the SSP requires.</span></span>

> [!Note]  
> <span data-ttu-id="095f1-113">A maioria dos aplicativos não precisa usar as principais funções de aquisição e pode simplesmente fornecer **NULL** a todos os parâmetros em que uma função de aquisição de chave é solicitada.</span><span class="sxs-lookup"><span data-stu-id="095f1-113">Most applications do not need to use key acquisition functions, and can simply supply **NULL** to all parameters where a key acquisition function is requested.</span></span>

 

 

 




