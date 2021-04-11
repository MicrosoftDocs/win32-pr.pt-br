---
title: Níveis de autenticação
description: O Microsoft RPC fornece vários níveis de autenticação.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159764"
---
# <a name="authentication-levels"></a><span data-ttu-id="5d66f-103">Níveis de autenticação</span><span class="sxs-lookup"><span data-stu-id="5d66f-103">Authentication Levels</span></span>

<span data-ttu-id="5d66f-104">O Microsoft RPC fornece vários níveis de autenticação.</span><span class="sxs-lookup"><span data-stu-id="5d66f-104">Microsoft RPC provides multiple levels of authentication.</span></span> <span data-ttu-id="5d66f-105">Dependendo do nível de autenticação, a origem do tráfego (que a entidade de segurança enviou o tráfego) pode ser verificada quando a conexão é estabelecida, quando o cliente inicia uma nova chamada de procedimento remoto ou durante cada troca de pacotes entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="5d66f-105">Depending on the authentication level, the origin of the traffic (which security principal sent the traffic) can be verified when the connection is established, when the client starts a new remote procedure call, or during each packet exchange between the client and server.</span></span>

<span data-ttu-id="5d66f-106">Mesmo quando o remetente do tráfego é verificado, a segurança ainda é fraca, uma vez que essa verificação não garante que o pacote não foi modificado ou corrompido na rota; Ele apenas verifica se o pacote veio da entidade de segurança fornecida.</span><span class="sxs-lookup"><span data-stu-id="5d66f-106">Even when the sender of the traffic is verified, security is still weak, since such verification does not ensure the packet was not modified or corrupted en route; it only verifies that the packet came from the given principal.</span></span> <span data-ttu-id="5d66f-107">Para maior segurança, os aplicativos distribuídos podem definir a biblioteca de tempo de execução RPC para verificar se nenhum dos dados trocados entre o cliente e o servidor foi modificado.</span><span class="sxs-lookup"><span data-stu-id="5d66f-107">For greater security, distributed applications can set the RPC run-time library to verify that none of the data exchanged between the client and server is modified.</span></span> <span data-ttu-id="5d66f-108">A Biblioteca RPC também pode criptografar o conteúdo de cada pacote antes de enviá-lo.</span><span class="sxs-lookup"><span data-stu-id="5d66f-108">The RPC library can also encrypt the contents of every packet before sending it.</span></span> <span data-ttu-id="5d66f-109">Em geral, os aplicativos que desejam proteger seu tráfego devem usar apenas os dois últimos níveis: integridade e privacidade.</span><span class="sxs-lookup"><span data-stu-id="5d66f-109">In general, applications that want to secure their traffic should use only the last two levels—integrity and privacy.</span></span>

<span data-ttu-id="5d66f-110">Lembre-se de que os níveis mais altos de autenticação exigem maior sobrecarga computacional.</span><span class="sxs-lookup"><span data-stu-id="5d66f-110">Be aware that higher levels of authentication require higher computational overhead.</span></span> <span data-ttu-id="5d66f-111">Você, como desenvolvedor, deve decidir qual é mais importante para seu aplicativo — velocidade ou segurança.</span><span class="sxs-lookup"><span data-stu-id="5d66f-111">You, as the developer, must decide which is more important for your application—speed or security.</span></span> <span data-ttu-id="5d66f-112">A maioria dos desenvolvedores descobre que, com alguns testes de desempenho, eles podem atingir níveis de desempenho aceitáveis, mantendo a segurança adequada.</span><span class="sxs-lookup"><span data-stu-id="5d66f-112">Most developers find that with some performance testing, they can achieve acceptable performance levels while maintaining adequate security.</span></span>

<span data-ttu-id="5d66f-113">As partes do cliente e do servidor do aplicativo distribuído devem usar o mesmo nível de autenticação.</span><span class="sxs-lookup"><span data-stu-id="5d66f-113">The client and the server portions of the distributed application must use the same authentication level.</span></span> <span data-ttu-id="5d66f-114">Para obter uma lista de níveis de autenticação RPC, consulte [constantes de nível de autenticação](authentication-level-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5d66f-114">For a list of RPC authentication levels, see [Authentication-Level Constants](authentication-level-constants.md).</span></span>

 

 




