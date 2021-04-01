---
title: Acesso thread-safe
description: Todas as funções nessa API são seguras para chamar simultaneamente de threads diferentes. No entanto, cada objeto passado como um parâmetro para as funções tem um comportamento de Threading específico, conforme descrito abaixo.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Serviços Web de segurança de thread para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103642987"
---
# <a name="thread-safety"></a><span data-ttu-id="d2b88-107">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="d2b88-107">Thread Safety</span></span>

<span data-ttu-id="d2b88-108">Todas as funções nessa API são seguras para chamar simultaneamente de threads diferentes.</span><span class="sxs-lookup"><span data-stu-id="d2b88-108">All functions in this API are safe to call concurrently from different threads.</span></span> <span data-ttu-id="d2b88-109">No entanto, cada objeto passado como um parâmetro para as funções tem um comportamento de Threading específico, conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="d2b88-109">However, each object passed as a parameter to the functions have specific threading behavior, as described below.</span></span>


<span data-ttu-id="d2b88-110">Os seguintes identificadores são thread único e não oferecem suporte a operações simultâneas para uma determinada instância:</span><span class="sxs-lookup"><span data-stu-id="d2b88-110">The following handles are single threaded and do not support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="d2b88-111">HEAP do WS \_</span><span class="sxs-lookup"><span data-stu-id="d2b88-111">WS\_HEAP</span></span>](ws-heap.md)
-   [<span data-ttu-id="d2b88-112">\_mensagem WS</span><span class="sxs-lookup"><span data-stu-id="d2b88-112">WS\_MESSAGE</span></span>](ws-message.md)
-   [<span data-ttu-id="d2b88-113">\_buffer XML do WS \_</span><span class="sxs-lookup"><span data-stu-id="d2b88-113">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)
-   [<span data-ttu-id="d2b88-114">\_leitor de XML do WS \_</span><span class="sxs-lookup"><span data-stu-id="d2b88-114">WS\_XML\_READER</span></span>](ws-xml-reader.md)
-   [<span data-ttu-id="d2b88-115">gravador do WS \_ XML \_</span><span class="sxs-lookup"><span data-stu-id="d2b88-115">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)
-   [<span data-ttu-id="d2b88-116">\_erro WS</span><span class="sxs-lookup"><span data-stu-id="d2b88-116">WS\_ERROR</span></span>](ws-error.md)
-   [<span data-ttu-id="d2b88-117">\_contexto de operação WS \_</span><span class="sxs-lookup"><span data-stu-id="d2b88-117">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)
-   [<span data-ttu-id="d2b88-118">\_política WS</span><span class="sxs-lookup"><span data-stu-id="d2b88-118">WS\_POLICY</span></span>](ws-policy.md)
-   [<span data-ttu-id="d2b88-119">metadados do WS \_</span><span class="sxs-lookup"><span data-stu-id="d2b88-119">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="d2b88-120">\_token de segurança do WS \_</span><span class="sxs-lookup"><span data-stu-id="d2b88-120">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md)
-   [<span data-ttu-id="d2b88-121">\_contexto de segurança do WS \_</span><span class="sxs-lookup"><span data-stu-id="d2b88-121">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md)

<span data-ttu-id="d2b88-122">Os seguintes identificadores são threads livres e oferecem suporte a operações simultâneas para uma determinada instância:</span><span class="sxs-lookup"><span data-stu-id="d2b88-122">The following handles are free threaded and do support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="d2b88-123">WS \_ Channel</span><span class="sxs-lookup"><span data-stu-id="d2b88-123">WS\_CHANNEL</span></span>](ws-channel.md)
-   [<span data-ttu-id="d2b88-124">\_ouvinte WS</span><span class="sxs-lookup"><span data-stu-id="d2b88-124">WS\_LISTENER</span></span>](ws-listener.md)
-   [<span data-ttu-id="d2b88-125">\_host de serviço WS \_</span><span class="sxs-lookup"><span data-stu-id="d2b88-125">WS\_SERVICE\_HOST</span></span>](ws-service-host.md)
-   [<span data-ttu-id="d2b88-126">\_proxy de serviço WS \_</span><span class="sxs-lookup"><span data-stu-id="d2b88-126">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md)

<span data-ttu-id="d2b88-127">Para todos esses identificadores, o threading é definido em termos de operações (não chamadas de função).</span><span class="sxs-lookup"><span data-stu-id="d2b88-127">For all these handles, threading is defined in terms of operations (not function calls).</span></span> <span data-ttu-id="d2b88-128">Uma operação é definida de maneira diferente para funções invocadas de forma síncrona versus funções invocadas de forma assíncrona:</span><span class="sxs-lookup"><span data-stu-id="d2b88-128">An operation is defined differently for functions invoked synchronously versus functions invoked asynchronously:</span></span>

-   <span data-ttu-id="d2b88-129">Para funções invocadas de forma síncrona, a operação está pendente durante a execução da função.</span><span class="sxs-lookup"><span data-stu-id="d2b88-129">For functions invoked synchronously, the operation is pending during the execution of the function.</span></span>
-   <span data-ttu-id="d2b88-130">Para funções invocadas de forma assíncrona, se a função retornar um código de retorno diferente de **WS \_ S \_ Async** , a operação estará pendente durante a execução da função.</span><span class="sxs-lookup"><span data-stu-id="d2b88-130">For functions invoked asynchronously, if the function returns a return code other than **WS\_S\_ASYNC** the operation is pending during the execution of the function.</span></span> <span data-ttu-id="d2b88-131">No entanto, se a função retornar **WS \_ S \_ Async** , a operação estará pendente até que o [**retorno de \_ \_ chamada WS assíncrono**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) seja invocado.</span><span class="sxs-lookup"><span data-stu-id="d2b88-131">If the function returns **WS\_S\_ASYNC** , however, the operation is pending until the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) is invoked.</span></span> <span data-ttu-id="d2b88-132">Para obter mais informações sobre como invocar funções de forma assíncrona, consulte o tópico [modelo assíncrono](asynchronous-model.md) .</span><span class="sxs-lookup"><span data-stu-id="d2b88-132">For more information about invoking functions asynchronously, see the [Asynchronous Model](asynchronous-model.md) topic.</span></span> <span data-ttu-id="d2b88-133">Para códigos de erro, consulte [valores de retorno dos serviços Web do Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d2b88-133">For error codes, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

<span data-ttu-id="d2b88-134">A falha ao seguir o contrato de threading de um objeto resultará em um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="d2b88-134">Failure to follow the threading contract for an object will result in undefined behavior.</span></span>

 

 




