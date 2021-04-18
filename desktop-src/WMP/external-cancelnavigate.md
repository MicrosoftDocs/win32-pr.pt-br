---
title: Método external. cancelNavigate
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Método external. cancelNavigate
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- método cancelNavigate Windows Media Player
- método cancelNavigate Windows Media Player, classe externa
- Classe externa Windows Media Player, método cancelNavigate
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6cbc0f749fd6ca33d78dfaed1d256634eb9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760438"
---
# <a name="externalcancelnavigate-method"></a><span data-ttu-id="8476c-107">Método external. cancelNavigate</span><span class="sxs-lookup"><span data-stu-id="8476c-107">External.cancelNavigate method</span></span>

> [!Note]  
> <span data-ttu-id="8476c-108">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="8476c-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="8476c-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="8476c-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="8476c-110">O método **cancelNavigate** informa ao Windows Media Player que ele não deve exibir uma nova página de descoberta, embora a exibição tenha sido alterada no Player.</span><span class="sxs-lookup"><span data-stu-id="8476c-110">The **cancelNavigate** method informs Windows Media Player that it should not display a new discovery page even though the view has changed in the Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="8476c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8476c-111">Syntax</span></span>


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a><span data-ttu-id="8476c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8476c-112">Parameters</span></span>

<span data-ttu-id="8476c-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8476c-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8476c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8476c-114">Return value</span></span>

<span data-ttu-id="8476c-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8476c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8476c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8476c-116">Remarks</span></span>

<span data-ttu-id="8476c-117">Quando a exibição é alterada no Windows Media Player, o Player chama o plug-in da loja online para determinar qual página de descoberta exibir em seguida.</span><span class="sxs-lookup"><span data-stu-id="8476c-117">When the view changes in Windows Media Player, the Player calls the online store's plug-in to determine which discovery page to display next.</span></span> <span data-ttu-id="8476c-118">Em alguns casos, no entanto, a loja online pode querer que o Player continue exibindo a página de descoberta existente.</span><span class="sxs-lookup"><span data-stu-id="8476c-118">In some cases, however, the online store might want the Player to continue displaying the existing discovery page.</span></span> <span data-ttu-id="8476c-119">O processo a seguir determina se o Player exibe uma nova página de descoberta:</span><span class="sxs-lookup"><span data-stu-id="8476c-119">The following process determines whether the Player displays a new discovery page:</span></span>

1.  <span data-ttu-id="8476c-120">Uma ação do usuário, na interface do usuário do Player ou na página descoberta, solicita que o Player altere sua exibição.</span><span class="sxs-lookup"><span data-stu-id="8476c-120">An action by the user, either in the Player's user interface or on the discovery page, requests that the Player change its view.</span></span>
2.  <span data-ttu-id="8476c-121">O Player chama o método [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) do plug-in para determinar qual página de descoberta exibir em seguida.</span><span class="sxs-lookup"><span data-stu-id="8476c-121">The Player calls the plug-in's [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to determine which discovery page to display next.</span></span> <span data-ttu-id="8476c-122">O Player armazena a URL da nova página de descoberta, mas não exibe a página nova descoberta neste momento.</span><span class="sxs-lookup"><span data-stu-id="8476c-122">The Player stores the URL of the new discovery page but does not display the new discovery page at this time.</span></span>
3.  <span data-ttu-id="8476c-123">O Player gera o evento [OnViewChange](external-onviewchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="8476c-123">The Player raises the [OnViewChange](external-onviewchange-event.md) event.</span></span>
4.  <span data-ttu-id="8476c-124">Se o manipulador de eventos **OnViewChange** na página de descoberta chamar **CancelNavigate**, o Player não exibirá a página nova descoberta (determinada na etapa 2).</span><span class="sxs-lookup"><span data-stu-id="8476c-124">If the **OnViewChange** event handler on the discovery page calls **cancelNavigate**, the Player does not display the new discovery page (determined in step 2).</span></span> <span data-ttu-id="8476c-125">Em vez disso, ele continua a exibir a página de descoberta existente.</span><span class="sxs-lookup"><span data-stu-id="8476c-125">Instead, it continues to display the existing discovery page.</span></span> <span data-ttu-id="8476c-126">Se o manipulador de eventos **OnViewChange** não chamar **CancelNavigate**, o Player exibirá a página nova descoberta.</span><span class="sxs-lookup"><span data-stu-id="8476c-126">If the **OnViewChange** event handler does not call **cancelNavigate**, the Player does display the new discovery page.</span></span>

<span data-ttu-id="8476c-127">Por exemplo, suponha que o Player esteja exibindo atualmente a exibição de um álbum com determinada faixa selecionada.</span><span class="sxs-lookup"><span data-stu-id="8476c-127">For example, suppose the Player is currently displaying the view of an album with a certain track selected.</span></span> <span data-ttu-id="8476c-128">Suponha também que a página de descoberta atual é a página que representa o álbum inteiro.</span><span class="sxs-lookup"><span data-stu-id="8476c-128">Also assume that the current discovery page is the page that represents the entire album.</span></span> <span data-ttu-id="8476c-129">Se o usuário clicar em uma faixa diferente do mesmo álbum, a exibição do jogador será levemente alterada para mostrar que a nova faixa está selecionada.</span><span class="sxs-lookup"><span data-stu-id="8476c-129">If the user clicks a different track from the same album, the Player's view changes slightly to show that the new track is selected.</span></span> <span data-ttu-id="8476c-130">Mas não há necessidade de exibir uma nova página de descoberta.</span><span class="sxs-lookup"><span data-stu-id="8476c-130">But there is no need to display a new discovery page.</span></span> <span data-ttu-id="8476c-131">A página de descoberta que representa todo o álbum ainda é a página apropriada para o Player exibir.</span><span class="sxs-lookup"><span data-stu-id="8476c-131">The discovery page that represents the entire album is still the appropriate page for the Player to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="8476c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8476c-132">Requirements</span></span>



| <span data-ttu-id="8476c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8476c-133">Requirement</span></span> | <span data-ttu-id="8476c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="8476c-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8476c-135">Versão</span><span class="sxs-lookup"><span data-stu-id="8476c-135">Version</span></span><br/> | <span data-ttu-id="8476c-136">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="8476c-136">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="8476c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8476c-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="8476c-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8476c-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8476c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="8476c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8476c-140">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="8476c-140">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8476c-141">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="8476c-141">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="8476c-142">**External. OnViewChange**</span><span class="sxs-lookup"><span data-stu-id="8476c-142">**External.OnViewChange**</span></span>](external-onviewchange-event.md)
</dt> </dl>

 

 





