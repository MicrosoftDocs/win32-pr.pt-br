---
title: Comprando conteúdo de mídia
description: Comprando conteúdo de mídia
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Lojas online do Windows Media Player, comprando conteúdo de mídia
- lojas online, comprando conteúdo de mídia
- Digite 1 lojas online, comprando conteúdo de mídia
- Lojas online do Windows Media Player, compras de conteúdo de mídia
- lojas online, compras de conteúdo de mídia
- Digite 1 lojas online, compras de conteúdo de mídia
- conteúdo de mídia, comprando
- comprando conteúdo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e420f1dce607e1c596c48490d10bbe8a2a5a5f61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916973"
---
# <a name="purchasing-media-content"></a><span data-ttu-id="a19fc-111">Comprando conteúdo de mídia</span><span class="sxs-lookup"><span data-stu-id="a19fc-111">Purchasing Media Content</span></span>

<span data-ttu-id="a19fc-112">Quando o Windows Media Player exibe o conteúdo de música no modo de exibição de árvore de biblioteca, a interface do usuário inclui elementos que o usuário pode clicar para comprar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a19fc-112">When Windows Media Player displays music content in the library tree view, the user interface includes elements that the user can click to buy the content.</span></span> <span data-ttu-id="a19fc-113">Por exemplo, o usuário pode clicar em um botão para comprar uma música individual ou para comprar um álbum inteiro.</span><span class="sxs-lookup"><span data-stu-id="a19fc-113">For example, the user might click a button to buy an individual song or to buy an entire album.</span></span>

<span data-ttu-id="a19fc-114">Se o repositório online ativo for um repositório do tipo 1, o Windows Media Player terá acesso a preços de acompanhamento, álbum e lista no catálogo da loja online.</span><span class="sxs-lookup"><span data-stu-id="a19fc-114">If the active online store is a Type 1 store, Windows Media Player has access to track, album, and list prices in the online store's catalog.</span></span> <span data-ttu-id="a19fc-115">Esses preços no catálogo são cadeias de caracteres que têm um formato compreendido somente pela loja online.</span><span class="sxs-lookup"><span data-stu-id="a19fc-115">Those prices in the catalog are strings that have a format understood only by the online store.</span></span> <span data-ttu-id="a19fc-116">O Windows Media Player não interpreta as cadeias de caracteres de preço; Ele simplesmente as exibe em elementos da interface do usuário, como botões de compra.</span><span class="sxs-lookup"><span data-stu-id="a19fc-116">Windows Media Player does not interpret price strings; it merely displays them in user interface elements like Buy buttons.</span></span>

<span data-ttu-id="a19fc-117">Quando o Windows Media Player configura uma compra para um conjunto de itens de mídia, ele passa as IDs e os preços dos itens de mídia para o plug-in de parceiro de conteúdo chamando [IWMPContentPartner:: CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent).</span><span class="sxs-lookup"><span data-stu-id="a19fc-117">When Windows Media Player sets up a purchase for a set of media items, it passes the IDs and prices of the media items to the content partner plug-in by calling [IWMPContentPartner::CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent).</span></span> <span data-ttu-id="a19fc-118">Nesse ponto, o plug-in pode inspecionar os preços fornecidos pelo jogador.</span><span class="sxs-lookup"><span data-stu-id="a19fc-118">At that point, the plug-in can inspect the prices provided by the Player.</span></span> <span data-ttu-id="a19fc-119">Estes são os preços que o usuário espera pagar; ou seja, os preços que o jogador exibiu ao usuário.</span><span class="sxs-lookup"><span data-stu-id="a19fc-119">These are the prices that the user expects to pay; that is, the prices that the Player displayed to the user.</span></span> <span data-ttu-id="a19fc-120">Com base nas IDs de mídia e nos preços fornecidos pelo Player, o plug-in calcula um preço total, que ele retorna ao Player no parâmetro *bstrTotalPrice* .</span><span class="sxs-lookup"><span data-stu-id="a19fc-120">Based on the media IDs and prices provided by the Player, the plug-in calculates a total price, which it returns to the Player in the *bstrTotalPrice* parameter.</span></span> <span data-ttu-id="a19fc-121">Os preços que o Player passa para o **CanBuySilent** fornecem o plug-in com informações, mas não obrigam o plug-in a retornar um determinado preço total.</span><span class="sxs-lookup"><span data-stu-id="a19fc-121">The prices that the Player passes to **CanBuySilent** provide the plug-in with information, but they do not obligate the plug-in to return a certain total price.</span></span> <span data-ttu-id="a19fc-122">O plug-in pode calcular o preço total conforme ele se ajusta.</span><span class="sxs-lookup"><span data-stu-id="a19fc-122">The plug-in can calculate the total price as it sees fit.</span></span>

