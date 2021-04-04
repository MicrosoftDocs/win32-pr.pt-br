---
title: RPC assíncrono sobre o protocolo de Named-Pipe
description: Se você usar pipes nomeados (ncacn \_ NP) como seu protocolo de transporte, evite permitir um grande número de chamadas pendentes ociosas no servidor.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf46f9e1c2ea5eb3fe20203db274233f5c10dec5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917602"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a><span data-ttu-id="36256-103">RPC assíncrono sobre o protocolo de Named-Pipe</span><span class="sxs-lookup"><span data-stu-id="36256-103">Asynchronous RPC over the Named-Pipe Protocol</span></span>

<span data-ttu-id="36256-104">Se você usar pipes nomeados ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)) como seu protocolo de transporte, evite permitir um grande número de chamadas pendentes ociosas no servidor.</span><span class="sxs-lookup"><span data-stu-id="36256-104">If you use named pipes ([**ncacn\_np**](/windows/desktop/Midl/ncacn-np)) as your transport protocol, you should avoid allowing a large number of idle pending calls on the server.</span></span> <span data-ttu-id="36256-105">Com pipes nomeados, cada cliente aguardando uma resposta terá um pipe nomeado pendente lido no servidor, cada um deles requer uma determinada quantidade de memória do kernel.</span><span class="sxs-lookup"><span data-stu-id="36256-105">With named pipes, each client waiting for a reply will have a pending named pipe read on the server, each of which requires a certain amount of kernel memory.</span></span>

<span data-ttu-id="36256-106">Por exemplo, você não desejaria usar uma chamada de notificação para novos emails com o transporte de pipe nomeado, porque essa chamada permaneceria pendente mesmo quando os clientes estiverem ociosos e a memória do kernel puder ser esgotada.</span><span class="sxs-lookup"><span data-stu-id="36256-106">For example, you would not want to use a notification call for new e-mail with the named-pipe transport, because such a call would remain pending even when clients are idle, and kernel memory could be depleted.</span></span> <span data-ttu-id="36256-107">Observe que isso não é um problema com os outros protocolos orientados à conexão, como [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp).</span><span class="sxs-lookup"><span data-stu-id="36256-107">Note that this is not a problem with the other connection-oriented protocols, such as [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp).</span></span>

<span data-ttu-id="36256-108">Como os pipes nomeados são um protocolo de transporte, seu aplicativo pode usá-los especificando [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) como o protocolo em uma associação de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="36256-108">Since named pipes are a transport protocol, your application can use them by specifying [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) as the protocol in a string binding.</span></span> <span data-ttu-id="36256-109">Para obter mais informações sobre pipes nomeados, consulte [pipes nomeados](/windows/desktop/ipc/named-pipes).</span><span class="sxs-lookup"><span data-stu-id="36256-109">For more information on named pipes, see [Named Pipes](/windows/desktop/ipc/named-pipes).</span></span> <span data-ttu-id="36256-110">Para obter detalhes sobre como criar associações de cadeia de caracteres, consulte [usando associações de cadeia de caracteres](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="36256-110">For details on creating string bindings, see [Using String Bindings](finding-server-host-systems.md).</span></span>

 

 