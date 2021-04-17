---
description: O serviço de componentes em fila do COM+ aprimora o modelo de programação COM, fornecendo um ambiente no qual um componente pode ser invocado de forma síncrona (em tempo real) ou assincronamente (na fila).
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Arquitetura de componentes na fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a2f6e1012bd3c11a27a44214ee28e84d5bd404
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104569987"
---
# <a name="queued-components-architecture"></a><span data-ttu-id="65e6f-103">Arquitetura de componentes na fila</span><span class="sxs-lookup"><span data-stu-id="65e6f-103">Queued Components Architecture</span></span>

<span data-ttu-id="65e6f-104">O serviço de componentes em fila do COM+ aprimora o modelo de programação COM, fornecendo um ambiente no qual um componente pode ser invocado de forma síncrona (em tempo real) ou assincronamente (na fila).</span><span class="sxs-lookup"><span data-stu-id="65e6f-104">The COM+ queued components service enhances the COM programming model by providing an environment in which a component can be invoked either synchronously (real-time) or asynchronously (queued).</span></span> <span data-ttu-id="65e6f-105">Um componente não precisa estar ciente se ele é empregado em um contexto em tempo real ou em fila.</span><span class="sxs-lookup"><span data-stu-id="65e6f-105">A component need not be aware of whether it is employed in a real-time or a queued context.</span></span>

<span data-ttu-id="65e6f-106">Os aplicativos de mensagens são como transações de email entre programas.</span><span class="sxs-lookup"><span data-stu-id="65e6f-106">Messaging applications are like email transactions between programs.</span></span> <span data-ttu-id="65e6f-107">O solicitante envia uma mensagem para o servidor; Quando o servidor chega a ele, a mensagem é processada.</span><span class="sxs-lookup"><span data-stu-id="65e6f-107">The requester sends a message to the server; when the server gets to it, the message is processed.</span></span> <span data-ttu-id="65e6f-108">Como o email, um sistema de mensagens deve lidar com os detalhes da rede e garantir que a mensagem se mova do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="65e6f-108">Like email, a messaging system must handle the network details and ensure that the message moves from the client to the server.</span></span> <span data-ttu-id="65e6f-109">Na estrutura de componentes em fila, o enfileiramento de mensagens é responsável por isso.</span><span class="sxs-lookup"><span data-stu-id="65e6f-109">In the queued components framework, Message Queuing is responsible for this.</span></span>

<span data-ttu-id="65e6f-110">O serviço de componentes em fila COM+ consiste nas seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="65e6f-110">The COM+ queued components service consists of the following parts:</span></span>

-   <span data-ttu-id="65e6f-111">Gravador (para o cliente ou para o lado de envio)</span><span class="sxs-lookup"><span data-stu-id="65e6f-111">Recorder (for the client or send side)</span></span>
-   <span data-ttu-id="65e6f-112">Ouvinte (para o servidor ou lado de recebimento)</span><span class="sxs-lookup"><span data-stu-id="65e6f-112">Listener (for the server or receive side)</span></span>
-   <span data-ttu-id="65e6f-113">Player (para o servidor ou lado de recebimento)</span><span class="sxs-lookup"><span data-stu-id="65e6f-113">Player (for the server or receive side)</span></span>

