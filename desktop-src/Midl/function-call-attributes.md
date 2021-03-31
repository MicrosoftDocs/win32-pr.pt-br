---
title: Atributos de chamada de função
description: Os programas podem usar esses atributos em funções individuais dentro da interface e afetar apenas essa função.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- MIDL, atributos, chamada de função IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637096"
---
# <a name="function-call-attributes"></a><span data-ttu-id="a2933-104">Atributos de chamada de função</span><span class="sxs-lookup"><span data-stu-id="a2933-104">Function Call Attributes</span></span>

<span data-ttu-id="a2933-105">Os programas podem usar esses atributos em funções individuais dentro da interface e afetar apenas essa função.</span><span class="sxs-lookup"><span data-stu-id="a2933-105">Programs can use these attributes on individual functions within the interface, and affect only that function.</span></span>



| <span data-ttu-id="a2933-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="a2933-106">Attribute</span></span>                        | <span data-ttu-id="a2933-107">Uso</span><span class="sxs-lookup"><span data-stu-id="a2933-107">Usage</span></span>                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2933-108">**Mensagem**</span><span class="sxs-lookup"><span data-stu-id="a2933-108">**message**</span></span>](message.md)       | <span data-ttu-id="a2933-109">A chamada de procedimento remoto deve ser tratada como uma mensagem assíncrona do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a2933-109">The remote procedure call is to be treated as an asynchronous message from the client to the server.</span></span> <span data-ttu-id="a2933-110">O cliente faz a chamada e retorna imediatamente, enquanto a chamada real é tratada pelo [**ncadg \_ MQ**](ncadg-mq.md)(transporte de enfileiramento de mensagens).</span><span class="sxs-lookup"><span data-stu-id="a2933-110">The client makes the call and returns immediately, while the actual call is handled by the message-queuing transport ([**ncadg\_mq**](ncadg-mq.md)).</span></span> |
| [<span data-ttu-id="a2933-111">**Eu**</span><span class="sxs-lookup"><span data-stu-id="a2933-111">**maybe**</span></span>](maybe.md)           | <span data-ttu-id="a2933-112">O cliente que faz essa chamada de procedimento remoto não espera nenhuma resposta indicando a entrega ou a conclusão da chamada.</span><span class="sxs-lookup"><span data-stu-id="a2933-112">The client making this remote procedure call does not expect any response indicating delivery or completion of the call.</span></span> <span data-ttu-id="a2933-113">Isso está em contraste com as operações de [**mensagem**](message.md) em que nenhuma resposta é esperada, mas a entrega é garantida.</span><span class="sxs-lookup"><span data-stu-id="a2933-113">This is in contrast to [**message**](message.md) operations where no response is expected but the delivery is guaranteed.</span></span>        |
| [<span data-ttu-id="a2933-114">**difusor**</span><span class="sxs-lookup"><span data-stu-id="a2933-114">**broadcast**</span></span>](broadcast.md)   | <span data-ttu-id="a2933-115">A chamada de procedimento remoto deve ser enviada a todos os servidores na rede.</span><span class="sxs-lookup"><span data-stu-id="a2933-115">The remote procedure call is to be sent to all of the servers on the network.</span></span> <span data-ttu-id="a2933-116">O cliente aceita o primeiro retorno, as respostas subsequentes de outros servidores são descartadas.</span><span class="sxs-lookup"><span data-stu-id="a2933-116">The client accepts the first return, subsequent replies from other servers are discarded.</span></span>                                                                                    |
| [<span data-ttu-id="a2933-117">**idempotente**</span><span class="sxs-lookup"><span data-stu-id="a2933-117">**idempotent**</span></span>](idempotent.md) | <span data-ttu-id="a2933-118">A chamada não altera o estado e retorna as mesmas informações cada vez que é chamada com os mesmos parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="a2933-118">The call does not change state and returns the same information each time it is called with the same input parameters.</span></span>                                                                                                                                     |
| [<span data-ttu-id="a2933-119">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="a2933-119">**callback**</span></span>](callback.md)     | <span data-ttu-id="a2933-120">Designa uma função que reside no aplicativo cliente, que o servidor pode chamar para obter informações do cliente.</span><span class="sxs-lookup"><span data-stu-id="a2933-120">Designates a function that resides in the client application, which the server can call to obtain information from the client.</span></span>                                                                                                                             |
| [<span data-ttu-id="a2933-121">**chamar \_ como**</span><span class="sxs-lookup"><span data-stu-id="a2933-121">**call\_as**</span></span>](call-as.md)      | <span data-ttu-id="a2933-122">Mapeia uma função não Remotable para uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="a2933-122">Maps a nonremotable function to a remote procedure call.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="a2933-123">**local**</span><span class="sxs-lookup"><span data-stu-id="a2933-123">**local**</span></span>](local.md)           | <span data-ttu-id="a2933-124">Designa um procedimento local para o qual MIDL não gere código stub.</span><span class="sxs-lookup"><span data-stu-id="a2933-124">Designates a local procedure for which MIDL does not generate stub code.</span></span>                                                                                                                                                                                   |



 

<span data-ttu-id="a2933-125">Em interfaces que não são de [**objeto**](object.md) , você também pode aplicar o atributo de [**\_ identificador de contexto**](context-handle.md) a uma função para especificar características do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a2933-125">On non-[**object**](object.md) interfaces, you can also apply the [**context\_handle**](context-handle.md) attribute to a function to specify characteristics of the return value.</span></span>

 

 




