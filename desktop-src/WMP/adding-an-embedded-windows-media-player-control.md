---
title: Adicionando um controle do Windows Media Player inserido
description: Adicionando um controle do Windows Media Player inserido
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Playlists do metarquivo do Windows Media, adicionando controles do Windows Media Player inseridos
- listas de reprodução, adicionando controles do Windows Media Player inseridos
- listas de reprodução de metarquivo, adicionando controles do Windows Media Player inseridos
- Listas de reprodução do metarquivo do Windows Media, controles do Windows Media Player inseridos
- listas de reprodução, controles do Windows Media Player inseridos
- listas de reprodução de metarquivo, controles do Windows Media Player inseridos
- Adicionando controles do Windows Media Player inseridos
- controles do Windows Media Player inseridos
- Windows Media Player, adicionando controles inseridos
- Windows Media Player, controles inseridos
- HTMLView, adicionando controles incorporados do Windows Media Player
- HTMLView, controles do Windows Media Player inseridos
- HTMLView, modelo de objeto do Windows Media Player
- HTMLView, modelo de objeto do Player
- Modelo de objeto do Windows Media Player, sobre
- modelo de objeto, sobre
- Objeto de jogador
- Windows Media, modelo de objeto do Player
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364202"
---
# <a name="adding-an-embedded-windows-media-player-control"></a><span data-ttu-id="c9d15-121">Adicionando um controle do Windows Media Player inserido</span><span class="sxs-lookup"><span data-stu-id="c9d15-121">Adding an Embedded Windows Media Player Control</span></span>

<span data-ttu-id="c9d15-122">Há dois motivos pelos quais você pode considerar adicionar uma instância incorporada do Windows Media Player à sua apresentação HTMLView.</span><span class="sxs-lookup"><span data-stu-id="c9d15-122">There are two reasons you might consider adding an embedded instance of Windows Media Player to your HTMLView presentation.</span></span> <span data-ttu-id="c9d15-123">Primeiro, se você quiser exibir conteúdo de vídeo, precisará usar o controle ActiveX do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c9d15-123">First, if you want to display video content, you need to use the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="c9d15-124">Em segundo lugar, se você quiser aproveitar os recursos do modelo de objeto do Windows Media Player de dentro de sua página da Web do HTMLView, deverá usar uma instância do controle de jogador para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="c9d15-124">Second, if you want to take advantage of features of the Windows Media Player object model from within your HTMLView webpage, you must use an instance the Player control to do so.</span></span>

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a><span data-ttu-id="c9d15-125">Usando o controle Player para exibir o vídeo no conteúdo do HTMLView</span><span class="sxs-lookup"><span data-stu-id="c9d15-125">Using the Player control to display video in HTMLView content</span></span>

<span data-ttu-id="c9d15-126">Normalmente, o Windows Media Player exibe vídeo usando o painel vídeo e visualização do recurso de **agora em execução** .</span><span class="sxs-lookup"><span data-stu-id="c9d15-126">Usually, Windows Media Player displays video using the Video and Visualization pane of the **Now Playing** feature.</span></span> <span data-ttu-id="c9d15-127">Como o HTMLView usa essa área para exibir sua página da Web, você deverá fornecer uma área de exibição de vídeo adicional se quiser que o jogador reproduza vídeo.</span><span class="sxs-lookup"><span data-stu-id="c9d15-127">Since HTMLView uses this area to display your webpage, you must supply an additional video display area if you want the Player to play video.</span></span> <span data-ttu-id="c9d15-128">Isso é fácil de usar usando o controle ActiveX do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c9d15-128">This is easy to do by using the Windows Media Player ActiveX control.</span></span>

<span data-ttu-id="c9d15-129">Para usar o controle de jogador para exibir vídeo, incorpore o controle em sua página da Web do HTMLView usando a marca de **objeto** .</span><span class="sxs-lookup"><span data-stu-id="c9d15-129">To use the Player control to display video, embed the control in your HTMLView webpage by using the **OBJECT** tag.</span></span> <span data-ttu-id="c9d15-130">Essa é a mesma técnica usada para inserir o controle do jogador em qualquer página da Web na qual você deseja exibir o vídeo.</span><span class="sxs-lookup"><span data-stu-id="c9d15-130">This is the same technique you use to embed the Player control into any webpage in which you want to display video.</span></span> <span data-ttu-id="c9d15-131">O código de exemplo a seguir mostra a sintaxe básica para inserir o controle de jogador no Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="c9d15-131">The following example code shows the basic syntax for embedding the Player control in Internet Explorer:</span></span>


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