![Diagrama que mostra o caminho do cliente para o servidor: cliente, gravador, fila, ouvinte, Player, servidor.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a><span data-ttu-id="65e6f-115">O gravador</span><span class="sxs-lookup"><span data-stu-id="65e6f-115">The Recorder</span></span>

<span data-ttu-id="65e6f-116">Em um cenário típico de componentes enfileirados, o cliente chama um componente enfileirado.</span><span class="sxs-lookup"><span data-stu-id="65e6f-116">In a typical queued components scenario, the client calls a queued component.</span></span> <span data-ttu-id="65e6f-117">A chamada é feita ao gravador de componentes em fila, que o empacota como parte de uma mensagem para o servidor e o coloca em uma fila.</span><span class="sxs-lookup"><span data-stu-id="65e6f-117">The call is made to the queued components recorder, which packages it as part of a message to the server and puts it in a queue.</span></span> <span data-ttu-id="65e6f-118">O gravador realiza marshaling do contexto de segurança do cliente na mensagem e registra todas as chamadas de método do cliente.</span><span class="sxs-lookup"><span data-stu-id="65e6f-118">The recorder marshals the client's security context into the message and records all of the client's method calls.</span></span> <span data-ttu-id="65e6f-119">Em sua função como proxy para o componente de servidor, o gravador seleciona interfaces das interfaces queuable no catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="65e6f-119">In its role as proxy for the server component, the recorder selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

<span data-ttu-id="65e6f-120">Uma representação da gravação é enviada ao serviço de enfileiramento de mensagens como uma mensagem a ser enviada a um servidor.</span><span class="sxs-lookup"><span data-stu-id="65e6f-120">A representation of the recording is sent to Message Queuing as a message to be sent to a server.</span></span> <span data-ttu-id="65e6f-121">Quando o componente em fila tiver a configuração de atributo de transação necessária ou com suporte, o enfileiramento de mensagens aceitará a entrega da mensagem somente se a transação do lado do cliente for confirmada e a fila de enfileiramento de mensagens for transacional, que é o padrão normalmente estabelecido.</span><span class="sxs-lookup"><span data-stu-id="65e6f-121">When the queued component has the transaction attribute setting of Required or Supported, Message Queuing accepts delivery of the message only if the client-side transaction commits and the Message Queuing queue is transactional, which is the default normally established.</span></span> <span data-ttu-id="65e6f-122">Quando a configuração do atributo de transação é necessária, o serviço de enfileiramento de mensagens pode aceitar a mensagem mesmo que a transação do lado do cliente seja anulada.</span><span class="sxs-lookup"><span data-stu-id="65e6f-122">When the transaction attribute setting is Requires New, Message Queuing can accept the message even if the client-side transaction aborts.</span></span> <span data-ttu-id="65e6f-123">Para obter mais informações sobre transações, consulte [enfileiramento de mensagens transacionais](transactional-message-queuing.md).</span><span class="sxs-lookup"><span data-stu-id="65e6f-123">For more information on transactions, see [Transactional Message Queuing](transactional-message-queuing.md).</span></span>

## <a name="the-listener"></a><span data-ttu-id="65e6f-124">O ouvinte</span><span class="sxs-lookup"><span data-stu-id="65e6f-124">The Listener</span></span>

<span data-ttu-id="65e6f-125">O ouvinte de componentes na fila recupera a mensagem da fila e a transmite para o player de componentes na fila.</span><span class="sxs-lookup"><span data-stu-id="65e6f-125">The queued components listener retrieves the message from the queue and passes it to the queued components player.</span></span>

## <a name="the-player"></a><span data-ttu-id="65e6f-126">O Player</span><span class="sxs-lookup"><span data-stu-id="65e6f-126">The Player</span></span>

<span data-ttu-id="65e6f-127">O Player desempacota o contexto de segurança do cliente no lado do servidor e, em seguida, invoca o componente do servidor e faz as mesmas chamadas de método.</span><span class="sxs-lookup"><span data-stu-id="65e6f-127">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="65e6f-128">As chamadas de método não são reproduzidas pelo Player até que o componente cliente seja concluído e a transação que registrou o método chame confirmações.</span><span class="sxs-lookup"><span data-stu-id="65e6f-128">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

## <a name="the-message-mover"></a><span data-ttu-id="65e6f-129">O movimentador de mensagens</span><span class="sxs-lookup"><span data-stu-id="65e6f-129">The Message Mover</span></span>

<span data-ttu-id="65e6f-130">O movimentador de mensagens de componentes em fila é um utilitário que move todas as mensagens de enfileiramento de mensagens com falha de uma fila para outra para que elas possam ser repetidas.</span><span class="sxs-lookup"><span data-stu-id="65e6f-130">The queued components message mover is a utility that moves all failed Message Queuing messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="65e6f-131">O utilitário de movimentação de mensagens é um objeto de automação que pode ser invocado com um VBScript; para obter mais informações, consulte [Manipulando erros](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="65e6f-131">The message mover utility is an Automation object that can be invoked with a VBScript; for more information, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

 

 



