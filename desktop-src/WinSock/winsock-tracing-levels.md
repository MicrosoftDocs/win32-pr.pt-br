---
description: 'Saiba mais sobre: níveis de rastreamento do Winsock'
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Níveis de rastreamento do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761577"
---
# <a name="winsock-tracing-levels"></a><span data-ttu-id="636a9-103">Níveis de rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="636a9-103">Winsock Tracing Levels</span></span>

## <a name="levels-of-winsock-tracing"></a><span data-ttu-id="636a9-104">Níveis de rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="636a9-104">Levels of Winsock Tracing</span></span>

<span data-ttu-id="636a9-105">Há dois níveis de registro em log possíveis no rastreamento de Winsock:</span><span class="sxs-lookup"><span data-stu-id="636a9-105">There are two levels of logging possible in Winsock tracing:</span></span>

-   <span data-ttu-id="636a9-106">Informações do</span><span class="sxs-lookup"><span data-stu-id="636a9-106">Information</span></span>
-   <span data-ttu-id="636a9-107">Detalhado</span><span class="sxs-lookup"><span data-stu-id="636a9-107">Verbose</span></span>

<span data-ttu-id="636a9-108">O nível de informação rastreia eventos de criação e fechamento de soquete, bem como quaisquer erros que ocorram no soquete.</span><span class="sxs-lookup"><span data-stu-id="636a9-108">The information level traces socket create and close events, as well as any errors that occur on the socket.</span></span>

<span data-ttu-id="636a9-109">O nível detalhado inclui os eventos de nível de informação e adiciona rastreamento adicional para eventos de envio e recebimento.</span><span class="sxs-lookup"><span data-stu-id="636a9-109">The verbose level includes the information level events, and adds additional tracing for send and receive events.</span></span> <span data-ttu-id="636a9-110">O log detalhado seria usado para detectar problemas de corrupção de buffer, bem como aplicativos mal escritos.</span><span class="sxs-lookup"><span data-stu-id="636a9-110">The verbose logging would be used to catch buffer corruption issues as well as poorly written applications.</span></span>

<span data-ttu-id="636a9-111">O nível de informações ou de detalhe pode ser usado com o rastreamento de eventos de rede do Winsock.</span><span class="sxs-lookup"><span data-stu-id="636a9-111">Either the information or verbose level can be used with the Winsock Network Event tracing.</span></span> <span data-ttu-id="636a9-112">O rastreamento de alterações do catálogo Winsock dá suporte apenas ao nível de informações.</span><span class="sxs-lookup"><span data-stu-id="636a9-112">The Winsock Catalog Change tracing supports only information level.</span></span>

## <a name="information-event-tracing"></a><span data-ttu-id="636a9-113">Rastreamento de eventos de informações</span><span class="sxs-lookup"><span data-stu-id="636a9-113">Information Event Tracing</span></span>

<span data-ttu-id="636a9-114">A lista a seguir fornece detalhes sobre as operações do soquete de evento de rede do Winsock que são rastreadas no nível de informação:</span><span class="sxs-lookup"><span data-stu-id="636a9-114">The following list details those Winsock network event socket operations that are traced at the information level:</span></span>

-   <span data-ttu-id="636a9-115">Criação de soquete</span><span class="sxs-lookup"><span data-stu-id="636a9-115">Socket creation</span></span>

    <span data-ttu-id="636a9-116">Um evento é registrado na criação de soquete, que pode ser usada para rastrear o tempo de vida de um soquete.</span><span class="sxs-lookup"><span data-stu-id="636a9-116">An event is logged on socket creation which can be used to trace the lifetime of a socket.</span></span> <span data-ttu-id="636a9-117">Esses eventos também incluem soquetes criados por meio da aceitação de conexões em um soquete de escuta.</span><span class="sxs-lookup"><span data-stu-id="636a9-117">These events also includes sockets created by accepting connections on a listening socket.</span></span>

-   <span data-ttu-id="636a9-118">Associar</span><span class="sxs-lookup"><span data-stu-id="636a9-118">Bind</span></span>

    <span data-ttu-id="636a9-119">O endereço IP local é registrado para ajudar a correlacionar as informações de rastreamento do Winsock às chamadas de soquete de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="636a9-119">The local IP address is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="636a9-120">Conectar</span><span class="sxs-lookup"><span data-stu-id="636a9-120">Connect</span></span>

    <span data-ttu-id="636a9-121">O endereço IP remoto do Soquete conectado é registrado para ajudar a correlacionar as informações de rastreamento do Winsock às chamadas de soquete de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="636a9-121">The remote IP address of the connected socket is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="636a9-122">Anulações e cancelamentos iniciados pelo Winsock</span><span class="sxs-lookup"><span data-stu-id="636a9-122">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="636a9-123">Sempre que o Winsock aborta ou cancela ativamente uma solicitação, o evento é registrado.</span><span class="sxs-lookup"><span data-stu-id="636a9-123">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="636a9-124">Redefinições iniciadas pelo transporte</span><span class="sxs-lookup"><span data-stu-id="636a9-124">Transport initiated resets</span></span>

    <span data-ttu-id="636a9-125">Sempre que o transporte subjacente indicar que uma conexão foi redefinida, o evento será registrado.</span><span class="sxs-lookup"><span data-stu-id="636a9-125">Anytime the underlying transport indicates a connection has been reset, the event is logged.</span></span>

