---
title: Usando RPC assíncrono com pipes de DCE
description: O Microsoft RPC dá suporte ao uso de pipes de DCE. Embora eles compartilhem um nome semelhante, os pipes de DCE não estão relacionados a pipes nomeados. Pipes nomeados são um protocolo de transporte. Os pipes de DCE são um método independente de protocolo de comunicação de cliente/servidor.
ms.assetid: 9de4f6dc-0aa9-446e-b68c-e0d1e247fea7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e9c98f4d4191a064d78cff2c918077f27d676f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005472"
---
# <a name="using-asynchronous-rpc-with-dce-pipes"></a><span data-ttu-id="84e21-106">Usando RPC assíncrono com pipes de DCE</span><span class="sxs-lookup"><span data-stu-id="84e21-106">Using Asynchronous RPC with DCE Pipes</span></span>

<span data-ttu-id="84e21-107">O Microsoft RPC dá suporte ao uso de pipes de DCE.</span><span class="sxs-lookup"><span data-stu-id="84e21-107">Microsoft RPC supports the use of DCE pipes.</span></span> <span data-ttu-id="84e21-108">Embora eles compartilhem um nome semelhante, os pipes de DCE não estão relacionados a [pipes nomeados](asynchronous-rpc-over-the-named-pipe-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="84e21-108">Although they share a similar name, DCE pipes are unrelated to [named pipes](asynchronous-rpc-over-the-named-pipe-protocol.md).</span></span> <span data-ttu-id="84e21-109">Pipes nomeados são um protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="84e21-109">Named pipes are a transport protocol.</span></span> <span data-ttu-id="84e21-110">Os pipes de DCE são um método independente de protocolo de comunicação de cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="84e21-110">DCE pipes are a protocol-independent method of client/server communication.</span></span>

<span data-ttu-id="84e21-111">Esta seção apresenta uma discussão do RPC usando pipes de DCE assíncronos.</span><span class="sxs-lookup"><span data-stu-id="84e21-111">This section presents a discussion of RPC using asynchronous DCE pipes.</span></span> <span data-ttu-id="84e21-112">Ele é dividido nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="84e21-112">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="84e21-113">Pipes assíncronos</span><span class="sxs-lookup"><span data-stu-id="84e21-113">Asynchronous Pipes</span></span>](asynchronous-pipes.md)
-   [<span data-ttu-id="84e21-114">Declarando pipes assíncronos</span><span class="sxs-lookup"><span data-stu-id="84e21-114">Declaring Asynchronous Pipes</span></span>](declaring-asynchronous-pipes.md)
-   [<span data-ttu-id="84e21-115">Manipulação de pipes assíncronos do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="84e21-115">Client-side Asynchronous Pipe Handling</span></span>](client-side-asynchronous-pipe-handling.md)
-   [<span data-ttu-id="84e21-116">Manipulação de pipes assíncronos do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="84e21-116">Server-side Asynchronous Pipe Handling</span></span>](server-side-asynchronous-pipe-handling.md)

<span data-ttu-id="84e21-117">Para obter um exemplo de aplicativo RPC de pipe assíncrono, consulte o exemplo FileRep no SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="84e21-117">For a sample asynchronous pipe RPC application, see the FileRep sample in the Platform Software Development Kit (SDK).</span></span>

 

 




