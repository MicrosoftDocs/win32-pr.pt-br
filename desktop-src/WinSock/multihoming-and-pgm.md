---
description: Uma consideração especial deve ser dada a remetentes ou destinatários de PGM de hospedagem múltipla. Esta página descreve as considerações e fornece diretrizes para melhores práticas de programação.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Hospedagem múltipla e PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751030"
---
# <a name="multihoming-and-pgm"></a><span data-ttu-id="6eaa4-104">Hospedagem múltipla e PGM</span><span class="sxs-lookup"><span data-stu-id="6eaa4-104">Multihoming and PGM</span></span>

<span data-ttu-id="6eaa4-105">Uma consideração especial deve ser dada a remetentes ou destinatários de PGM de hospedagem múltipla.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-105">Special consideration must be given to multihomed PGM senders or receivers.</span></span> <span data-ttu-id="6eaa4-106">Esta página descreve as considerações e fornece diretrizes para melhores práticas de programação.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-106">This page describes the considerations, and provides guidelines for best programming practices.</span></span>

## <a name="multihomed-pgm-sender"></a><span data-ttu-id="6eaa4-107">Remetente de PGM de hospedagem múltipla</span><span class="sxs-lookup"><span data-stu-id="6eaa4-107">Multihomed PGM Sender</span></span>

<span data-ttu-id="6eaa4-108">Quando um aplicativo falha ao especificar uma interface ao chamar a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , a primeira interface disponível é usada.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-108">When an application fails to specify an interface upon calling the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, the first available interface is used.</span></span> <span data-ttu-id="6eaa4-109">Se nenhuma interface estiver disponível, a **conexão** falhará.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-109">If no interface is available, **connect** fails.</span></span>

<span data-ttu-id="6eaa4-110">Quando um aplicativo especifica uma interface usando a [opção \_ set \_ Send \_ If](socket-options.md) Socket do RM, uma tentativa de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) é feita implicitamente a essa interface usando TCP/IP e falha se o TCP/IP falha na solicitação de associação.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-110">When an application specifies an interface using the [RM\_SET\_SEND\_IF](socket-options.md) socket option, a [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) attempt is made implicitly to that interface using TCP/IP, and fails if TCP/IP fails the bind request.</span></span> <span data-ttu-id="6eaa4-111">Se a interface for definida usando RM \_ set \_ Send \_ If várias vezes, somente o último conjunto de interface será aplicável com êxito.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-111">If the interface is set using RM\_SET\_SEND\_IF multiple times, only the last interface set successfully is applicable.</span></span>

<span data-ttu-id="6eaa4-112">O Windows Sockets mantém a interface definida e, se essa interface desaparecer, a sessão é desconectada.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-112">Windows Sockets maintains which interface is set, and if that interface disappears, the session is disconnected.</span></span>

## <a name="multihomed-pgm-receiver"></a><span data-ttu-id="6eaa4-113">Receptor de PGM de hospedagem múltipla</span><span class="sxs-lookup"><span data-stu-id="6eaa4-113">Multihomed PGM Receiver</span></span>

<span data-ttu-id="6eaa4-114">Quando um aplicativo falha ao especificar uma interface ao chamar a função [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , a interface padrão é usada.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-114">When an application fails to specify an interface upon calling the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, the default interface is used.</span></span> <span data-ttu-id="6eaa4-115">Se nenhuma interface estiver disponível, a [**ligação**](/windows/desktop/api/winsock/nf-winsock-bind) falhará.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-115">If no interface is available, [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) fails.</span></span>

<span data-ttu-id="6eaa4-116">Quando um aplicativo especifica uma ou mais interfaces para escuta, usando o [RM \_ Add \_ Receive \_ If](socket-options.md), o Windows Sockets tenta se associar à interface ou às interfaces solicitadas usando TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-116">When an application specifies one or more interfaces on which to listen, using [RM\_ADD\_RECEIVE\_IF](socket-options.md), Windows Sockets attempts to bind to the requested interface or interfaces using TCP/IP.</span></span> <span data-ttu-id="6eaa4-117">Qualquer erro do TCP/IP faz com que essa solicitação falhe.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-117">Any error from TCP/IP causes this request to fail.</span></span> <span data-ttu-id="6eaa4-118">Ao contrário do caso do emissor do PGM, a adição de uma interface de recebimento várias vezes resulta na postagem de escuta em todas as interfaces adicionadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-118">Unlike the PGM sender case, adding a receive interface multiple times result in the listens being posted on all the successfully added interfaces.</span></span> <span data-ttu-id="6eaa4-119">Use a \_ opção RM del \_ Receive \_ If Socket para parar de escutar em uma interface.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-119">Use the RM\_DEL\_RECEIVE\_IF socket option to stop listening on an interface.</span></span>

<span data-ttu-id="6eaa4-120">O Windows Sockets não mantém o estado sobre várias interfaces de escuta especificadas e, em vez disso, depende do TCP/IP para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-120">Windows Sockets does not maintain state about multiple specified listening interfaces, and instead relies on TCP/IP to do so.</span></span> <span data-ttu-id="6eaa4-121">No entanto, quando uma sessão está em andamento, o Windows Sockets rastreia a interface de entrada para essa sessão e, se essa interface desaparecer, o Windows Sockets desconecta a sessão.</span><span class="sxs-lookup"><span data-stu-id="6eaa4-121">Once a session is in progress, however, Windows Sockets track the incoming interface for that session, and if that interface disappears, Windows Sockets disconnects the session.</span></span>

 

 



