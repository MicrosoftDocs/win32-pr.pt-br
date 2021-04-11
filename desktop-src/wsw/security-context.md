---
title: Contexto de segurança
description: Os contextos de segurança habilitam o estabelecimento de um contexto de segurança de mensagem de acordo com o WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Contexto de segurança nativo-Web-Services
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294611"
---
# <a name="security-context"></a><span data-ttu-id="fc173-106">Contexto de segurança</span><span class="sxs-lookup"><span data-stu-id="fc173-106">Security Context</span></span>

<span data-ttu-id="fc173-107">Os contextos de segurança habilitam o estabelecimento de um contexto de segurança de mensagem de acordo com o WS-SecureConversation.</span><span class="sxs-lookup"><span data-stu-id="fc173-107">Security contexts enable the establishment of a message security context according to WS-SecureConversation.</span></span> <span data-ttu-id="fc173-108">Esse contexto pode, então, ser usado para proteger mensagens como uma alternativa para a segurança de uma imagem em que as credenciais são transmitidas para cada solicitação.</span><span class="sxs-lookup"><span data-stu-id="fc173-108">That context can then be used to secure messages as an alternative to one-shot security where the credentials are transmitted for every request.</span></span> <span data-ttu-id="fc173-109">O contexto de segurança estabelecido é um método mais eficiente de proteger mensagens quando várias mensagens são trocadas.</span><span class="sxs-lookup"><span data-stu-id="fc173-109">The established security context is a more efficient method of securing messages when multiple messages are exchanged.</span></span>


<span data-ttu-id="fc173-110">Contextos de segurança exigem a presença de credenciais de segurança de bootstrap que são usadas para proteger as mensagens enviadas no contexto.</span><span class="sxs-lookup"><span data-stu-id="fc173-110">Security contexts require the presence of bootstrap security credentials that are used to secure the messages sent in the context.</span></span> <span data-ttu-id="fc173-111">A associação de [**\_ \_ segurança de \_ mensagem \_ \_ APREQ do WS Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**Associação de \_ segurança de \_ \_ mensagem \_ \_ de token do WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)e estruturas de associação de [**segurança de \_ \_ mensagem \_ \_ WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) podem ser usadas para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="fc173-111">The [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding), and [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) structures may be used for this purpose.</span></span>

<span data-ttu-id="fc173-112">Os contextos de segurança são um recurso de segurança de mensagem e são configurados por meio de associações de segurança de mensagem.</span><span class="sxs-lookup"><span data-stu-id="fc173-112">Security contexts are a message security feature and are configured by way of message security bindings.</span></span>

## <a name="client"></a><span data-ttu-id="fc173-113">Cliente</span><span class="sxs-lookup"><span data-stu-id="fc173-113">Client</span></span>

<span data-ttu-id="fc173-114">No lado do cliente, o contexto de segurança é vinculado a um canal específico.</span><span class="sxs-lookup"><span data-stu-id="fc173-114">On the client side, the security context is tied to a particular channel.</span></span> <span data-ttu-id="fc173-115">Ele é configurado usando a [**\_ Associação de \_ \_ segurança de \_ \_ mensagem de contexto de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span><span class="sxs-lookup"><span data-stu-id="fc173-115">It is configured using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span></span> <span data-ttu-id="fc173-116">O comportamento e o tempo de vida do contexto são determinados pelo canal.</span><span class="sxs-lookup"><span data-stu-id="fc173-116">Behavior and lifetime of the context are determined by the channel.</span></span> <span data-ttu-id="fc173-117">Quando a primeira mensagem é enviada no canal, o contexto de segurança é estabelecido.</span><span class="sxs-lookup"><span data-stu-id="fc173-117">When the first message is sent on the channel, the security context is established.</span></span> <span data-ttu-id="fc173-118">Depois disso, o contexto é renovado proativamente em um intervalo configurável.</span><span class="sxs-lookup"><span data-stu-id="fc173-118">After that, the context is proactively renewed at a configurable interval.</span></span> <span data-ttu-id="fc173-119">Se o servidor retornar uma falha indicando que o contexto requer renovação, o contexto será renovado quando a próxima mensagem for enviada.</span><span class="sxs-lookup"><span data-stu-id="fc173-119">If the server returns a fault indicating that the context requires renewal, the context is renewed when the next message is sent.</span></span> <span data-ttu-id="fc173-120">Se o canal estiver no estado aberto, o contexto será cancelado por uma mensagem de cancelamento quando o canal for fechado.</span><span class="sxs-lookup"><span data-stu-id="fc173-120">If the channel is in the open state, the context is canceled by a cancel message when the channel is closed.</span></span>

## <a name="server"></a><span data-ttu-id="fc173-121">Servidor</span><span class="sxs-lookup"><span data-stu-id="fc173-121">Server</span></span>

<span data-ttu-id="fc173-122">No servidor, um contexto de segurança é configurado da mesma maneira que no cliente.</span><span class="sxs-lookup"><span data-stu-id="fc173-122">On the server, a security context is configured the same way as on the client.</span></span> <span data-ttu-id="fc173-123">No entanto, ele não está vinculado a nenhum canal específico.</span><span class="sxs-lookup"><span data-stu-id="fc173-123">However, it is not tied to any particular channel.</span></span> <span data-ttu-id="fc173-124">Em vez disso, todos os canais criados para o ouvinte que tem o conjunto de [**Associação de segurança de mensagem de \_ contexto de segurança \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) são capazes de receber mensagens com qualquer um dos contextos de segurança que foram estabelecidos em canais desse ouvinte.</span><span class="sxs-lookup"><span data-stu-id="fc173-124">Instead, all channels created for the listener that has the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) set are capable of receiving messages with any of the security contexts that were established on channels of that listener.</span></span>

