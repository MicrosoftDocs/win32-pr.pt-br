---
title: Legendagem oculta
description: Legendagem oculta
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Windows Media Player, SAMI (intercâmbio de mídia acessível) sincronizado
- Modelo de objeto do Windows Media Player, SAMI (sincronização de mídia acessível)
- modelo de objeto, SAMI (intercâmbio de mídia acessível) sincronizado
- Windows Media Player Mobile, SAMI (sincronização de mídia acessível) sincronizado
- Controle ActiveX do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX móvel do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX, SAMI (sincronização de mídia acessível)
- Windows Media Player, migrando legendas ocultas
- Modelo de objeto do Windows Media Player, legendas codificadas do Smigrating
- modelo de objeto, migrando legendas ocultas
- Windows Media Player Mobile, migrando legendas ocultas
- Controle ActiveX do Windows Media Player, migrando legendas ocultas
- Controle ActiveX móvel do Windows Media Player, migrando legendas ocultas
- Controle ActiveX, migrando legendas ocultas
- SAMI (intercâmbio de mídia acessível) sincronizado, migrando legendas ocultas
- SAMI (sincronizado com o intercâmbio de mídia acessível), migrando legendas ocultas
- Guia de migração, SAMI (sincronização de mídia acessível)
- Guia de migração, legendagem oculta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104084376"
---
# <a name="closed-captioning"></a><span data-ttu-id="f2c0c-121">Legendagem oculta</span><span class="sxs-lookup"><span data-stu-id="f2c0c-121">Closed Captioning</span></span>

<span data-ttu-id="f2c0c-122">O controle ActiveX do Windows Media Player 6,4 inclui um painel de exibição de legenda oculta integrada que, quando torna-se visível, habilita legendas codificadas SAMI (intercâmbio de mídia acessível) e exibe o texto da legenda oculta.</span><span class="sxs-lookup"><span data-stu-id="f2c0c-122">The Windows Media Player 6.4 ActiveX control includes an integrated closed caption display panel that, when made visible, enables Synchronized Accessible Media Interchange (SAMI) closed captions and displays the closed caption text.</span></span> <span data-ttu-id="f2c0c-123">O controle Windows Media Player 7 ou posterior habilita a exibição da legenda fechada do SAMI usando um **<DIV>** elemento HTML.</span><span class="sxs-lookup"><span data-stu-id="f2c0c-123">The Windows Media Player 7 or later control enables SAMI closed caption display by using an HTML **<DIV>** element.</span></span> <span data-ttu-id="f2c0c-124">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f2c0c-124">For example:</span></span>


```C++
<DIV  ID = "CCDiv"></DIV>

```



<span data-ttu-id="f2c0c-125">Essa técnica oferece flexibilidade total, já que você pode criar sua página da Web para exibir legendas ocultas de uma maneira personalizada; a exibição de legenda oculta não precisa mais estar em um local fixo adjacente à interface do usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f2c0c-125">This technique provides you with complete flexibility, since you can design your webpage to display closed captions in a customized manner; the closed caption display is no longer required to be in a fixed location adjacent to the Windows Media Player user interface.</span></span>

<span data-ttu-id="f2c0c-126">Depois de criar uma área para exibir legendas codificadas, use o *ClosedCaption*. Propriedade **captioningID** para especificar o local em que o Windows Media Player renderiza o texto da legenda oculta.</span><span class="sxs-lookup"><span data-stu-id="f2c0c-126">Once you have created an area to display closed captions, use the *ClosedCaption*.**captioningID** property to specify the location where Windows Media Player renders the closed caption text.</span></span>


```C++
Player.closedCaption.captioningID = "CCDiv";

```



<span data-ttu-id="f2c0c-127">O SDK (Software Development Kit) do Windows Media Player contém um exemplo funcional de um player incorporado que exibe texto de legenda oculta.</span><span class="sxs-lookup"><span data-stu-id="f2c0c-127">The Windows Media Player Software Development Kit (SDK) contains a working sample of an embedded Player that displays closed caption text.</span></span> <span data-ttu-id="f2c0c-128">Para obter as amostras do SDK, baixe e instale o SDK completo do Windows Media Player no site da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f2c0c-128">To get the SDK samples, download and install the complete Windows Media Player SDK from the Microsoft Web Site.</span></span> <span data-ttu-id="f2c0c-129">Para obter mais informações sobre legendas codificadas e SAMI, consulte o [site de acessibilidade da Microsoft](https://www.microsoft.com/enable/).</span><span class="sxs-lookup"><span data-stu-id="f2c0c-129">For more information about closed captions and SAMI, see the [Microsoft Accessibility website](https://www.microsoft.com/enable/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2c0c-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2c0c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2c0c-131">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="f2c0c-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="f2c0c-132">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="f2c0c-132">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="f2c0c-133">**Guia de migração do modelo de objeto**</span><span class="sxs-lookup"><span data-stu-id="f2c0c-133">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