<span data-ttu-id="a19fc-123">Além de calcular o preço total de uma compra, o **CanBuySilent** determina se o purchace pode continuar silenciosamente; ou seja, sem exibir uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a19fc-123">In addition to calculating the total price of a purchase, **CanBuySilent** determines whether the purchace can proceed silently; that is, without displaying a dialog box.</span></span> <span data-ttu-id="a19fc-124">Se **CanBuySilent** retornar **true**, o Windows Media Player simplesmente altera o texto no botão comprar para solicitar que o usuário confirme a compra.</span><span class="sxs-lookup"><span data-stu-id="a19fc-124">If **CanBuySilent** returns **True**, Windows Media Player simply changes the text on the Buy button to prompt the user to confirm the purchase.</span></span> <span data-ttu-id="a19fc-125">Se **CanBuySilent** retornar **false**, o Windows Media Player exibirá uma caixa de diálogo solicitando que o usuário confirme a compra.</span><span class="sxs-lookup"><span data-stu-id="a19fc-125">If **CanBuySilent** returns **False**, Windows Media Player displays a dialog box that prompts the user to confirm the purchase.</span></span> <span data-ttu-id="a19fc-126">A caixa de diálogo fornece ao usuário informações que resumem a compra, como o número de álbuns, o número de faixas individuais e o preço total (conforme retornado pelo plug-in).</span><span class="sxs-lookup"><span data-stu-id="a19fc-126">The dialog box provides the user with information that summarizes the purchase like number of albums, number of individual tracks, and the total price (as returned by the plug-in).</span></span>

<span data-ttu-id="a19fc-127">Depois que o usuário confirmar a compra, o jogador chamará [IWMPContentPartner:: Buy](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy).</span><span class="sxs-lookup"><span data-stu-id="a19fc-127">After the user confirms the purchase, the Player calls [IWMPContentPartner::Buy](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy).</span></span> <span data-ttu-id="a19fc-128">Essa chamada de método fornece o plug-in com a mesma lista de contêineres de conteúdo que **CanBuySilent**.</span><span class="sxs-lookup"><span data-stu-id="a19fc-128">This method call provides the plug-in with the same content container list as **CanBuySilent**.</span></span> <span data-ttu-id="a19fc-129">Ao chamar **comprar**, o Windows Media Player também fornece um cookie (simplesmente um valor **DWORD** , exclusivo para a sessão) que o plug-in pode usar para identificar a transação.</span><span class="sxs-lookup"><span data-stu-id="a19fc-129">When calling **Buy**, Windows Media Player also provides a cookie (simply a **DWORD** value, unique for the session) that the plug-in can use to identify the transaction.</span></span> <span data-ttu-id="a19fc-130">Quando a transação é concluída, o plug-in deve chamar [IWMPContentPartnerCallback:: BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete), passando o valor do cookie original para o parâmetro *dwBuyCookie* , para notificar o player de que a transação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="a19fc-130">When the transaction is completed, the plug-in must call [IWMPContentPartnerCallback::BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete), passing the original cookie value for the *dwBuyCookie* parameter, to notify the Player that the transaction is finished.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a19fc-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a19fc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a19fc-132">**Guia de programação para lojas online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="a19fc-132">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




