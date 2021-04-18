---
title: Usando o script em uma página da Web exibida pelo Firefox
description: Usando o script em uma página da Web exibida pelo Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
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
- Controle ActiveX do Windows Media Player, exemplo de script
- Controle ActiveX móvel do Windows Media Player, exemplo de script
- Controle ActiveX, exemplo de script
- inserindo, páginas da Web
- Inserção de página da Web, exemplo de script
- Windows Media Player, Firefox
- Modelo de objeto do Windows Media Player, Firefox
- modelo de objeto, Firefox
- Windows Media Player Mobile, Firefox
- Controle ActiveX do Windows Media Player, Firefox
- Controle ActiveX móvel do Windows Media Player, Firefox
- Controle ActiveX, Firefox
- Firefox, exemplo de script
- Incorporação de página da Web, Firefox
- exemplo de script para inserção de página da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "105771522"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="1aab7-128">Usando o script em uma página da Web exibida pelo Firefox</span><span class="sxs-lookup"><span data-stu-id="1aab7-128">Using Script in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="1aab7-129">O script em uma página da Web pode usar o modelo de objeto do Player para controlar o Player à medida que o usuário interage com a página.</span><span class="sxs-lookup"><span data-stu-id="1aab7-129">Script on a webpage can use the Player object model to control the Player as the user interacts with the page.</span></span> <span data-ttu-id="1aab7-130">Por exemplo, o elemento INPUT a seguir tem um script que define o volume do Player.</span><span class="sxs-lookup"><span data-stu-id="1aab7-130">For example, the following INPUT element has script that sets the Player volume.</span></span>


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



<span data-ttu-id="1aab7-131">Muitos dos objetos no modelo de objeto do Windows Media Player têm suporte do Internet Explorer e do plug-in do Firefox.</span><span class="sxs-lookup"><span data-stu-id="1aab7-131">Many of the objects in the Windows Media Player object model are supported by Internet Explorer and by the Firefox plug-in.</span></span> <span data-ttu-id="1aab7-132">No entanto, há alguns objetos que não têm suporte do plug-in do Firefox.</span><span class="sxs-lookup"><span data-stu-id="1aab7-132">However, there are some objects that are not supported by the Firefox plug-in.</span></span> <span data-ttu-id="1aab7-133">A tabela a seguir lista todos os objetos no modelo de objeto do Player e mostra quais objetos têm suporte no plug-in do Firefox.</span><span class="sxs-lookup"><span data-stu-id="1aab7-133">The following table lists all of the objects in the Player object model and shows which objects are supported by the Firefox plug-in.</span></span>



