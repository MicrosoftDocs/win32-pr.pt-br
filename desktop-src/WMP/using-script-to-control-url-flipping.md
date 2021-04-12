---
title: Usando o script para controlar a inversão de URL
description: Usando o script para controlar a inversão de URL
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player, apresentações baseadas na Web
- Modelo de objeto do Windows Media Player, apresentações baseadas na Web
- modelo de objeto, apresentações baseadas na Web
- Windows Media Player Mobile, apresentações baseadas na Web
- Controle ActiveX do Windows Media Player, apresentações baseadas na Web
- Controle ActiveX móvel do Windows Media Player, apresentações baseadas na Web
- Controle ActiveX, apresentações baseadas na Web
- Windows Media Player, inversão de URL
- Modelo de objeto do Windows Media Player, inversão de URL
- modelo de objeto, inversão de URL
- Windows Media Player Mobile, inversão de URL
- Controle ActiveX do Windows Media Player, inversão de URL
- Controle ActiveX móvel do Windows Media Player, inversão de URL
- Controle ActiveX, inversão de URL
- Apresentações baseadas na Web, inversão de URL
- Criando apresentações baseadas na Web, inversão de URL
- Inversão de URL
- Windows Media Player, streaming de mídia avançada
- Modelo de objeto do Windows Media Player, streaming de mídia avançada
- modelo de objeto, streaming de mídia avançada
- Windows Media Player Mobile, streaming de mídia avançada
- Controle ActiveX do Windows Media Player, streaming de mídia avançada
- Controle ActiveX móvel do Windows Media Player, streaming de mídia avançada
- Controle ActiveX, streaming de mídia avançada
- Apresentações baseadas na Web, streaming de mídia avançada
- Criando apresentações baseadas na Web, streaming de mídia avançado
- streaming de mídia avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4815562bba92d67bb4b02ea0317d6c29accd9262
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104364531"
---
# <a name="using-script-to-control-url-flipping"></a><span data-ttu-id="fba00-130">Usando o script para controlar a inversão de URL</span><span class="sxs-lookup"><span data-stu-id="fba00-130">Using Script to Control URL Flipping</span></span>

<span data-ttu-id="fba00-131">Quando um usuário se conecta a um fluxo de mídia avançado enquanto o fluxo já está em andamento, é possível que a página da Web transmitida seja exibida antes que todos os elementos sejam recebidos e armazenados em cache se o Windows Media Player invocar automaticamente a URL.</span><span class="sxs-lookup"><span data-stu-id="fba00-131">When a user connects to a rich media stream while the stream is already in progress, it is possible for the streamed webpage to display before all the elements have arrived and been cached if Windows Media Player automatically invokes the URL.</span></span> <span data-ttu-id="fba00-132">Quando isso acontece, o usuário vê uma página da Web em branco ou incompleta até que o próximo conjunto de dados chegue no cache.</span><span class="sxs-lookup"><span data-stu-id="fba00-132">When this happens, the user sees a blank or incomplete webpage until the next set of data arrives in the cache.</span></span>

<span data-ttu-id="fba00-133">Você pode evitar a exibição de uma página da Web em branco ou incompleta invocando a URL usando o script em vez de permitir que o Windows Media Player faça isso automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fba00-133">You can avoid displaying a blank or incomplete webpage by invoking the URL using script instead of letting Windows Media Player do it automatically.</span></span> <span data-ttu-id="fba00-134">Dessa forma, você pode ignorar a primeira URL inverter e, em seguida, invocar URLs subsequentes usando o código de script.</span><span class="sxs-lookup"><span data-stu-id="fba00-134">That way, you can ignore the first URL flip and then invoke subsequent URLs by using script code.</span></span>

> [!Note]  
> <span data-ttu-id="fba00-135">Esta seção pressupõe que você esteja transmitindo HTML usando o SDK do Windows Media Encoder 9 Series e que você definiu o fluxo HTML para repetir.</span><span class="sxs-lookup"><span data-stu-id="fba00-135">This section assumes that you are streaming HTML using the Windows Media Encoder 9 Series SDK and that you have set the HTML stream to repeat.</span></span>

 