<span data-ttu-id="c9d15-132">O parâmetro *AutoStart* garante que o conteúdo seja reproduzido automaticamente sempre que uma nova URL for especificada.</span><span class="sxs-lookup"><span data-stu-id="c9d15-132">The *autoStart* parameter ensures that content plays automatically whenever a new URL is specified.</span></span> <span data-ttu-id="c9d15-133">O valor especificado para *UIMODE* depende de você, mas geralmente você desejará especificar "None" ao criar conteúdo para apresentações HtmlView.</span><span class="sxs-lookup"><span data-stu-id="c9d15-133">The value you specify for *uiMode* is up to you, but you will usually want to specify "none" when creating content for HTMLView presentations.</span></span> <span data-ttu-id="c9d15-134">Quando você insere o controle do Windows Media Player para exibir vídeo dessa maneira, o usuário pode controlar a reprodução usando os controles do player de modo completo, portanto, não há necessidade de fornecer controles de transporte adicionais na página da Web.</span><span class="sxs-lookup"><span data-stu-id="c9d15-134">When you embed the Windows Media Player control to display video in this manner, the user can control playback using the controls of the full-mode Player, so there's no need to provide additional transport controls in the webpage.</span></span> <span data-ttu-id="c9d15-135">Você pode usar o espaço que normalmente aloca para controles de transporte para exibir mais texto, gráficos ou links para outro conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c9d15-135">You can use the space you would usually allocate for transport controls to display more text, graphics, or links to other content.</span></span>

<span data-ttu-id="c9d15-136">Não especifique um parâmetro de *URL* ao inserir o controle do Windows Media Player em uma página da Web criada para ser exibida em uma apresentação do HtmlView.</span><span class="sxs-lookup"><span data-stu-id="c9d15-136">Do not specify a *URL* parameter when embedding the Windows Media Player control in a webpage designed to display in an HTMLView presentation.</span></span> <span data-ttu-id="c9d15-137">Em vez disso, especifique os arquivos de mídia digital no arquivo. asx que abre o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c9d15-137">Instead, specify the digital media files in the .asx file that opens the content.</span></span>

<span data-ttu-id="c9d15-138">Como você fornece a região de exibição de vídeo em sua página da Web do HTMLView, você pode decidir onde posicionar o vídeo e o tamanho desejado para a região de exibição.</span><span class="sxs-lookup"><span data-stu-id="c9d15-138">Because you provide the video display region in your HTMLView webpage, you can decide where to position the video and how large you want the display region to be.</span></span> <span data-ttu-id="c9d15-139">Por exemplo, você pode conter o objeto **Player** dentro de um elemento HTML **div** e, em seguida, especificar a posição do **div** para Posicione a exibição do vídeo na página da Web.</span><span class="sxs-lookup"><span data-stu-id="c9d15-139">For example, you can contain the **Player** object within an HTML **DIV** element and then specify the position for the **DIV** to situate the video display on the webpage.</span></span> <span data-ttu-id="c9d15-140">Você pode alterar as dimensões da exibição do vídeo especificando valores para os atributos Height e Width do elemento **Object** .</span><span class="sxs-lookup"><span data-stu-id="c9d15-140">You can change the dimensions of the video display by specifying values for the height and width attributes of the **OBJECT** element.</span></span> <span data-ttu-id="c9d15-141">Você também pode especificar esses valores usando o código de script.</span><span class="sxs-lookup"><span data-stu-id="c9d15-141">You can also specify these values using script code.</span></span>

## <a name="using-the-player-object-model"></a><span data-ttu-id="c9d15-142">Usando o modelo de objeto do Player</span><span class="sxs-lookup"><span data-stu-id="c9d15-142">Using the Player object model</span></span>

<span data-ttu-id="c9d15-143">O modelo de objeto do Windows Media Player expõe propriedades, métodos e eventos que você pode usar em suas páginas da Web do HTMLView.</span><span class="sxs-lookup"><span data-stu-id="c9d15-143">The Windows Media Player object model exposes properties, methods, and events that you can use in your HTMLView webpages.</span></span> <span data-ttu-id="c9d15-144">Ao inserir o controle ActiveX do Windows Media Player em sua página da Web do HTMLView, você terá acesso automaticamente ao modelo de objeto do Player.</span><span class="sxs-lookup"><span data-stu-id="c9d15-144">When you embed the Windows Media Player ActiveX control in your HTMLView webpage, you automatically have access to the Player object model.</span></span>

<span data-ttu-id="c9d15-145">Se você inserir o controle do Windows Media Player em sua página da Web do HTMLView, não use o modelo de objeto do Player para especificar o arquivo de mídia digital a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="c9d15-145">If you embed the Windows Media Player control in your HTMLView webpage, do not use the Player object model to specify the digital media file to be played.</span></span> <span data-ttu-id="c9d15-146">Por exemplo, se você usar o código de script para especificar um valor para a propriedade **URL** do controle incorporado, sua página da Web HtmlView será descarregada do recurso em **execução** quando o arquivo de mídia digital for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="c9d15-146">For example, if you use script code to specify a value for the **URL** property of the embedded control, your HTMLView webpage will be unloaded from the **Now Playing** feature when the digital media file plays.</span></span> <span data-ttu-id="c9d15-147">Para evitar que isso aconteça, sempre abra arquivos. asx que incluem parâmetros HTMLView quando você precisa usar o script para abrir o conteúdo de mídia digital na sua página da Web do HTMLView.</span><span class="sxs-lookup"><span data-stu-id="c9d15-147">To prevent this from happening, always open .asx files that include HTMLView parameters when you need to use script to open digital media content from your HTMLView webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9d15-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9d15-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9d15-149">**Exibindo páginas da Web no Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="c9d15-149">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="c9d15-150">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="c9d15-150">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="c9d15-151">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="c9d15-151">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="c9d15-152">**Settings. AutoStart**</span><span class="sxs-lookup"><span data-stu-id="c9d15-152">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 




