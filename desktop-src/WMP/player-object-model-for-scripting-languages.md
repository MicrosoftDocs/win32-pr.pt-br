---
title: Modelo de objeto do Player para linguagens de script
description: Modelo de objeto do Player para linguagens de script
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Windows Media Player, modelo de objeto
- Modelo de objeto do Windows Media Player, sobre
- modelo de objeto, sobre
- Controle ActiveX do Windows Media Player, modelo de objeto
- Controle ActiveX, modelo de objeto
- Controle ActiveX móvel do Windows Media Player, modelo de objeto
- Windows Media Player Mobile, modelo de objeto
- Software Development Kit (SDK), modelo de objeto de controle ActiveX do Windows Media Player
- SDK (Software Development Kit), modelo de objeto de controle ActiveX do Windows Media Player
- documentação, modelo de objeto de controle ActiveX do Windows Media Player
- Windows Media Player, linguagens de script
- Modelo de objeto do Windows Media Player, linguagens de script
- modelo de objeto, linguagens de script
- Controle ActiveX do Windows Media Player, linguagens de script
- Controle ActiveX, linguagens de script
- Controle ActiveX móvel do Windows Media Player, linguagens de script
- Windows Media Player Mobile, linguagens de script
- linguagens de script
- Windows Media Player, objeto Player
- Modelo de objeto do Windows Media Player, objeto Player
- modelo de objeto, objeto Player
- Controle ActiveX do Windows Media Player, objeto Player
- Controle ActiveX, objeto Player
- Controle ActiveX móvel do Windows Media Player, objeto Player
- Windows Media Player Mobile, objeto Player
- Objeto de jogador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559831"
---
# <a name="player-object-model-for-scripting-languages"></a><span data-ttu-id="d557d-129">Modelo de objeto do Player para linguagens de script</span><span class="sxs-lookup"><span data-stu-id="d557d-129">Player Object Model for Scripting Languages</span></span>

<span data-ttu-id="d557d-130">O ActiveX usa o conceito de objetos para conter funcionalidade de programação.</span><span class="sxs-lookup"><span data-stu-id="d557d-130">ActiveX uses the concept of objects to contain programming functionality.</span></span> <span data-ttu-id="d557d-131">O Windows Media Player usa vários objetos para dividir a funcionalidade que o controle fornece.</span><span class="sxs-lookup"><span data-stu-id="d557d-131">Windows Media Player uses several objects to divide up the functionality the control provides.</span></span> <span data-ttu-id="d557d-132">O objeto raiz é o objeto de **jogador** e os outros objetos são anexados ao objeto **Player** por meio de propriedades específicas.</span><span class="sxs-lookup"><span data-stu-id="d557d-132">The root object is the **Player** object, and the other objects are attached to the **Player** object through specific properties.</span></span>

<span data-ttu-id="d557d-133">O diagrama a seguir mostra como o modelo de objeto de controle ActiveX do Windows Media Player 11 funciona para linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="d557d-133">The following diagram shows how the Windows Media Player 11 ActiveX control object model works for scripting languages.</span></span>

![diagrama do modelo de objeto do Windows Media Player 11](images/playeromdiag.png)

<span data-ttu-id="d557d-135">Em C++ e, às vezes, em linguagens .NET, os objetos são representados por interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="d557d-135">In C++, and sometimes in .NET languages, objects are represented by COM interfaces.</span></span> <span data-ttu-id="d557d-136">No modelo de objeto do Windows Media Player, os nomes de interface COM são iguais ao nome do objeto, mas são prefixados com "IWMP".</span><span class="sxs-lookup"><span data-stu-id="d557d-136">In the Windows Media Player object model, COM interface names are the same as the object name, but are prefixed with "IWMP".</span></span> <span data-ttu-id="d557d-137">Por exemplo, o objeto de **rede** é exposto por meio da interface **IWMPNetwork** .</span><span class="sxs-lookup"><span data-stu-id="d557d-137">For example, the **Network** object is exposed through the **IWMPNetwork** interface.</span></span>

<span data-ttu-id="d557d-138">As seções a seguir fornecem visões gerais conceituais para cada objeto:</span><span class="sxs-lookup"><span data-stu-id="d557d-138">The following sections provide conceptual overviews for each object:</span></span>