| <span data-ttu-id="1aab7-134">Objeto</span><span class="sxs-lookup"><span data-stu-id="1aab7-134">Object</span></span>                                              | <span data-ttu-id="1aab7-135">Suporte do Firefox</span><span class="sxs-lookup"><span data-stu-id="1aab7-135">Firefox support</span></span> |
|-----------------------------------------------------|-----------------|
| [<span data-ttu-id="1aab7-136">ROMs</span><span class="sxs-lookup"><span data-stu-id="1aab7-136">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="1aab7-137">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-137">no</span></span>              |
| [<span data-ttu-id="1aab7-138">CdromCollection</span><span class="sxs-lookup"><span data-stu-id="1aab7-138">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="1aab7-139">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-139">no</span></span>              |
| [<span data-ttu-id="1aab7-140">ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="1aab7-140">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="1aab7-141">sim</span><span class="sxs-lookup"><span data-stu-id="1aab7-141">yes</span></span>             |
| [<span data-ttu-id="1aab7-142">Controles</span><span class="sxs-lookup"><span data-stu-id="1aab7-142">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="1aab7-143">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-143">no</span></span>              |
| [<span data-ttu-id="1aab7-144">DVD</span><span class="sxs-lookup"><span data-stu-id="1aab7-144">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="1aab7-145">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-145">no</span></span>              |
| [<span data-ttu-id="1aab7-146">Erro</span><span class="sxs-lookup"><span data-stu-id="1aab7-146">Error</span></span>](error-object.md)                           | <span data-ttu-id="1aab7-147">sim</span><span class="sxs-lookup"><span data-stu-id="1aab7-147">yes</span></span>             |
| [<span data-ttu-id="1aab7-148">ErrorItem</span><span class="sxs-lookup"><span data-stu-id="1aab7-148">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="1aab7-149">sim</span><span class="sxs-lookup"><span data-stu-id="1aab7-149">yes</span></span>             |
| [<span data-ttu-id="1aab7-150">Mídia</span><span class="sxs-lookup"><span data-stu-id="1aab7-150">Media</span></span>](media-object.md)                           | <span data-ttu-id="1aab7-151">sim</span><span class="sxs-lookup"><span data-stu-id="1aab7-151">yes</span></span>             |
| [<span data-ttu-id="1aab7-152">Mediacollection</span><span class="sxs-lookup"><span data-stu-id="1aab7-152">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="1aab7-153">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-153">no</span></span>              |
| [<span data-ttu-id="1aab7-154">MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="1aab7-154">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="1aab7-155">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-155">no</span></span>              |
| [<span data-ttu-id="1aab7-156">MetadataText</span><span class="sxs-lookup"><span data-stu-id="1aab7-156">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="1aab7-157">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-157">no</span></span>              |
| [<span data-ttu-id="1aab7-158">Rede</span><span class="sxs-lookup"><span data-stu-id="1aab7-158">Network</span></span>](network-object.md)                       | <span data-ttu-id="1aab7-159">sim</span><span class="sxs-lookup"><span data-stu-id="1aab7-159">yes</span></span>             |
| [<span data-ttu-id="1aab7-160">Jogador</span><span class="sxs-lookup"><span data-stu-id="1aab7-160">Player</span></span>](player-object.md)                         | <span data-ttu-id="1aab7-161">sim</span><span class="sxs-lookup"><span data-stu-id="1aab7-161">yes</span></span>             |
| [<span data-ttu-id="1aab7-162">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="1aab7-162">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="1aab7-163">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-163">no</span></span>              |
| [<span data-ttu-id="1aab7-164">7.1</span><span class="sxs-lookup"><span data-stu-id="1aab7-164">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="1aab7-165">sim</span><span class="sxs-lookup"><span data-stu-id="1aab7-165">yes</span></span>             |
| [<span data-ttu-id="1aab7-166">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="1aab7-166">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="1aab7-167">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-167">no</span></span>              |
| [<span data-ttu-id="1aab7-168">Playlistcollection</span><span class="sxs-lookup"><span data-stu-id="1aab7-168">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="1aab7-169">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-169">no</span></span>              |
| [<span data-ttu-id="1aab7-170">Consulta</span><span class="sxs-lookup"><span data-stu-id="1aab7-170">Query</span></span>](query-object.md)                           | <span data-ttu-id="1aab7-171">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-171">no</span></span>              |
| [<span data-ttu-id="1aab7-172">Configurações</span><span class="sxs-lookup"><span data-stu-id="1aab7-172">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="1aab7-173">sim</span><span class="sxs-lookup"><span data-stu-id="1aab7-173">yes</span></span>             |
| [<span data-ttu-id="1aab7-174">StringCollection</span><span class="sxs-lookup"><span data-stu-id="1aab7-174">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="1aab7-175">não</span><span class="sxs-lookup"><span data-stu-id="1aab7-175">no</span></span>              |



 

<span data-ttu-id="1aab7-176">O plug-in do Firefox dá suporte ao objeto **Player** , mas determinadas propriedades do objeto **Player** retornam **NULL** em um navegador Firefox.</span><span class="sxs-lookup"><span data-stu-id="1aab7-176">The Firefox plug-in supports the **Player** object, but certain properties of the **Player** object return **NULL** in a Firefox browser.</span></span> <span data-ttu-id="1aab7-177">Por exemplo, a propriedade [cdromCollection](player-cdromcollection.md) do objeto **Player** retorna **NULL** porque o plug-in do Firefox não oferece suporte ao objeto **cdrom** .</span><span class="sxs-lookup"><span data-stu-id="1aab7-177">For example, the [cdromCollection](player-cdromcollection.md) property of the **Player** object returns **NULL** because the Firefox plug-in does not support the **Cdrom** object.</span></span> <span data-ttu-id="1aab7-178">Da mesma forma, as propriedades [DVD](player-dvd.md), [mediacollection](player-mediacollection.md), [playerApplication](player-playerapplication.md)e [playlistcollection](player-playlistcollection.md) do objeto **Player** retornam **NULL** em um navegador Firefox.</span><span class="sxs-lookup"><span data-stu-id="1aab7-178">Similarly, the [dvd](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md), and [playlistCollection](player-playlistcollection.md) properties of the **Player** object return **NULL** in a Firefox browser.</span></span>

<span data-ttu-id="1aab7-179">A propriedade **Player. pluginVersionInfo** é suportada pelo plug-in do Firefox, mas não pelo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1aab7-179">The **Player.pluginVersionInfo** property is supported by the Firefox plug-in but not by Internet Explorer.</span></span> <span data-ttu-id="1aab7-180">Essa propriedade retorna a versão do plug-in do Firefox.</span><span class="sxs-lookup"><span data-stu-id="1aab7-180">This property returns the version of the Firefox plug-in.</span></span>

<span data-ttu-id="1aab7-181">O plug-in do Firefox dá suporte ao objeto de **mídia** , incluindo a propriedade [getItemInfoByType](media-getiteminfobytype.md) .</span><span class="sxs-lookup"><span data-stu-id="1aab7-181">The Firefox plug-in supports the **Media** object, including the [getItemInfoByType](media-getiteminfobytype.md) property.</span></span> <span data-ttu-id="1aab7-182">No entanto, em um navegador Firefox, a propriedade **getItemInfoByType** não dá suporte aos tipos de retorno **MetadataText** e **MetadataPicture** .</span><span class="sxs-lookup"><span data-stu-id="1aab7-182">However, in a Firefox browser, the **getItemInfoByType** property does not support the **MetadataText** and **MetadataPicture** return types.</span></span>

<span data-ttu-id="1aab7-183">O plug-in do Firefox dá suporte ao objeto de [configurações](settings-object.md) , exceto para o método [setmode](settings-setmode.md) e a propriedade [requestMediaAccessRights](settings-requestmediaaccessrights.md) .</span><span class="sxs-lookup"><span data-stu-id="1aab7-183">The Firefox plug-in supports the [Settings](settings-object.md) object except for the [setMode](settings-setmode.md) method and the [requestMediaAccessRights](settings-requestmediaaccessrights.md) property.</span></span> <span data-ttu-id="1aab7-184">Em um navegador Firefox, a propriedade **requestMediaAccessRight** sempre retorna false.</span><span class="sxs-lookup"><span data-stu-id="1aab7-184">In a Firefox browser, the **requestMediaAccessRight** property always returns false.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1aab7-185">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1aab7-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aab7-186">**Usando o controle do Windows Media Player com o Firefox**</span><span class="sxs-lookup"><span data-stu-id="1aab7-186">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