-   <span data-ttu-id="636a9-126">Enviar e receber erros</span><span class="sxs-lookup"><span data-stu-id="636a9-126">Send and receive errors</span></span>

    <span data-ttu-id="636a9-127">Sempre que uma chamada de envio ou recebimento para o transporte subjacente falhar, o evento será registrado.</span><span class="sxs-lookup"><span data-stu-id="636a9-127">Whenever a send or receive call to the underlying transport fails, the event is logged.</span></span>

-   <span data-ttu-id="636a9-128">Desconexão e fechamento de soquete</span><span class="sxs-lookup"><span data-stu-id="636a9-128">Socket disconnect and close</span></span>

    <span data-ttu-id="636a9-129">Um evento é registrado quando um identificador de soquete é fechado.</span><span class="sxs-lookup"><span data-stu-id="636a9-129">An event is logged when a socket handle is closed.</span></span>

## <a name="verbose-event-tracing"></a><span data-ttu-id="636a9-130">Rastreamento de eventos detalhado</span><span class="sxs-lookup"><span data-stu-id="636a9-130">Verbose Event Tracing</span></span>

<span data-ttu-id="636a9-131">Todos os eventos de informação são rastreados no nível detalhado.</span><span class="sxs-lookup"><span data-stu-id="636a9-131">All of the information events are traced at the verbose level.</span></span> <span data-ttu-id="636a9-132">A lista a seguir fornece detalhes sobre as operações adicionais do soquete de evento de rede do Winsock que são rastreadas no nível detalhado:</span><span class="sxs-lookup"><span data-stu-id="636a9-132">The following list details those additional Winsock network event socket operations that are traced at the verbose level:</span></span>

-   <span data-ttu-id="636a9-133">Buffers de envio e recebimento</span><span class="sxs-lookup"><span data-stu-id="636a9-133">Send and receive buffers</span></span>

    <span data-ttu-id="636a9-134">Os eventos são registrados em log de endereços de buffer de usuário e comprimentos quando as chamadas de envio e recebimento são postadas no Winsock, bem como na conclusão dessas chamadas.</span><span class="sxs-lookup"><span data-stu-id="636a9-134">Events are logged of user buffer addresses and lengths when send and receive calls are posted to Winsock, as well as upon completion of these calls.</span></span> <span data-ttu-id="636a9-135">Isso é útil para diagnosticar problemas de reutilização de buffer, bem como o uso ineficiente de buffers.</span><span class="sxs-lookup"><span data-stu-id="636a9-135">This is useful for diagnosing buffer re-use issues as well as inefficient use of buffers.</span></span>

-   <span data-ttu-id="636a9-136">Opções de soquete</span><span class="sxs-lookup"><span data-stu-id="636a9-136">Socket options</span></span>

    <span data-ttu-id="636a9-137">Um evento é registrado quando um aplicativo altera determinados valores de opção de soquete.</span><span class="sxs-lookup"><span data-stu-id="636a9-137">An event is logged when an application changes certain socket option values.</span></span> <span data-ttu-id="636a9-138">Algumas das opções registradas incluem \_ SNDBUF, portanto, \_ RCVBUF, SiO \_ habilitam o \_ \_ enfileiramento circular e FIONBIO.</span><span class="sxs-lookup"><span data-stu-id="636a9-138">Some of the options logged include SO\_SNDBUF, SO\_RCVBUF, SIO\_ENABLE\_CIRCULAR\_QUEUEING, and FIONBIO.</span></span>

-   <span data-ttu-id="636a9-139">WSAPoll e selecione</span><span class="sxs-lookup"><span data-stu-id="636a9-139">WSAPoll and select</span></span>

    <span data-ttu-id="636a9-140">Um evento é registrado no uso de um aplicativo de [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) e [**seleciona**](/windows/desktop/api/Winsock2/nf-winsock2-select) chamadas que podem ser usadas para encontrar afunilamentos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="636a9-140">An event is logged of an application's usage of [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) and [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) calls which can be used to find performance bottlenecks.</span></span>

-   <span data-ttu-id="636a9-141">Anulações e cancelamentos iniciados pelo Winsock</span><span class="sxs-lookup"><span data-stu-id="636a9-141">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="636a9-142">Sempre que o Winsock aborta ou cancela ativamente uma solicitação, o evento é registrado.</span><span class="sxs-lookup"><span data-stu-id="636a9-142">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="636a9-143">Máscara de evento</span><span class="sxs-lookup"><span data-stu-id="636a9-143">Event mask</span></span>

    <span data-ttu-id="636a9-144">Um evento é registrado na máscara de evento que um aplicativo registra para usar a função [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .</span><span class="sxs-lookup"><span data-stu-id="636a9-144">An event is logged of the event mask an application registers for using the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

-   <span data-ttu-id="636a9-145">Datagrama</span><span class="sxs-lookup"><span data-stu-id="636a9-145">Datagram</span></span>

    <span data-ttu-id="636a9-146">Um evento é registrado sempre que um datagrama chega e não há espaço de buffer para copiá-lo.</span><span class="sxs-lookup"><span data-stu-id="636a9-146">An event is logged whenever a datagram arrives and there is no buffer space in which to copy it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="636a9-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="636a9-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="636a9-148">Controle do rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="636a9-148">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="636a9-149">Rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="636a9-149">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="636a9-150">Detalhes de rastreamento de alteração do catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="636a9-150">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="636a9-151">Detalhes de rastreamento de eventos de rede do Winsock</span><span class="sxs-lookup"><span data-stu-id="636a9-151">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
