---
title: Correspondendo às cores do Windows Media Player
description: Correspondendo às cores do Windows Media Player
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Lojas online do Windows Media Player, correspondência de cores do Windows Media Player
- lojas online, correspondência de cores do Windows Media Player
- Digite 1 lojas online, correspondência de cores do Windows Media Player
- Digite 2 lojas online, correspondência de cores do Windows Media Player
- Lojas online do Windows Media Player, correspondência de cores do Windows Media Player
- lojas online, correspondência de cores do Windows Media Player
- Digite 1 lojas online, correspondência de cores do Windows Media Player
- Digite 2 lojas online, correspondência de cores do Windows Media Player
- Lojas online do Windows Media Player, correspondência de cores para o Windows Media Player
- lojas online, correspondência de cores para o Windows Media Player
- tipo 1 lojas online, correspondência de cores para o Windows Media Player
- tipo 2 lojas online, correspondência de cores para o Windows Media Player
- correspondência de cores para o Windows Media Player
- correspondência de cores do Windows Media Player
- Windows Media Player, cores correspondentes
- Windows Media Player, correspondência de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765616"
---
# <a name="matching-the-windows-media-player-colors"></a><span data-ttu-id="44990-119">Correspondendo às cores do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="44990-119">Matching the Windows Media Player Colors</span></span>

<span data-ttu-id="44990-120">Fazer com que sua página da Web da loja online corresponda ao esquema de cores do Windows Media Player é fácil.</span><span class="sxs-lookup"><span data-stu-id="44990-120">Making your online store webpage match the Windows Media Player color scheme is easy.</span></span> <span data-ttu-id="44990-121">Simplesmente manipule o evento **external. OnColorChange** .</span><span class="sxs-lookup"><span data-stu-id="44990-121">Simply handle the **External.OnColorChange** event.</span></span> <span data-ttu-id="44990-122">Para especificar uma função para manipular o evento, use um código semelhante ao seguinte quando sua página da Web for carregada:</span><span class="sxs-lookup"><span data-stu-id="44990-122">To specify a function to handle the event, use code like the following when your webpage loads:</span></span>


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



<span data-ttu-id="44990-123">Cada vez que o usuário altera o esquema de cores do Windows Media Player, o Player chamará sua função.</span><span class="sxs-lookup"><span data-stu-id="44990-123">Each time the user changes the color scheme of Windows Media Player, the Player will call your function.</span></span> <span data-ttu-id="44990-124">O exemplo a seguir mostra uma função simples que define o plano de fundo da página da Web para corresponder à propriedade **external. appColorLight** :</span><span class="sxs-lookup"><span data-stu-id="44990-124">The following example shows a simple function that sets the webpage background to match the **External.appColorLight** property:</span></span>


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



<span data-ttu-id="44990-125">Também há outras propriedades de cor disponíveis para seu uso.</span><span class="sxs-lookup"><span data-stu-id="44990-125">There are other color properties available for your use as well.</span></span> <span data-ttu-id="44990-126">Consulte [objeto externo para lojas online do tipo 2](external-object-for-type-2-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="44990-126">See [External Object for Type 2 Online Stores](external-object-for-type-2-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="44990-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44990-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44990-128">**External. appColorLight**</span><span class="sxs-lookup"><span data-stu-id="44990-128">**External.appColorLight**</span></span>](external-appcolorlight.md)
</dt> <dt>

[<span data-ttu-id="44990-129">**Evento external. OnColorChange**</span><span class="sxs-lookup"><span data-stu-id="44990-129">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
</dt> <dt>

[<span data-ttu-id="44990-130">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="44990-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




