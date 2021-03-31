---
title: Manipulação de pipes assíncronos do lado do cliente
description: Antes de fazer uma chamada remota assíncrona, o cliente deve primeiro inicializar o identificador assíncrono.
ms.assetid: 3d54b233-d8b0-45d1-b759-0d2d24c1e247
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ff503f80c77b2403d683c2b644d89836365956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822903"
---
# <a name="client-side-asynchronous-pipe-handling"></a><span data-ttu-id="eb434-103">Manipulação de pipes assíncronos do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="eb434-103">Client-side Asynchronous Pipe Handling</span></span>

<span data-ttu-id="eb434-104">Antes de fazer uma chamada remota assíncrona, o cliente deve primeiro inicializar o identificador assíncrono.</span><span class="sxs-lookup"><span data-stu-id="eb434-104">Before making an asynchronous remote call, the client must first initialize the asynchronous handle.</span></span> <span data-ttu-id="eb434-105">Assim como ocorre com os procedimentos nonpipe, o cliente chama uma função assíncrona com o identificador assíncrono como o primeiro parâmetro e usa o identificador assíncrono para enviar e receber dados de pipe, consultar o status da chamada e receber a resposta.</span><span class="sxs-lookup"><span data-stu-id="eb434-105">As with nonpipe procedures, the client calls an asynchronous function with the asynchronous handle as the first parameter and uses the asynchronous handle to send and receive pipe data, query the status of the call, and receive the reply.</span></span>

<span data-ttu-id="eb434-106">O cliente faz a chamada de procedimento remoto assíncrona com o identificador assíncrono como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb434-106">The client makes the asynchronous remote procedure call with the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="eb434-107">O cliente pode usar esse identificador para consultar o status da chamada e para receber a resposta.</span><span class="sxs-lookup"><span data-stu-id="eb434-107">The client can use this handle to query the status of the call and to receive the reply.</span></span> <span data-ttu-id="eb434-108">O modelo de pipe assíncrono é simétrico.</span><span class="sxs-lookup"><span data-stu-id="eb434-108">The asynchronous pipe model is symmetric.</span></span> <span data-ttu-id="eb434-109">Os aplicativos cliente e servidor enviam e recebem dados de pipe ativamente (em oposição ao RPC síncrono, em que os dados do pipe são enviados e recebidos passivamente).</span><span class="sxs-lookup"><span data-stu-id="eb434-109">Both client and server applications send and receive pipe data actively (as opposed to synchronous RPC, where the pipe data is sent and received passively).</span></span>

<span data-ttu-id="eb434-110">O cliente envia dados de pipe assíncrono chamando a função **Push** no pipe assíncrono apropriado, com a variável de estado do pipe como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb434-110">The client sends asynchronous pipe data by calling the **push** function on the appropriate asynchronous pipe, with the pipe's state variable as the first parameter.</span></span> <span data-ttu-id="eb434-111">Quando a função **Push** retorna, o cliente pode modificar ou liberar o buffer de envio.</span><span class="sxs-lookup"><span data-stu-id="eb434-111">When the **push** function returns, the client can modify or free the send buffer.</span></span>

<span data-ttu-id="eb434-112">Se o \_ sinalizador de \_ notificação assíncrona de RPC \_ no \_ envio \_ for definido no identificador assíncrono e se APCs for usado como o mecanismo de notificação, uma APC será enfileirada quando o pipe Send for realmente concluído.</span><span class="sxs-lookup"><span data-stu-id="eb434-112">If the RPC\_ASYNC\_NOTIFY\_ON\_SEND\_COMPLETE flag is set in the asynchronous handle, and if APCs are used as the notification mechanism, an APC is queued when the pipe send is actually complete.</span></span> <span data-ttu-id="eb434-113">Você pode aproveitar esse mecanismo para implementar o controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="eb434-113">You can take advantage of this mechanism to implement flow control.</span></span> <span data-ttu-id="eb434-114">No entanto, observe que, se o cliente enviar outro buffer antes da conclusão do envio anterior, o cliente poderá, dependendo da velocidade da operação de transferência, receberá apenas uma notificação de envio por push, em vez de uma notificação para cada buffer ou cada operação de **envio** .</span><span class="sxs-lookup"><span data-stu-id="eb434-114">Note, however, that if the client pushes another buffer before the previous push is complete, the client may, depending on the speed of the transfer operation, receive only one send-complete notification, rather than one notification for each buffer or each **push** operation.</span></span> <span data-ttu-id="eb434-115">Quando o cliente enviou todos os dados do pipe, ele faz uma chamada de **envio por push** final com o número de elementos definido como 0.</span><span class="sxs-lookup"><span data-stu-id="eb434-115">When the client has sent all of the pipe data, it makes one final **push** call with the number of elements set to 0.</span></span>

<span data-ttu-id="eb434-116">O programa cliente recebe dados de pipe assíncrono chamando a função **pull** no pipe assíncrono apropriado, com a variável de estado do pipe como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb434-116">The client program receives asynchronous pipe data by calling the **pull** function on the appropriate asynchronous pipe, with the pipe's state variable as the first parameter.</span></span> <span data-ttu-id="eb434-117">Se nenhum dado de pipe estiver disponível, a função **pull** retornará \_ a \_ chamada assíncrona de RPC S \_ \_ pendente.</span><span class="sxs-lookup"><span data-stu-id="eb434-117">If no pipe data is available, the **pull** function returns RPC\_S\_ASYNC\_CALL\_PENDING.</span></span>

<span data-ttu-id="eb434-118">Se o mecanismo de notificação for a APC e o servidor tiver retornado a \_ \_ chamada assíncrona de RPC S \_ \_ pendente, o cliente deverá aguardar até receber a APC **RpcReceiveComplete** do tempo de execução antes de chamar **pull** novamente.</span><span class="sxs-lookup"><span data-stu-id="eb434-118">If the notification mechanism is APC, and the server returned RPC\_S\_ASYNC\_CALL\_PENDING, the client must wait until it receives the **RpcReceiveComplete** APC from run-time before calling **pull** again.</span></span>

 

 