<span data-ttu-id="fc173-125">Quando uma mensagem chega em um canal que dá suporte a contextos de segurança, o contexto usado por essa mensagem pode ser obtido chamando-se a função [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) com o contexto de segurança de [**propriedade de \_ mensagem \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span><span class="sxs-lookup"><span data-stu-id="fc173-125">When a message arrives on a channel that supports security contexts, the context used by that message can by obtained by calling the [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) function with the [**WS\_MESSAGE\_PROPERTY\_SECURITY\_CONTEXT**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="fc173-126">O valor recuperado pode ser usado com [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) e [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span><span class="sxs-lookup"><span data-stu-id="fc173-126">The retrieved value can be used with [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) and [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span></span>

## <a name="metadata"></a><span data-ttu-id="fc173-127">Metadados</span><span class="sxs-lookup"><span data-stu-id="fc173-127">Metadata</span></span>

<span data-ttu-id="fc173-128">A estrutura de restrição de associação de segurança de mensagem de contexto de segurança do WS é usada para extrair a política de contexto de segurança dos metadados. [**\_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)</span><span class="sxs-lookup"><span data-stu-id="fc173-128">The [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) structure is used to extract the security context policy from metadata.</span></span> <span data-ttu-id="fc173-129">Para obter mais informações, consulte [importação de metadados](metadata-import.md).</span><span class="sxs-lookup"><span data-stu-id="fc173-129">For more information, see [Metadata Import](metadata-import.md).</span></span>

<span data-ttu-id="fc173-130">Os seguintes elementos de API são usados com contextos de segurança.</span><span class="sxs-lookup"><span data-stu-id="fc173-130">The following API elements are used with security contexts.</span></span>

| <span data-ttu-id="fc173-131">Enumeração</span><span class="sxs-lookup"><span data-stu-id="fc173-131">Enumeration</span></span>                                                                    | <span data-ttu-id="fc173-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc173-132">Description</span></span>                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="fc173-133">**\_ID da \_ Propriedade do contexto de segurança WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc173-133">**WS\_SECURITY\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | <span data-ttu-id="fc173-134">Identifica uma propriedade de um objeto de contexto de segurança.</span><span class="sxs-lookup"><span data-stu-id="fc173-134">Identifies a property of a security context object.</span></span> |



 



| <span data-ttu-id="fc173-135">Função</span><span class="sxs-lookup"><span data-stu-id="fc173-135">Function</span></span>                                                             | <span data-ttu-id="fc173-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc173-136">Description</span></span>                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="fc173-137">**WsGetSecurityContextProperty**</span><span class="sxs-lookup"><span data-stu-id="fc173-137">**WsGetSecurityContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | <span data-ttu-id="fc173-138">Obtém uma propriedade do contexto de segurança especificado.</span><span class="sxs-lookup"><span data-stu-id="fc173-138">Gets a property of the specified security context.</span></span> |
| [<span data-ttu-id="fc173-139">**WsRevokeSecurityContext**</span><span class="sxs-lookup"><span data-stu-id="fc173-139">**WsRevokeSecurityContext**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | <span data-ttu-id="fc173-140">Revoga um contexto de segurança.</span><span class="sxs-lookup"><span data-stu-id="fc173-140">Revokes a security context.</span></span>                        |



 



| <span data-ttu-id="fc173-141">Handle</span><span class="sxs-lookup"><span data-stu-id="fc173-141">Handle</span></span>                                           | <span data-ttu-id="fc173-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc173-142">Description</span></span>                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="fc173-143">\_contexto de segurança do WS \_</span><span class="sxs-lookup"><span data-stu-id="fc173-143">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md) | <span data-ttu-id="fc173-144">Um tipo opaco usado para fazer referência a um objeto de contexto de segurança.</span><span class="sxs-lookup"><span data-stu-id="fc173-144">An opaque type used to reference a security context object.</span></span> |



 



| <span data-ttu-id="fc173-145">Estrutura</span><span class="sxs-lookup"><span data-stu-id="fc173-145">Structure</span></span>                                                               | <span data-ttu-id="fc173-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc173-146">Description</span></span>                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="fc173-147">**\_propriedade de \_ contexto de segurança WS \_**</span><span class="sxs-lookup"><span data-stu-id="fc173-147">**WS\_SECURITY\_CONTEXT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | <span data-ttu-id="fc173-148">Define uma propriedade de um [ \_ \_ contexto de segurança do WS](ws-security-context.md).</span><span class="sxs-lookup"><span data-stu-id="fc173-148">Defines a property of a [WS\_SECURITY\_CONTEXT](ws-security-context.md).</span></span> |



 

 

 




