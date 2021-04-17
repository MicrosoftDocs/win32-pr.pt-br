---
title: Evento external. OnSendMessageComplete
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnSendMessageComplete
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Evento external. OnSendMessageComplete do Windows Media Player
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761444"
---
# <a name="externalonsendmessagecomplete-event"></a><span data-ttu-id="5f00b-105">Evento external. OnSendMessageComplete</span><span class="sxs-lookup"><span data-stu-id="5f00b-105">External.OnSendMessageComplete Event</span></span>

> [!Note]  
> <span data-ttu-id="5f00b-106">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="5f00b-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5f00b-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="5f00b-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5f00b-108">O evento **OnSendMessageComplete** ocorre quando o armazenamento online termina de processar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="5f00b-108">The **OnSendMessageComplete** event occurs when the online store has finished processing a message.</span></span> <span data-ttu-id="5f00b-109">O script na página de descoberta enviou a mensagem anteriormente chamando [external. SendMessage](external-sendmessage.md).</span><span class="sxs-lookup"><span data-stu-id="5f00b-109">Script on the discovery page previously sent the message by calling [External.sendMessage](external-sendmessage.md).</span></span>

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="5f00b-110">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5f00b-110">Possible Values</span></span>

<span data-ttu-id="5f00b-111">Essa é uma propriedade somente gravação que especifica o nome da função no script que o Windows Media Player chama quando o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="5f00b-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f00b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f00b-112">Parameters</span></span>

<span data-ttu-id="5f00b-113">A função que manipula esse evento tem os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f00b-113">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="5f00b-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*MSG*</span><span class="sxs-lookup"><span data-stu-id="5f00b-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Msg*</span></span>
</dt> <dd>

<span data-ttu-id="5f00b-115">A mesma cadeia de caracteres que foi passada no parâmetro **msg** de **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="5f00b-115">The same string that was passed in the **Msg** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="5f00b-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*</span><span class="sxs-lookup"><span data-stu-id="5f00b-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*</span></span>
</dt> <dd>

<span data-ttu-id="5f00b-117">A mesma cadeia de caracteres que foi passada no parâmetro **param** de **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="5f00b-117">The same string that was passed in the **Param** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="5f00b-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Disso*</span><span class="sxs-lookup"><span data-stu-id="5f00b-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Result*</span></span>
</dt> <dd>

<span data-ttu-id="5f00b-119">**Cadeia de caracteres** que contém o resultado da manipulação de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5f00b-119">**String** that contains the result of the message handling.</span></span> <span data-ttu-id="5f00b-120">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="5f00b-120">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f00b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f00b-121">Remarks</span></span>

<span data-ttu-id="5f00b-122">O método **SendMessage** chama [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), que retorna de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5f00b-122">The **sendMessage** method calls [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), which returns asynchronously.</span></span> <span data-ttu-id="5f00b-123">Ou seja, ele retorna antes que a loja online termine de processar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="5f00b-123">That is, it returns before the online store finishes processing the message.</span></span> <span data-ttu-id="5f00b-124">Quando o armazenamento online termina de processar a mensagem, ele chama [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), que, por sua vez, chama o manipulador de eventos **OnSendMessageComplete** do script.</span><span class="sxs-lookup"><span data-stu-id="5f00b-124">When the online store finishes processing the message, it calls [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), which in turn calls the script's **OnSendMessageComplete** event handler.</span></span>

<span data-ttu-id="5f00b-125">Quando o armazenamento online chama **IWMPContentPartnerCallback:: SendMessageComplete**, ele fornece um código de resultado no parâmetro *bstrResult* .</span><span class="sxs-lookup"><span data-stu-id="5f00b-125">When the online store calls **IWMPContentPartnerCallback::SendMessageComplete**, it supplies a result code in the *bstrResult* parameter.</span></span> <span data-ttu-id="5f00b-126">O Windows Media Player não interpreta esse código de resultado.</span><span class="sxs-lookup"><span data-stu-id="5f00b-126">Windows Media Player does not interpret that result code.</span></span> <span data-ttu-id="5f00b-127">Em vez disso, o Windows Media Player passa o código de resultado ao manipulador de eventos **OnSendMessageComplete** no parâmetro *Result* .</span><span class="sxs-lookup"><span data-stu-id="5f00b-127">Instead, Windows Media Player passes the result code along to the **OnSendMessageComplete** event handler in the *Result* parameter.</span></span>

<span data-ttu-id="5f00b-128">Nenhum dos parâmetros (*msg*, *param*, *Result*) do manipulador de eventos **OnSendMessageComplete** é interpretado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5f00b-128">None of the parameters (*Msg*, *Param*, *Result*) of the **OnSendMessageComplete** event handler is interpreted by Windows Media Player.</span></span> <span data-ttu-id="5f00b-129">Os parâmetros têm significado apenas para a loja online.</span><span class="sxs-lookup"><span data-stu-id="5f00b-129">The parameters have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f00b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f00b-130">Requirements</span></span>



| <span data-ttu-id="5f00b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f00b-131">Requirement</span></span> | <span data-ttu-id="5f00b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5f00b-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f00b-133">Versão</span><span class="sxs-lookup"><span data-stu-id="5f00b-133">Version</span></span><br/> | <span data-ttu-id="5f00b-134">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="5f00b-134">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="5f00b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5f00b-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="5f00b-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f00b-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f00b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f00b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f00b-138">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="5f00b-138">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="5f00b-139">**External. sendMessage**</span><span class="sxs-lookup"><span data-stu-id="5f00b-139">**External.sendMessage**</span></span>](external-sendmessage.md)
</dt> <dt>

[<span data-ttu-id="5f00b-140">**IWMPContentPartner:: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="5f00b-140">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="5f00b-141">**IWMPContentPartnerCallback::SendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="5f00b-141">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





