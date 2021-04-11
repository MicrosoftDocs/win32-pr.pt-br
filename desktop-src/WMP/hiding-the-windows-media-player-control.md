---
title: Ocultando o controle do Windows Media Player
description: Ocultando o controle do Windows Media Player
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Controle ActiveX do Windows Media Player, páginas da Web
- Controle ActiveX móvel do Windows Media Player, páginas da Web
- Controle ActiveX, páginas da Web
- inserindo, páginas da Web
- Windows Media Player, ocultando o controle ActiveX
- Modelo de objeto do Windows Media Player, ocultando o controle ActiveX
- modelo de objeto, ocultando o controle ActiveX
- Windows Media Player Mobile, controle hidingActiveX
- Controle ActiveX do Windows Media Player, ocultando
- Controle ActiveX móvel do Windows Media Player, ocultando
- Controle ActiveX, ocultando
- Controle ActiveX do Windows Media Player, páginas da Web
- Controle ActiveX móvel do Windows Media Player, páginas da Web
- Controle ActiveX, páginas da Web
- Incorporação de página da Web, ocultando o controle ActiveX
- ocultando o controle ActiveX do Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292553"
---
# <a name="hiding-the-windows-media-player-control"></a><span data-ttu-id="f7d1d-126">Ocultando o controle do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="f7d1d-126">Hiding the Windows Media Player Control</span></span>

<span data-ttu-id="f7d1d-127">O objeto ActiveX do Windows Media Player é inserido em uma página da Web usando o elemento OBJECT.</span><span class="sxs-lookup"><span data-stu-id="f7d1d-127">The Windows Media Player ActiveX object is embedded in a webpage using the OBJECT element.</span></span> <span data-ttu-id="f7d1d-128">Ao contrário das versões anteriores, o elemento OBJECT que define o Windows Media Player deve ser colocado na seção BODY de uma página da Web, entre as marcas <BODY> e </BODY> .</span><span class="sxs-lookup"><span data-stu-id="f7d1d-128">Unlike earlier versions, the OBJECT element that defines Windows Media Player must be placed in the BODY section of a webpage, between the <BODY> and </BODY> tags.</span></span> <span data-ttu-id="f7d1d-129">Colocar o objeto ActiveX do Windows Media Player na seção de cabeçalho de uma página da Web para ocultar a interface do usuário pode produzir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="f7d1d-129">Placing the Windows Media Player ActiveX object in the HEAD section of a webpage to hide the user interface can produce unexpected results.</span></span>

<span data-ttu-id="f7d1d-130">Se você colocar o controle ActiveX do Windows Media Player na seção corpo de uma página da Web, a interface do usuário de controle será exibida.</span><span class="sxs-lookup"><span data-stu-id="f7d1d-130">If you put the Windows Media Player ActiveX control in the BODY section of a webpage, the control user interface will be displayed.</span></span> <span data-ttu-id="f7d1d-131">Se você não quiser que ele seja exibido e deseja criar sua própria interface do usuário, defina os atributos Height e Width do elemento OBJECT como zero.</span><span class="sxs-lookup"><span data-stu-id="f7d1d-131">If you do not want it to be displayed, and wish to create your own user interface, set the height and width attributes of the OBJECT element to zero.</span></span>

<span data-ttu-id="f7d1d-132">O controle também pode ser invisível definindo o *Player*. Propriedade **UIMODE** como "invisível".</span><span class="sxs-lookup"><span data-stu-id="f7d1d-132">The control can also be made invisible by setting the *Player*.**uiMode** property to "invisible".</span></span> <span data-ttu-id="f7d1d-133">Isso pode ser feito usando uma marca PARAM, conforme discutido na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="f7d1d-133">This can be done using a PARAM tag as discussed in the next section.</span></span> <span data-ttu-id="f7d1d-134">Nesse caso, o espaço é reservado para o controle usando altura e largura, mas nada é exibido no espaço reservado até que **UIMODE** seja alterado para algo diferente de "invisível".</span><span class="sxs-lookup"><span data-stu-id="f7d1d-134">In this case, space is reserved for the control using height and width, but nothing is displayed in the reserved space until **uiMode** is changed to something other than "invisible".</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7d1d-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7d1d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7d1d-136">**Usando o controle do Windows Media Player em uma página da Web**</span><span class="sxs-lookup"><span data-stu-id="f7d1d-136">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