<span data-ttu-id="fba00-136">Primeiro, você deve criar uma página da Web de conjunto de quadros para conter o quadro com o player incorporado e o quadro que exibe o HTML de streaming.</span><span class="sxs-lookup"><span data-stu-id="fba00-136">First, you must create a frameset webpage to contain the frame with the embedded Player and the frame that displays the streaming HTML.</span></span> <span data-ttu-id="fba00-137">Cada um desses dois quadros exibirá inicialmente uma página da Web separada, portanto, você criará um total de três páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="fba00-137">Each of these two frames will display a separate webpage initially, so you will create a total of three webpages.</span></span> <span data-ttu-id="fba00-138">O código de exemplo a seguir demonstra a página da Web do conjunto de quadros:</span><span class="sxs-lookup"><span data-stu-id="fba00-138">The following example code demonstrates the frameset webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



<span data-ttu-id="fba00-139">O exemplo da página da Web anterior incorpora dois quadros.</span><span class="sxs-lookup"><span data-stu-id="fba00-139">The preceding webpage example incorporates two frames.</span></span> <span data-ttu-id="fba00-140">O primeiro quadro é exibido na metade esquerda da janela do navegador e exibe a página da Web chamada embed \_player.htm.</span><span class="sxs-lookup"><span data-stu-id="fba00-140">The first frame displays in the left half of the browser window and displays the webpage named embed\_player.htm.</span></span> <span data-ttu-id="fba00-141">O código de exemplo a seguir cria esta página da Web:</span><span class="sxs-lookup"><span data-stu-id="fba00-141">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="fba00-142">O segundo quadro no conjunto de quadros é exibido na metade direita da janela do navegador e exibe uma página da Web chamada "blank.htm".</span><span class="sxs-lookup"><span data-stu-id="fba00-142">The second frame in the frameset displays in the right half of the browser window and displays a webpage named "blank.htm".</span></span> <span data-ttu-id="fba00-143">O código de exemplo a seguir cria esta página da Web:</span><span class="sxs-lookup"><span data-stu-id="fba00-143">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



<span data-ttu-id="fba00-144">Quando a página conjunto de quadros é carregada no navegador, o quadro esquerdo mostra o player incorporado e o quadro direito mostra o texto "carregando..." para informar ao usuário que mais dados estão em breve.</span><span class="sxs-lookup"><span data-stu-id="fba00-144">When the frameset page loads in the browser, the left frame shows the embedded Player and the right frame shows the text "Loading..." to inform the user that more data is forthcoming.</span></span> <span data-ttu-id="fba00-145">Quando o comando de script da primeira URL chega do fluxo HTML, o manipulador de eventos simplesmente altera o valor do sinalizador **booliano** .</span><span class="sxs-lookup"><span data-stu-id="fba00-145">When the first URL script command arrives from the HTML stream, the event handler simply changes the value of the **Boolean** flag.</span></span> <span data-ttu-id="fba00-146">Quando cada comando de script de URL subsequente chega do fluxo HTML, o script no manipulador de eventos carrega a nova URL no quadro chamado "content" e a página da Web completa é exibida no quadro localizado na metade direita da janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="fba00-146">When each subsequent URL script command arrives from the HTML stream, the script in the event handler loads the new URL into the frame named "content", and the complete webpage displays in the frame located in the right half of the browser window.</span></span>

<span data-ttu-id="fba00-147">Para obter mais informações sobre o streaming de HTML usando o Windows Media, consulte o SDK do Windows Media Encoder.</span><span class="sxs-lookup"><span data-stu-id="fba00-147">For more information about streaming HTML using Windows Media, see the Windows Media Encoder SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fba00-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fba00-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fba00-149">**Streaming de mídia avançada**</span><span class="sxs-lookup"><span data-stu-id="fba00-149">**Rich Media Streaming**</span></span>](rich-media-streaming.md)
</dt> <dt>

[<span data-ttu-id="fba00-150">**Inversão de URL**</span><span class="sxs-lookup"><span data-stu-id="fba00-150">**URL Flipping**</span></span>](url-flipping.md)
</dt> </dl>

 

 




