---
title: Usando elementos PARAM em uma página da Web exibida pelo Firefox
description: Usando elementos PARAM em uma página da Web exibida pelo Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Windows Media Player, elementos PARAM no elemento OBJECT
- Modelo de objeto do Windows Media Player, elementos PARAM no elemento OBJECT
- modelo de objeto, elementos PARAM no elemento OBJECT
- Windows Media Player Mobile, elementos PARAM no elemento OBJECT
- Controle ActiveX do Windows Media Player, elementos PARAM no elemento OBJECT
- Controle ActiveX móvel do Windows Media Player, elementos PARAM no elemento OBJECT
- Controle ActiveX, elementos PARAM no elemento OBJECT
- inserindo, páginas da Web
- Inserção de página da Web, elementos PARAM no elemento OBJECT
- Elementos PARAM no elemento OBJECT
- Windows Media Player, Firefox
- Modelo de objeto do Windows Media Player, Firefox
- modelo de objeto, Firefox
- Windows Media Player Mobile, Firefox
- Controle ActiveX do Windows Media Player, Firefox
- Controle ActiveX móvel do Windows Media Player, Firefox
- Controle ActiveX, Firefox
- Elementos do Firefox, PARAM no elemento OBJECT
- Incorporação de página da Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b045d111ff3cd0de09f54a8cf7ac25028fa1dc6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104292906"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="feb7a-122">Usando elementos PARAM em uma página da Web exibida pelo Firefox</span><span class="sxs-lookup"><span data-stu-id="feb7a-122">Using PARAM Elements in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="feb7a-123">Você pode usar elementos PARAM dentro de um elemento OBJECT para definir o estado inicial do controle Player.</span><span class="sxs-lookup"><span data-stu-id="feb7a-123">You can use PARAM elements inside an OBJECT element to set the initial state of the Player control.</span></span> <span data-ttu-id="feb7a-124">Por exemplo, os elementos PARAM no exemplo a seguir especificam que o controle deve executar Seattle. wmv automaticamente.</span><span class="sxs-lookup"><span data-stu-id="feb7a-124">For example, the PARAM elements in the following example specify that the control should play seattle.wmv automatically.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



<span data-ttu-id="feb7a-125">A maioria dos elementos PARAM pode ser interpretada pelo Internet Explorer e pelo Firefox.</span><span class="sxs-lookup"><span data-stu-id="feb7a-125">Most PARAM elements can be interpreted by Internet Explorer and by Firefox.</span></span> <span data-ttu-id="feb7a-126">No entanto, há alguns elementos PARAM para os quais o plug-in Firefox não oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="feb7a-126">However, there are a few PARAM elements that the Firefox plug-in does not support.</span></span> <span data-ttu-id="feb7a-127">Para obter informações sobre quais elementos PARAM são suportados pelo plug-in do Firefox, consulte [elementos param em um elemento Object](param-elements-in-an-object-element.md).</span><span class="sxs-lookup"><span data-stu-id="feb7a-127">For information about which PARAM elements are supported by the Firefox plug-in, see [PARAM Elements in an OBJECT Element](param-elements-in-an-object-element.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="feb7a-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="feb7a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feb7a-129">**Usando o controle do Windows Media Player com o Firefox**</span><span class="sxs-lookup"><span data-stu-id="feb7a-129">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




