---
title: Ouvinte
description: Um ouvinte é usado pelo cliente para aceitar um canal de entrada de um serviço.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Serviços Web de ouvinte para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e372f3fa9109647e009f0258c059cc4c2065f6bc
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104368947"
---
# <a name="listener"></a><span data-ttu-id="59162-106">Ouvinte</span><span class="sxs-lookup"><span data-stu-id="59162-106">Listener</span></span>

<span data-ttu-id="59162-107">Um ouvinte é usado pelo cliente para aceitar um [canal](channel.md) de entrada de um serviço.</span><span class="sxs-lookup"><span data-stu-id="59162-107">A listener is used by the client to accept an incoming [channel](channel.md) from a service.</span></span>

<span data-ttu-id="59162-108">Para criar um ouvinte, você especifica o tipo de canal como um valor de enumeração de [**\_ \_ tipo de canal do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , as informações de [Associação](binding.md) e a [URL](url.md) a ser escutada.</span><span class="sxs-lookup"><span data-stu-id="59162-108">To create a listner, you specify the channel type as a [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) enumeration value, the [binding](binding.md) information, and the [URL](url.md) to listen on.</span></span>


<span data-ttu-id="59162-109">Para iniciar a escuta na URL, chame a função [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) .</span><span class="sxs-lookup"><span data-stu-id="59162-109">To start listening on the URL, call the [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) function.</span></span>

<span data-ttu-id="59162-110">Para aceitar comunicações de entrada, chame [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span><span class="sxs-lookup"><span data-stu-id="59162-110">To accept incoming communications, call [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span></span>

<span data-ttu-id="59162-111">Para cancelar a e/s pendente para um ouvinte, chame [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span><span class="sxs-lookup"><span data-stu-id="59162-111">To cancel pending IO for a listener, call [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span></span>

<span data-ttu-id="59162-112">Para obter informações sobre as transições de estado para um ouvinte, consulte a enumeração de [**\_ \_ estado do WS Listener**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .</span><span class="sxs-lookup"><span data-stu-id="59162-112">For information on the state transitions for a listener, see the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) enumeration.</span></span>

<span data-ttu-id="59162-113">As seguintes chamadas de retorno fazem parte do ouvinte:</span><span class="sxs-lookup"><span data-stu-id="59162-113">The following callbacks are part of the listener:</span></span>

-   [<span data-ttu-id="59162-114">**\_retorno de \_ chamada de ouvinte WS Abort \_**</span><span class="sxs-lookup"><span data-stu-id="59162-114">**WS\_ABORT\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [<span data-ttu-id="59162-115">**\_retorno de \_ chamada do canal WS Accept \_**</span><span class="sxs-lookup"><span data-stu-id="59162-115">**WS\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [<span data-ttu-id="59162-116">**\_retorno de \_ chamada de ouvinte WS Close \_**</span><span class="sxs-lookup"><span data-stu-id="59162-116">**WS\_CLOSE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [<span data-ttu-id="59162-117">**WS- \_ criar \_ canal \_ para \_ retorno de chamada do ouvinte \_**</span><span class="sxs-lookup"><span data-stu-id="59162-117">**WS\_CREATE\_CHANNEL\_FOR\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [<span data-ttu-id="59162-118">**\_retorno de \_ chamada de ouvinte WS Create \_**</span><span class="sxs-lookup"><span data-stu-id="59162-118">**WS\_CREATE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [<span data-ttu-id="59162-119">**\_retorno de \_ chamada do ouvinte gratuito WS \_**</span><span class="sxs-lookup"><span data-stu-id="59162-119">**WS\_FREE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [<span data-ttu-id="59162-120">**\_retorno de \_ \_ chamada de propriedade WS Get Listener \_**</span><span class="sxs-lookup"><span data-stu-id="59162-120">**WS\_GET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [<span data-ttu-id="59162-121">**retorno de chamada do WS \_ Open \_ Listener \_**</span><span class="sxs-lookup"><span data-stu-id="59162-121">**WS\_OPEN\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [<span data-ttu-id="59162-122">**\_retorno de \_ chamada do ouvinte WS Reset \_**</span><span class="sxs-lookup"><span data-stu-id="59162-122">**WS\_RESET\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [<span data-ttu-id="59162-123">**\_retorno de \_ \_ chamada da propriedade WS Set Listener \_**</span><span class="sxs-lookup"><span data-stu-id="59162-123">**WS\_SET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

<span data-ttu-id="59162-124">As seguintes enumerações fazem parte do ouvinte:</span><span class="sxs-lookup"><span data-stu-id="59162-124">The following enumerations are part of the listener:</span></span>

-   [<span data-ttu-id="59162-125">**versão do WS \_ IP \_**</span><span class="sxs-lookup"><span data-stu-id="59162-125">**WS\_IP\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [<span data-ttu-id="59162-126">**\_ID da \_ Propriedade WS Listener \_**</span><span class="sxs-lookup"><span data-stu-id="59162-126">**WS\_LISTENER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [<span data-ttu-id="59162-127">**Estado do WS \_ Listener \_**</span><span class="sxs-lookup"><span data-stu-id="59162-127">**WS\_LISTENER\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

<span data-ttu-id="59162-128">As funções a seguir fazem parte do ouvinte:</span><span class="sxs-lookup"><span data-stu-id="59162-128">The following functions are part of the listener:</span></span>

-   [<span data-ttu-id="59162-129">**WsAbortListener**</span><span class="sxs-lookup"><span data-stu-id="59162-129">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [<span data-ttu-id="59162-130">**WsAcceptChannel**</span><span class="sxs-lookup"><span data-stu-id="59162-130">**WsAcceptChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [<span data-ttu-id="59162-131">**WsCloseListener**</span><span class="sxs-lookup"><span data-stu-id="59162-131">**WsCloseListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [<span data-ttu-id="59162-132">**WsCreateListener**</span><span class="sxs-lookup"><span data-stu-id="59162-132">**WsCreateListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [<span data-ttu-id="59162-133">**WsFreeListener**</span><span class="sxs-lookup"><span data-stu-id="59162-133">**WsFreeListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [<span data-ttu-id="59162-134">**WsGetListenerProperty**</span><span class="sxs-lookup"><span data-stu-id="59162-134">**WsGetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [<span data-ttu-id="59162-135">**WsOpenListener**</span><span class="sxs-lookup"><span data-stu-id="59162-135">**WsOpenListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [<span data-ttu-id="59162-136">**WsResetListener**</span><span class="sxs-lookup"><span data-stu-id="59162-136">**WsResetListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [<span data-ttu-id="59162-137">**WsSetListenerProperty**</span><span class="sxs-lookup"><span data-stu-id="59162-137">**WsSetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

<span data-ttu-id="59162-138">O identificador a seguir faz parte do ouvinte:</span><span class="sxs-lookup"><span data-stu-id="59162-138">The following handle is part of the listener:</span></span>

-   [<span data-ttu-id="59162-139">\_ouvinte WS</span><span class="sxs-lookup"><span data-stu-id="59162-139">WS\_LISTENER</span></span>](ws-listener.md)

<span data-ttu-id="59162-140">As seguintes estruturas fazem parte do ouvinte:</span><span class="sxs-lookup"><span data-stu-id="59162-140">The following structures are part of the listener:</span></span>

-   [<span data-ttu-id="59162-141">**\_ \_ retornos de chamada de ouvinte personalizado WS \_**</span><span class="sxs-lookup"><span data-stu-id="59162-141">**WS\_CUSTOM\_LISTENER\_CALLBACKS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [<span data-ttu-id="59162-142">**\_SUBcadeias de \_ agente do usuário não permitidas do WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="59162-142">**WS\_DISALLOWED\_USER\_AGENT\_SUBSTRINGS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [<span data-ttu-id="59162-143">**\_nomes de host do WS \_**</span><span class="sxs-lookup"><span data-stu-id="59162-143">**WS\_HOST\_NAMES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [<span data-ttu-id="59162-144">**\_Propriedades do ouvinte WS \_**</span><span class="sxs-lookup"><span data-stu-id="59162-144">**WS\_LISTENER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [<span data-ttu-id="59162-145">**\_Propriedade WS Listener \_**</span><span class="sxs-lookup"><span data-stu-id="59162-145">**WS\_LISTENER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




