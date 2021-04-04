---
title: Enfileiramento de mensagens RPC
description: O MSMQ (enfileiramento de mensagens) permite que os usuários se comuniquem entre redes e sistemas, independentemente do estado atual dos aplicativos e sistemas de comunicação.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- RPC de chamada de procedimento remoto, descrito, Enfileiramento de mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b72e9e35ec2aa1cc440c0d0356c681c4fe8548c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005932"
---
# <a name="rpc-message-queuing"></a><span data-ttu-id="e89dc-104">Enfileiramento de mensagens RPC</span><span class="sxs-lookup"><span data-stu-id="e89dc-104">RPC Message Queuing</span></span>

<span data-ttu-id="e89dc-105">O MSMQ (enfileiramento de mensagens) permite que os usuários se comuniquem entre redes e sistemas, independentemente do estado atual dos aplicativos e sistemas de comunicação.</span><span class="sxs-lookup"><span data-stu-id="e89dc-105">Message Queuing (MSMQ) lets users communicate across networks and systems regardless of the current state of the communicating applications and systems.</span></span> <span data-ttu-id="e89dc-106">Os aplicativos enviam e recebem mensagens por meio de filas de mensagens que o MSMQ mantém.</span><span class="sxs-lookup"><span data-stu-id="e89dc-106">Applications send and receive messages through message queues that MSMQ maintains.</span></span> <span data-ttu-id="e89dc-107">As filas de mensagens continuam a funcionar mesmo quando o aplicativo cliente ou servidor não está em execução.</span><span class="sxs-lookup"><span data-stu-id="e89dc-107">The message queues continue to function even when the client or server application is not running.</span></span> <span data-ttu-id="e89dc-108">O enfileiramento de mensagens fornece:</span><span class="sxs-lookup"><span data-stu-id="e89dc-108">Message queuing provides:</span></span>

-   <span data-ttu-id="e89dc-109">**Mensagens assíncronas.**</span><span class="sxs-lookup"><span data-stu-id="e89dc-109">**Asynchronous messaging.**</span></span> <span data-ttu-id="e89dc-110">Com o sistema de mensagens assíncrono MSMQ, um aplicativo cliente pode enviar uma mensagem para um servidor e retornar imediatamente, mesmo que o computador de destino ou o programa do servidor não esteja respondendo.</span><span class="sxs-lookup"><span data-stu-id="e89dc-110">With MSMQ asynchronous messaging, a client application can send a message to a server and return immediately, even if the target computer or server program is not responding.</span></span>
-   <span data-ttu-id="e89dc-111">**Entrega de mensagem garantida.**</span><span class="sxs-lookup"><span data-stu-id="e89dc-111">**Guaranteed message delivery.**</span></span> <span data-ttu-id="e89dc-112">Quando um aplicativo envia uma mensagem por meio do MSMQ, a mensagem atingirá seu destino, mesmo se o aplicativo de destino não estiver em execução ao mesmo tempo ou se as redes e os sistemas estiverem offline.</span><span class="sxs-lookup"><span data-stu-id="e89dc-112">When an application sends a message through MSMQ, the message will reach its destination even if the destination application is not running at the same time or the networks and systems are offline.</span></span>
-   <span data-ttu-id="e89dc-113">**Roteamento e configuração dinâmica.**</span><span class="sxs-lookup"><span data-stu-id="e89dc-113">**Routing and dynamic configuration.**</span></span> <span data-ttu-id="e89dc-114">O MSMQ fornece roteamento flexível em redes heterogêneas.</span><span class="sxs-lookup"><span data-stu-id="e89dc-114">MSMQ provides flexible routing over heterogeneous networks.</span></span> <span data-ttu-id="e89dc-115">A configuração dessas redes pode ser alterada dinamicamente sem alterações importantes em sistemas e redes.</span><span class="sxs-lookup"><span data-stu-id="e89dc-115">The configuration of such networks can be changed dynamically without any major changes to systems and networks themselves.</span></span>
-   <span data-ttu-id="e89dc-116">**Mensagens sem conexão.**</span><span class="sxs-lookup"><span data-stu-id="e89dc-116">**Connectionless messaging.**</span></span> <span data-ttu-id="e89dc-117">Os aplicativos que usam o MSMQ não precisam configurar sessões diretas com aplicativos de destino.</span><span class="sxs-lookup"><span data-stu-id="e89dc-117">Applications using MSMQ do not need to set up direct sessions with target applications.</span></span>
-   <span data-ttu-id="e89dc-118">[Segurança](security.md).</span><span class="sxs-lookup"><span data-stu-id="e89dc-118">[Security](security.md).</span></span> <span data-ttu-id="e89dc-119">O MSMQ fornece comunicação segura com base na segurança do Windows e na CryptoAPI (API de criptografia) para criptografia e assinaturas digitais.</span><span class="sxs-lookup"><span data-stu-id="e89dc-119">MSMQ provides secure communication based on Windows security and the Cryptographic API (CryptoAPI) for encryption and digital signatures.</span></span>
-   <span data-ttu-id="e89dc-120">**Mensagens priorizadas.**</span><span class="sxs-lookup"><span data-stu-id="e89dc-120">**Prioritized Messaging.**</span></span> <span data-ttu-id="e89dc-121">O MSMQ transfere mensagens entre redes com base na prioridade, permitindo uma comunicação mais rápida para aplicativos críticos.</span><span class="sxs-lookup"><span data-stu-id="e89dc-121">MSMQ transfers messages across networks based on priority, allowing faster communication for critical applications.</span></span>

