---
description: Esta seção descreve a implementação do protocolo de multicast de Pragmatic General multicast (PGM) no Windows, geralmente conhecida como multicast confiável. O multicast confiável é implementado por meio do Windows Sockets no Windows Server 2003 e posterior.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Programação de multicast confiável (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce57fcce7bf2faf471604bed97d345971801ca1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796225"
---
# <a name="reliable-multicast-programming-pgm"></a><span data-ttu-id="ac728-104">Programação de multicast confiável (PGM)</span><span class="sxs-lookup"><span data-stu-id="ac728-104">Reliable Multicast Programming (PGM)</span></span>

<span data-ttu-id="ac728-105">Esta seção descreve a implementação do protocolo de multicast de Pragmatic General multicast (PGM) no Windows, geralmente conhecida como multicast confiável.</span><span class="sxs-lookup"><span data-stu-id="ac728-105">This section describes the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as reliable multicast.</span></span> <span data-ttu-id="ac728-106">O multicast confiável é implementado por meio do Windows Sockets no Windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ac728-106">Reliable multicast is implemented through Windows Sockets in Windows Server 2003 and later.</span></span>

<span data-ttu-id="ac728-107">**Windows XP:** O PGM só tem suporte quando o MSMQ (enfileiramento de mensagens da Microsoft) 3,0 está instalado.</span><span class="sxs-lookup"><span data-stu-id="ac728-107">**Windows XP:** PGM is only supported when Microsoft Message Queuing (MSMQ) 3.0 is installed.</span></span>

<span data-ttu-id="ac728-108">O PGM é um protocolo multicast confiável e escalonável que permite que os receptores detectem perda, solicitem a retransmissão de dados perdidos ou notifiquem uma aplicação de perda irrecuperável.</span><span class="sxs-lookup"><span data-stu-id="ac728-108">PGM is a reliable and scalable multicast protocol that enables receivers to detect loss, request retransmission of lost data, or notify an application of unrecoverable loss.</span></span> <span data-ttu-id="ac728-109">O PGM é um protocolo confiável para receptor, o que significa que o receptor é responsável por garantir que todos os dados sejam recebidos, absolvingndo o remetente da responsabilidade de recepção.</span><span class="sxs-lookup"><span data-stu-id="ac728-109">PGM is a receiver-reliable protocol, which means the receiver is responsible for ensuring all data is received, absolving the sender of reception responsibility.</span></span>

<span data-ttu-id="ac728-110">O PGM é apropriado para aplicativos que exigem entrega de dados multicast livre de duplicação de várias fontes para vários destinatários.</span><span class="sxs-lookup"><span data-stu-id="ac728-110">PGM is appropriate for applications that require duplicate-free multicast data delivery from multiple sources to multiple receivers.</span></span> <span data-ttu-id="ac728-111">O PGM não dá suporte à entrega confirmada, nem garante a ordenação de pacotes de vários remetentes.</span><span class="sxs-lookup"><span data-stu-id="ac728-111">PGM does not support acknowledged delivery, nor does it guarantee ordering of packets from multiple senders.</span></span>

<span data-ttu-id="ac728-112">Para obter mais informações sobre o PGM, consulte RFC 3208 disponível em [www.ietf.org](https://www.ietf.org/).</span><span class="sxs-lookup"><span data-stu-id="ac728-112">For more information about PGM, refer to RFC 3208 available at [www.ietf.org](https://www.ietf.org/).</span></span>

<span data-ttu-id="ac728-113">Esta seção descreve como usar multicast confiável no Windows.</span><span class="sxs-lookup"><span data-stu-id="ac728-113">This section describes how to use reliable multicast on Windows.</span></span> <span data-ttu-id="ac728-114">Os tópicos a seguir explicam os diversos aspectos da criação de um aplicativo de multicast confiável usando soquetes do Windows:</span><span class="sxs-lookup"><span data-stu-id="ac728-114">The following topics explain the various aspects of creating a reliable multicast application using Windows Sockets:</span></span>

-   [<span data-ttu-id="ac728-115">Remetentes e receptores de PGM</span><span class="sxs-lookup"><span data-stu-id="ac728-115">PGM Senders and Receivers</span></span>](pgm-senders-and-receivers.md)
-   [<span data-ttu-id="ac728-116">Opções do remetente PGM</span><span class="sxs-lookup"><span data-stu-id="ac728-116">PGM Sender Options</span></span>](pgm-sender-options.md)
-   [<span data-ttu-id="ac728-117">Enviando e recebendo dados do PGM</span><span class="sxs-lookup"><span data-stu-id="ac728-117">Sending and Receiving PGM Data</span></span>](sending-and-receiving-pgm-data.md)
-   [<span data-ttu-id="ac728-118">Hospedagem múltipla e PGM</span><span class="sxs-lookup"><span data-stu-id="ac728-118">Multihoming and PGM</span></span>](multihoming-and-pgm.md)
-   [<span data-ttu-id="ac728-119">Opções de soquete PGM</span><span class="sxs-lookup"><span data-stu-id="ac728-119">PGM Socket Options</span></span>](pgm-socket-options.md)

 

 



