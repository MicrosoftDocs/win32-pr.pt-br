---
title: Evento external. OnLoginChange
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnLoginChange
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Evento external. OnLoginChange do Windows Media Player
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760437"
---
# <a name="externalonloginchange-event"></a><span data-ttu-id="23c61-105">Evento external. OnLoginChange</span><span class="sxs-lookup"><span data-stu-id="23c61-105">External.OnLoginChange Event</span></span>

> [!Note]  
> <span data-ttu-id="23c61-106">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="23c61-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="23c61-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="23c61-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="23c61-108">O evento **OnLoginChange** ocorre quando o status de logon do usuário é alterado ou quando uma tentativa de logon falha.</span><span class="sxs-lookup"><span data-stu-id="23c61-108">The **OnLoginChange** event occurs when the user's log-in status changes or when an attempt to log in fails.</span></span>

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="23c61-109">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="23c61-109">Possible Values</span></span>

<span data-ttu-id="23c61-110">Essa é uma propriedade somente gravação que especifica o nome da função no script que o Windows Media Player chama quando o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="23c61-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="23c61-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23c61-111">Parameters</span></span>

<span data-ttu-id="23c61-112">A função que manipula esse evento não usa parâmetros.</span><span class="sxs-lookup"><span data-stu-id="23c61-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="23c61-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="23c61-113">Remarks</span></span>

<span data-ttu-id="23c61-114">Esse evento ocorre toda vez que o plug-in do repositório online chama [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnLoginStateChange no parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="23c61-114">This event occurs every time the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="23c61-115">Às vezes, o plug-in faz essa chamada para notificar o Windows Media Player de que houve uma alteração no estado de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="23c61-115">Sometimes the plug-in makes this call to notify Windows Media Player that there was a change in the user's log-in state.</span></span> <span data-ttu-id="23c61-116">Em outras ocasiões, o plug-in faz essa chamada para notificar o player que uma tentativa de fazer logon falhou.</span><span class="sxs-lookup"><span data-stu-id="23c61-116">Other times, the plug-in makes this call to notify the Player that an attempt to log in failed.</span></span> <span data-ttu-id="23c61-117">O parâmetro *pContext* do método **Notify** especifica se a notificação é para uma alteração de estado de logon ou para uma tentativa de logon com falha.</span><span class="sxs-lookup"><span data-stu-id="23c61-117">The *pContext* parameter of the **Notify** method specifies whether the notification is for a change of log-in state or for a failed log-in attempt.</span></span>

<span data-ttu-id="23c61-118">Como cada chamada para `Notify(wmpcnLoginStateChange, ...)` faz com que o Windows Media Player gere o evento **OnLoginChange** , o manipulador de eventos **OnLoginChange** é chamado às vezes como resultado de uma alteração no estado de logon e, às vezes, do resultado de uma tentativa de logon com falha.</span><span class="sxs-lookup"><span data-stu-id="23c61-118">Because every call to `Notify(wmpcnLoginStateChange, ...)` causes Windows Media Player to raise the **OnLoginChange** event, the **OnLoginChange** event handler is called sometimes as the result of a change in log-in state and sometimes as the result of a failed log-in attempt.</span></span> <span data-ttu-id="23c61-119">Para determinar o estado de logon atual do usuário, o manipulador de eventos **OnLoginChange** deve chamar [external. userlogind](external-userloggedin.md).</span><span class="sxs-lookup"><span data-stu-id="23c61-119">To determine the user's current log-in state, the **OnLoginChange** event handler must call [External.userLoggedIn](external-userloggedin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23c61-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23c61-120">Requirements</span></span>



| <span data-ttu-id="23c61-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="23c61-121">Requirement</span></span> | <span data-ttu-id="23c61-122">Valor</span><span class="sxs-lookup"><span data-stu-id="23c61-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23c61-123">Versão</span><span class="sxs-lookup"><span data-stu-id="23c61-123">Version</span></span><br/> | <span data-ttu-id="23c61-124">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="23c61-124">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="23c61-125">DLL</span><span class="sxs-lookup"><span data-stu-id="23c61-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="23c61-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23c61-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23c61-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="23c61-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c61-128">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="23c61-128">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="23c61-129">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="23c61-129">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="23c61-130">**External. userlogado**</span><span class="sxs-lookup"><span data-stu-id="23c61-130">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