-   [<span data-ttu-id="d557d-139">Sobre os objetos cdrom e cdromCollection</span><span class="sxs-lookup"><span data-stu-id="d557d-139">About the Cdrom and CdromCollection Objects</span></span>](about-the-cdrom-and-cdromcollection-objects.md)
-   [<span data-ttu-id="d557d-140">Sobre o objeto ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="d557d-140">About the ClosedCaption Object</span></span>](about-the-closedcaption-object.md)
-   [<span data-ttu-id="d557d-141">Sobre o objeto Controls</span><span class="sxs-lookup"><span data-stu-id="d557d-141">About the Controls Object</span></span>](about-the-controls-object.md)
-   [<span data-ttu-id="d557d-142">Sobre o objeto DVD</span><span class="sxs-lookup"><span data-stu-id="d557d-142">About the DVD Object</span></span>](about-the-dvd-object.md)
-   [<span data-ttu-id="d557d-143">Sobre os objetos Error e ErrorItem</span><span class="sxs-lookup"><span data-stu-id="d557d-143">About the Error and ErrorItem Objects</span></span>](about-the-error-and-erroritem-objects.md)
-   [<span data-ttu-id="d557d-144">Sobre o Mediacollection e os objetos de mídia</span><span class="sxs-lookup"><span data-stu-id="d557d-144">About the MediaCollection and Media Objects</span></span>](about-the-mediacollection-and-media-objects.md)
-   [<span data-ttu-id="d557d-145">Sobre o objeto MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="d557d-145">About the MetadataPicture Object</span></span>](about-the-metadatapicture-object.md)
-   [<span data-ttu-id="d557d-146">Sobre o objeto MetadataText</span><span class="sxs-lookup"><span data-stu-id="d557d-146">About the MetadataText Object</span></span>](about-the-metadatatext-object.md)
-   [<span data-ttu-id="d557d-147">Sobre o objeto de rede</span><span class="sxs-lookup"><span data-stu-id="d557d-147">About the Network Object</span></span>](about-the-network-object.md)
-   [<span data-ttu-id="d557d-148">Sobre o objeto do Player</span><span class="sxs-lookup"><span data-stu-id="d557d-148">About the Player Object</span></span>](about-the-player-object.md)
-   [<span data-ttu-id="d557d-149">Sobre o objeto PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="d557d-149">About the PlayerApplication Object</span></span>](about-the-playerapplication-object.md)
-   [<span data-ttu-id="d557d-150">Sobre os objetos playlist, Playlistcollection e PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="d557d-150">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [<span data-ttu-id="d557d-151">Sobre o objeto de consulta</span><span class="sxs-lookup"><span data-stu-id="d557d-151">About the Query Object</span></span>](about-the-query-object.md)
-   [<span data-ttu-id="d557d-152">Sobre o objeto de configurações</span><span class="sxs-lookup"><span data-stu-id="d557d-152">About the Settings Object</span></span>](about-the-settings-object.md)
-   [<span data-ttu-id="d557d-153">Sobre o objeto StringCollection</span><span class="sxs-lookup"><span data-stu-id="d557d-153">About the StringCollection Object</span></span>](about-the-stringcollection-object.md)

<span data-ttu-id="d557d-154">A funcionalidade adicional está disponível por meio de determinadas interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="d557d-154">Additional functionality is available through certain COM interfaces.</span></span> <span data-ttu-id="d557d-155">Se você pode acessar essas interfaces pode depender do idioma usado para a programação e outros fatores, como o modo usado para criar a instância do controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d557d-155">Whether you can access these interfaces may depend on the language you use for programming and other factors, such as the mode used to create the instance of the Windows Media Player control.</span></span> <span data-ttu-id="d557d-156">Para obter uma lista completa de interfaces COM expostas pelo controle do Windows Media Player, consulte a [referência de modelo de objeto para C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="d557d-156">For a complete list of COM interfaces exposed by the Windows Media Player control, see the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d557d-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d557d-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d557d-158">**Sobre o modelo de objeto do Player**</span><span class="sxs-lookup"><span data-stu-id="d557d-158">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="d557d-159">**Usando o controle do Windows Media Player em uma solução de .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="d557d-159">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