<span data-ttu-id="e89dc-122">O Microsoft RPC estende o modelo Open Software Foundation – equipamento de comunicações de dados (uso-DCE) para chamadas de procedimento remoto, permitindo que aplicativos distribuídos usem o MSMQ como um transporte e controlem muitos de seus recursos.</span><span class="sxs-lookup"><span data-stu-id="e89dc-122">Microsoft RPC extends the Open Software Foundation–Data Communications Equipment (OSF-DCE) model for remote procedure calls by allowing distributed applications to use MSMQ as a transport and to control many of its features.</span></span> <span data-ttu-id="e89dc-123">Essa funcionalidade está disponível para aplicativos RPC convencionais e, por meio da interface **IRPCOptions** , para aplicativos com.</span><span class="sxs-lookup"><span data-stu-id="e89dc-123">This functionality is available both to conventional RPC applications and, through the **IRPCOptions** interface, to COM applications.</span></span>

> [!Note]  
> <span data-ttu-id="e89dc-124">O enfileiramento de mensagens RPC está disponível somente no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e89dc-124">RPC message queuing is available only on Windows 2000.</span></span> <span data-ttu-id="e89dc-125">As versões posteriores do Windows não dão suporte ao enfileiramento de mensagens RPC.</span><span class="sxs-lookup"><span data-stu-id="e89dc-125">Later versions of Windows do not support RPC message queuing.</span></span>

 

<span data-ttu-id="e89dc-126">Os tópicos a seguir fornecem uma visão geral do enfileiramento de mensagens:</span><span class="sxs-lookup"><span data-stu-id="e89dc-126">The following topics provide an overview of message queuing:</span></span>

-   [<span data-ttu-id="e89dc-127">Visão geral da arquitetura dos serviços de enfileiramento de mensagens</span><span class="sxs-lookup"><span data-stu-id="e89dc-127">Overview of Message Queuing Services Architecture</span></span>](overview-of-message-queuing-services-architecture.md)
-   [<span data-ttu-id="e89dc-128">Propriedades da mensagem e da fila de mensagens</span><span class="sxs-lookup"><span data-stu-id="e89dc-128">Message and Message Queue Properties</span></span>](message-and-message-queue-properties.md)
-   [<span data-ttu-id="e89dc-129">Usando o MSMQ como um transporte RPC</span><span class="sxs-lookup"><span data-stu-id="e89dc-129">Using MSMQ as an RPC Transport</span></span>](using-msmq-as-an-rpc-transport.md)
-   [<span data-ttu-id="e89dc-130">Requisitos de sistema para RPC – \_ aplicativos de enfileiramento de mensagens</span><span class="sxs-lookup"><span data-stu-id="e89dc-130">System Requirements for RPC-Message\_Queuing Applications</span></span>](system-requirements-for-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="e89dc-131">Desenvolvendo aplicativos de enfileiramento RPC-Message</span><span class="sxs-lookup"><span data-stu-id="e89dc-131">Developing RPC-Message Queuing Applications</span></span>](developing-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="e89dc-132">Serviços de segurança MSMQ</span><span class="sxs-lookup"><span data-stu-id="e89dc-132">MSMQ Security Services</span></span>](msmq-security-services.md)

 

 




