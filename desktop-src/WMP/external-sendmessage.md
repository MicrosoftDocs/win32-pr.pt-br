---
title: Método external. sendMessage
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método sendMessage envia uma mensagem para o plug-in da loja online.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- método sendMessage Windows Media Player
- método sendMessage Windows Media Player, classe externa
- Classe externa Windows Media Player, método sendMessage
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779415"
---
# <a name="externalsendmessage-method"></a><span data-ttu-id="928fa-108">Método external. sendMessage</span><span class="sxs-lookup"><span data-stu-id="928fa-108">External.sendMessage method</span></span>

> [!Note]  
> <span data-ttu-id="928fa-109">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="928fa-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="928fa-110">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="928fa-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="928fa-111">O método **SendMessage** envia uma mensagem para o plug-in da loja online.</span><span class="sxs-lookup"><span data-stu-id="928fa-111">The **sendMessage** method sends a message to the online store's plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="928fa-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="928fa-112">Syntax</span></span>


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="928fa-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="928fa-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="928fa-114">*Mensagem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="928fa-114">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="928fa-115">**Cadeia de caracteres** que contém a mensagem.</span><span class="sxs-lookup"><span data-stu-id="928fa-115">**String** containing the message.</span></span>

</dd> <dt>

<span data-ttu-id="928fa-116">*Parâmetro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="928fa-116">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="928fa-117">**Cadeia de caracteres** que contém parâmetros associados à mensagem.</span><span class="sxs-lookup"><span data-stu-id="928fa-117">**String** containing parameters associated with the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="928fa-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="928fa-118">Return value</span></span>

<span data-ttu-id="928fa-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="928fa-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="928fa-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="928fa-120">Remarks</span></span>

<span data-ttu-id="928fa-121">A mensagem é enviada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="928fa-121">The message is sent asynchronously.</span></span> <span data-ttu-id="928fa-122">Ou seja, esse método retorna imediatamente em vez de aguardar a mensagem ser processada.</span><span class="sxs-lookup"><span data-stu-id="928fa-122">That is, this method returns immediately rather than waiting for the message to be processed.</span></span> <span data-ttu-id="928fa-123">Quando o plug-in termina de processar a mensagem, ele chama o método [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) , que, por sua vez, chama o manipulador de eventos [OnSendMessageComplete](external-onsendmessagecomplete-event.md) do script.</span><span class="sxs-lookup"><span data-stu-id="928fa-123">When the plug-in finishes processing the message, it calls the [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) method, which in turn calls the script's [OnSendMessageComplete](external-onsendmessagecomplete-event.md) event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="928fa-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="928fa-124">Requirements</span></span>



| <span data-ttu-id="928fa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="928fa-125">Requirement</span></span> | <span data-ttu-id="928fa-126">Valor</span><span class="sxs-lookup"><span data-stu-id="928fa-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="928fa-127">Versão</span><span class="sxs-lookup"><span data-stu-id="928fa-127">Version</span></span><br/> | <span data-ttu-id="928fa-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="928fa-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="928fa-129">DLL</span><span class="sxs-lookup"><span data-stu-id="928fa-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="928fa-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="928fa-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="928fa-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="928fa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="928fa-132">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="928fa-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="928fa-133">**External. OnSendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="928fa-133">**External.OnSendMessageComplete**</span></span>](external-onsendmessagecomplete-event.md)
</dt> <dt>

[<span data-ttu-id="928fa-134">**IWMPContentPartner:: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="928fa-134">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="928fa-135">**IWMPContentPartnerCallback::SendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="928fa-135">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





