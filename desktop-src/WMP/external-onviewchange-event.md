---
title: Evento external. OnViewChange
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O evento OnViewChange ocorre quando a exibição é alterada no Windows Media Player.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Evento external. OnViewChange do Windows Media Player
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796417"
---
# <a name="externalonviewchange-event"></a><span data-ttu-id="7bcaf-106">Evento external. OnViewChange</span><span class="sxs-lookup"><span data-stu-id="7bcaf-106">External.OnViewChange Event</span></span>

> [!Note]  
> <span data-ttu-id="7bcaf-107">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="7bcaf-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7bcaf-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="7bcaf-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7bcaf-109">O evento **OnViewChange** ocorre quando a exibição é alterada no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7bcaf-109">The **OnViewChange** event occurs when the view changes in Windows Media Player.</span></span>

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="7bcaf-110">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="7bcaf-110">Possible Values</span></span>

<span data-ttu-id="7bcaf-111">Essa é uma propriedade somente gravação que especifica o nome da função no script que o Windows Media Player chama quando o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="7bcaf-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="7bcaf-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bcaf-112">Parameters</span></span>

<span data-ttu-id="7bcaf-113">A função que manipula esse evento não usa parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7bcaf-113">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bcaf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bcaf-114">Remarks</span></span>

<span data-ttu-id="7bcaf-115">O modo de exibição no Windows Media Player pode ser alterado por qualquer um dos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="7bcaf-115">The view in Windows Media Player can change for any of the following reasons:</span></span>

-   <span data-ttu-id="7bcaf-116">O usuário interage com a interface do usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7bcaf-116">The user interacts with the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="7bcaf-117">O usuário interage com uma página de descoberta e o script na página de descoberta chama [external. changeView](external-changeview.md).</span><span class="sxs-lookup"><span data-stu-id="7bcaf-117">The user interacts with a discovery page, and script on the discovery page calls [External.changeView](external-changeview.md).</span></span>
-   <span data-ttu-id="7bcaf-118">O usuário interage com uma página de descoberta e o script na página de descoberta chama [external. changeViewOnlineList](external-changeviewonlinelist.md).</span><span class="sxs-lookup"><span data-stu-id="7bcaf-118">The user interacts with a discovery page, and script on the discovery page calls [External.changeViewOnlineList](external-changeviewonlinelist.md).</span></span>

<span data-ttu-id="7bcaf-119">Quando a exibição é alterada no Windows Media Player, o Player chama [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) para obter a URL da próxima página de descoberta a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="7bcaf-119">When the view changes in Windows Media Player, the Player calls [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) to get the URL of the next discovery page to display.</span></span> <span data-ttu-id="7bcaf-120">No entanto, antes de o Player exibir a página nova descoberta, ele gera o evento **OnViewChange** .</span><span class="sxs-lookup"><span data-stu-id="7bcaf-120">However, before the Player displays the new discovery page, it raises the **OnViewChange** event.</span></span> <span data-ttu-id="7bcaf-121">Se o manipulador de eventos **OnViewChange** chamar [external. cancelNavigate](external-cancelnavigate.md), o Windows Media Player não exibirá a página nova descoberta.</span><span class="sxs-lookup"><span data-stu-id="7bcaf-121">If the **OnViewChange** event handler calls [External.cancelNavigate](external-cancelnavigate.md), Windows Media Player does not display the new discovery page.</span></span> <span data-ttu-id="7bcaf-122">Em vez disso, ele continua a exibir a página de descoberta atual.</span><span class="sxs-lookup"><span data-stu-id="7bcaf-122">Instead, it continues to display the current discovery page.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bcaf-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bcaf-123">Requirements</span></span>



| <span data-ttu-id="7bcaf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bcaf-124">Requirement</span></span> | <span data-ttu-id="7bcaf-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7bcaf-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7bcaf-126">Versão</span><span class="sxs-lookup"><span data-stu-id="7bcaf-126">Version</span></span><br/> | <span data-ttu-id="7bcaf-127">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="7bcaf-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="7bcaf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7bcaf-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="7bcaf-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bcaf-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bcaf-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bcaf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bcaf-131">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="7bcaf-131">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="7bcaf-132">**External. changeView**</span><span class="sxs-lookup"><span data-stu-id="7bcaf-132">**External.changeView**</span></span>](external-changeview.md)
</dt> <dt>

[<span data-ttu-id="7bcaf-133">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="7bcaf-133">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> </dl>

 

 





