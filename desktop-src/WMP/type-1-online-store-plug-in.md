---
title: Tipo 1 plug-in de loja online
description: Tipo 1 plug-in de loja online
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Repositórios online do Windows Media Player, plug-ins
- lojas online, plug-ins
- Digite 1 lojas online, plug-ins
- Lojas online do Windows Media Player, interface IWMPContentPartner
- lojas online, interface IWMPContentPartner
- Digite 1 lojas online, interface IWMPContentPartner
- plug-ins, lojas online do Windows Media Player
- plug-ins, lojas online
- plug-ins, digite 1 lojas online
- plug-ins, interface IWMPContentPartner
- Plug-ins do Windows Media Player, tipo 1 lojas online
- Plug-ins do Windows Media Player, lojas online
- Plug-ins do Windows Media Player, lojas online do Windows Media Player
- Plug-ins do Windows Media Player, interface IWMPContentPartner
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007248"
---
# <a name="type-1-online-store-plug-in"></a><span data-ttu-id="15229-118">Tipo 1 plug-in de loja online</span><span class="sxs-lookup"><span data-stu-id="15229-118">Type 1 Online Store Plug-in</span></span>

<span data-ttu-id="15229-119">Para aproveitar os recursos de integração de biblioteca, digite 1 provedores de loja online devem criar um plug-in que implemente a interface [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="15229-119">To take advantage of library integration features, type 1 online store providers must create a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="15229-120">Essa interface fornece os métodos que o Windows Media Player chama para notificar a loja online sobre as atividades que estão ocorrendo no Player e recuperar informações específicas sobre o conteúdo da loja online, o catálogo ou a própria loja.</span><span class="sxs-lookup"><span data-stu-id="15229-120">This interface provides the methods that Windows Media Player calls to notify the online store about activities taking place in the Player and to retrieve specific information about online store content, the catalog, or the store itself.</span></span>

<span data-ttu-id="15229-121">Depois que o Windows Media Player instancia o plug-in, o jogador chama [IWMPContentPartner:: SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)e fornece um ponteiro para a interface **IWMPContentPartnerCallback** .</span><span class="sxs-lookup"><span data-stu-id="15229-121">After Windows Media Player instantiates the plug-in, the Player calls [IWMPContentPartner::SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback), and provides a pointer to the **IWMPContentPartnerCallback** interface.</span></span> <span data-ttu-id="15229-122">Essa interface fornece ao armazenamento online uma maneira de fazer chamadas no Windows Media Player para fornecer informações de status ou para iniciar processos específicos, como baixar uma faixa de música.</span><span class="sxs-lookup"><span data-stu-id="15229-122">This interface gives the online store a way to make calls into Windows Media Player to provide status information or to initiate specific processes, such as downloading a music track.</span></span>

<span data-ttu-id="15229-123">O Windows Media Player e o plug-in são executados em processos separados.</span><span class="sxs-lookup"><span data-stu-id="15229-123">Windows Media Player and the plug-in run in separate processes.</span></span> <span data-ttu-id="15229-124">O plug-in é um servidor em processo que é executado na DLL padrão alternativa, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="15229-124">The plug-in is an in-process server that runs in the default DLL surrogate, dllhost.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15229-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15229-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15229-126">**Sobre o tipo 1 lojas online**</span><span class="sxs-lookup"><span data-stu-id="15229-126">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="15229-127">**Interface IWMPContentPartner**</span><span class="sxs-lookup"><span data-stu-id="15229-127">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[<span data-ttu-id="15229-128">**Interface IWMPContentPartnerCallback**</span><span class="sxs-lookup"><span data-stu-id="15229-128">**IWMPContentPartnerCallback Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




