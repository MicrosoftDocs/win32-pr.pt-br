---
description: Microsoft Digest executa uma autenticação inicial quando o servidor recebe a primeira resposta de desafio de um cliente.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Autenticação do Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747648"
---
# <a name="microsoft-digest-authentication"></a><span data-ttu-id="b5668-103">Autenticação do Microsoft Digest</span><span class="sxs-lookup"><span data-stu-id="b5668-103">Microsoft Digest Authentication</span></span>

<span data-ttu-id="b5668-104">Microsoft Digest executa uma autenticação inicial quando o servidor recebe a primeira resposta de desafio de um cliente.</span><span class="sxs-lookup"><span data-stu-id="b5668-104">Microsoft Digest performs an initial authentication when the server receives the first challenge response from a client.</span></span> <span data-ttu-id="b5668-105">O servidor verifica se o cliente não foi autenticado e, em seguida, executa a autenticação inicial acessando os serviços de um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="b5668-105">The server verifies that the client has not been authenticated and then performs the initial authentication by accessing the services of a domain controller.</span></span> <span data-ttu-id="b5668-106">Para obter uma descrição detalhada desse procedimento, consulte [autenticação inicial usando Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="b5668-106">For a detailed description of this procedure, see [Initial Authentication Using Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span></span>

<span data-ttu-id="b5668-107">Quando a autenticação inicial for bem-sucedida, o servidor receberá uma [*chave de sessão*](../secgloss/s-gly.md)de resumo.</span><span class="sxs-lookup"><span data-stu-id="b5668-107">When the initial authentication is successful the server receives a Digest [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="b5668-108">O servidor armazena em cache essa chave e a usa para autenticar solicitações subsequentes de recursos do cliente.</span><span class="sxs-lookup"><span data-stu-id="b5668-108">The server caches this key and uses it to authenticate subsequent requests for resources from the client.</span></span> <span data-ttu-id="b5668-109">Essa autenticação é local, ou seja, não requer acesso a um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="b5668-109">This authentication is local, that is, it does not require access to a domain controller.</span></span> <span data-ttu-id="b5668-110">Para obter uma descrição detalhada desse procedimento, consulte [Autenticando solicitações subsequentes usando Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="b5668-110">For a detailed description of this procedure see [Authenticating Subsequent Requests Using Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span></span>

<span data-ttu-id="b5668-111">Ao usar HTTP, não há nenhuma conexão mantida entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="b5668-111">When using HTTP, there is no connection maintained between client and server.</span></span> <span data-ttu-id="b5668-112">Para reduzir o tráfego do controlador de domínio e melhorar o desempenho, o Microsoft Digest armazena em cache as informações recebidas após a autenticação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b5668-112">To reduce domain controller traffic and improve performance, Microsoft Digest caches information received after successful authentication.</span></span> <span data-ttu-id="b5668-113">Para obter informações sobre esse processo, consulte [mantendo o contexto de segurança entre conexões](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="b5668-113">For information about this process, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span>

 

 
