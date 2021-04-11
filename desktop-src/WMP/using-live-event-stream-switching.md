---
title: Usando a alternância de fluxo de eventos ao vivo
description: Usando a alternância de fluxo de eventos ao vivo
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
keywords:
- Playlists do metarquivo do Windows Media, alternância de fluxo de eventos ao vivo
- listas de reprodução, alternância de fluxo de eventos ao vivo
- listas de reprodução de metarquivo, alternância de fluxo de eventos ao vivo
- Playlists do metarquivo do Windows Media, alternância de fluxo de eventos
- listas de reprodução, alternância de fluxo de eventos
- listas de reprodução de metarquivo, alternância de fluxo de eventos
- Playlists do metarquivo do Windows Media, inserção do AD
- listas de reprodução, inserção de anúncio
- listas de reprodução de metarquivo, inserção de anúncio
- Windows Media Player, alternância de fluxo de eventos ao vivo
- Windows Media Player, alternância de fluxo de eventos
- Windows Media Player, inserção de anúncio
- alternância de fluxo de eventos ao vivo
- alternância de fluxo de eventos
- inserção de anúncio
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159519"
---
# <a name="using-live-event-stream-switching"></a><span data-ttu-id="68d40-118">Usando a alternância de fluxo de eventos ao vivo</span><span class="sxs-lookup"><span data-stu-id="68d40-118">Using Live Event Stream Switching</span></span>

<span data-ttu-id="68d40-119">A mídia de streaming também pode ser controlada pela interação dos comandos de script inseridos em um fluxo de mídia com elementos do metarquivo do Windows Media em uma lista de reprodução de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="68d40-119">Streaming media can also be controlled by the interaction of script commands embedded in a media stream with Windows Media metafile elements in a metafile playlist.</span></span>

<span data-ttu-id="68d40-120">Um evento é um tipo específico de comando de script inserido em um fluxo de mídia ou arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="68d40-120">An event is a particular type of script command embedded in a media stream or media file.</span></span> <span data-ttu-id="68d40-121">Quando o controle do Windows Media Player recebe o comando de script, ele processa o evento conforme definido pelo elemento **Event** na lista de reprodução do metarquivo.</span><span class="sxs-lookup"><span data-stu-id="68d40-121">When the Windows Media Player control receives the script command, it processes the event as defined by the **EVENT** element in the metafile playlist.</span></span> <span data-ttu-id="68d40-122">O Windows Media Player alterna do fluxo atual que está renderizando e renderiza o conteúdo referenciado no elemento de **evento** de playlist de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="68d40-122">Windows Media Player switches from the current stream it is rendering and renders the content referenced in the metafile playlist **EVENT** element.</span></span> <span data-ttu-id="68d40-123">O elemento **Event** geralmente é usado na produção ao vivo.</span><span class="sxs-lookup"><span data-stu-id="68d40-123">The **EVENT** element is usually used in live production.</span></span>

<span data-ttu-id="68d40-124">Um elemento de **evento** é semelhante a um elemento de **entrada** , mas cada um manipula a reprodução de fluxos e arquivos de mídia de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="68d40-124">An **EVENT** element looks similar to an **ENTRY** element, but each handles the playback of streams and media files differently.</span></span> <span data-ttu-id="68d40-125">O elemento **entry** é usado para criar listas de reprodução.</span><span class="sxs-lookup"><span data-stu-id="68d40-125">The **ENTRY** element is used to create playlists.</span></span> <span data-ttu-id="68d40-126">Um fluxo ou arquivo de mídia referenciado em um elemento de **entrada** começa a ser reproduzido quando o fluxo ou o arquivo de mídia referenciado na **entrada** anterior é concluído.</span><span class="sxs-lookup"><span data-stu-id="68d40-126">A stream or media file referenced in an **ENTRY** element starts playing when the stream or media file referenced in the previous **ENTRY** finishes.</span></span> <span data-ttu-id="68d40-127">Um fluxo referenciado em um **evento** é executado somente quando um comando de script específico é recebido.</span><span class="sxs-lookup"><span data-stu-id="68d40-127">A stream referenced in an **EVENT** plays only when a specific script command is received.</span></span> <span data-ttu-id="68d40-128">Por exemplo, quando o Windows Media Player recebe um comando de script com a cadeia de caracteres de tipo "EVENT" e a cadeia de caracteres de comando "Adlink", ele pesquisa os seguintes elementos na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="68d40-128">For example, when Windows Media Player receives a script command with type string "EVENT" and the command string "Adlink", it searches the playlist for the following elements.</span></span>


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



<span data-ttu-id="68d40-129">Em seguida, o Windows Media Player alterna da transmissão ao vivo para reproduzir o fluxo ou o arquivo de mídia contido no **evento**, neste caso, Adlink. WMA.</span><span class="sxs-lookup"><span data-stu-id="68d40-129">Windows Media Player then switches from the live stream to play the stream or media file contained in the **EVENT**, in this case Adlink.wma.</span></span> <span data-ttu-id="68d40-130">O código `WHENDONE="RESUME"` instrui o Windows Media Player a retomar a reprodução do fluxo anterior quando o Adlink. WMA for concluído.</span><span class="sxs-lookup"><span data-stu-id="68d40-130">The code `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous stream when Adlink.wma is finished.</span></span>

> [!Note]  
> <span data-ttu-id="68d40-131">A falha ao manipular todos os eventos inseridos em um fluxo de mídia ou arquivo de mídia pode gerar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="68d40-131">Failure to handle every event embedded in a media stream or media file may yield unexpected results.</span></span>

 

<span data-ttu-id="68d40-132">Se você quiser usar a alternância de fluxo de eventos ao vivo, deverá incluir um elemento de **evento** em sua lista de reprodução para manipular cada comando de script de evento inserido nos fluxos de mídia ou nos arquivos de mídia em sua lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="68d40-132">If you want to use live event stream switching, you must include one **EVENT** element in your playlist to handle each event script command embedded in the media streams or media files in your playlist.</span></span> <span data-ttu-id="68d40-133">Antes de criar sua lista de reprodução, você deve saber os detalhes sobre quais comandos de script são inseridos no seu conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="68d40-133">Before you create your playlist, you must know the details about which script commands are embedded in your digital media content.</span></span> <span data-ttu-id="68d40-134">Se houver um comando de script de evento que você deseja que o Windows Media Player ignore, inclua um elemento de **evento** em sua lista de reprodução para manipular o evento, mas faça referência a uma URL fictícia no manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="68d40-134">If there is an event script command that you want Windows Media Player to ignore, include an **EVENT** element in your playlist to handle the event, but reference a dummy URL in the event handler.</span></span>

## <a name="ad-insertion"></a><span data-ttu-id="68d40-135">Inserção de anúncio</span><span class="sxs-lookup"><span data-stu-id="68d40-135">Ad Insertion</span></span>

<span data-ttu-id="68d40-136">Essa técnica pode ser usada para inserção de anúncios.</span><span class="sxs-lookup"><span data-stu-id="68d40-136">This technique can be used for ad insertion.</span></span> <span data-ttu-id="68d40-137">Por exemplo, durante uma transmissão ao vivo pela Internet de um jogo de bola, um comando pode ser enviado no início de cada interrupção comercial que instrui cada cliente (Windows Media Player) a reproduzir comerciais listados em sua lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="68d40-137">For example, during a live Internet broadcast of a ball game, a command can be sent at the beginning of every commercial break that instructs each client (Windows Media Player) to play commercials listed in its playlist.</span></span> <span data-ttu-id="68d40-138">Quando os clientes terminarem de reproduzir os negócios, a lista de reprodução instruirá cada cliente a recortar para a transmissão ao vivo.</span><span class="sxs-lookup"><span data-stu-id="68d40-138">When clients finish playing the commercials, the playlist instructs each client to cut back to the live broadcast.</span></span> <span data-ttu-id="68d40-139">O conteúdo de mídia do **evento** será renderizado somente quando a mídia de streaming que está sendo acessada difundir o script incorporado com o nome do **evento** correspondente.</span><span class="sxs-lookup"><span data-stu-id="68d40-139">The **EVENT** media content will be rendered only when the streaming media being accessed broadcasts embedded scripting with the matching **EVENT** name.</span></span>

<span data-ttu-id="68d40-140">As possibilidades inerentes à alternância de **eventos** são mais bem apreciadas ao contrastarem como os anúncios atingem os visualizadores por meio de transmissão padrão por satélite com o modo como os anúncios podem acessar os visualizadores usando tecnologias de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="68d40-140">The possibilities inherent in **EVENT** switching are best appreciated by contrasting how ads reach viewers through standard, over-the-air broadcasting with how ads can reach viewers using Windows Media Technologies.</span></span> <span data-ttu-id="68d40-141">Historicamente, os anúncios de difusão podem ser apenas aproximadamente direcionados para os visualizadores, usando dados de classificação como os critérios primários.</span><span class="sxs-lookup"><span data-stu-id="68d40-141">Historically, broadcast ads could only be roughly targeted at viewers, using ratings data as the primary criteria.</span></span> <span data-ttu-id="68d40-142">Os anúncios enviados usando tecnologias de mídia do Windows podem ser direcionados diretamente ao usuário de destino, pois os **eventos** e as listas de reprodução podem ser criados dinamicamente com base na entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="68d40-142">Ads sent using Windows Media Technologies can be aimed directly at the target user because **EVENTs** and playlists can be built on the fly based on user input.</span></span> <span data-ttu-id="68d40-143">Para obter mais informações, consulte [Personalizando a entrega de mídia](personalizing-media-delivery.md).</span><span class="sxs-lookup"><span data-stu-id="68d40-143">For more information, see [Personalizing Media Delivery](personalizing-media-delivery.md).</span></span>

<span data-ttu-id="68d40-144">Você também pode usar listas de reprodução de metarquivo para exibir gráficos, áudio e texto personalizados para publicidade.</span><span class="sxs-lookup"><span data-stu-id="68d40-144">You can also use metafile playlists to display customized graphics, audio and text for advertising.</span></span> <span data-ttu-id="68d40-145">Você pode usar o elemento **banner** como um elemento filho de um **evento** para exibir um gráfico de mensagem de anúncio.</span><span class="sxs-lookup"><span data-stu-id="68d40-145">You can use the **BANNER** element as a child element of an **EVENT** to display an advertising message graphic.</span></span> <span data-ttu-id="68d40-146">O elemento **banner** fornece o caminho e o arquivo que contém os elementos gráficos para sua faixa publicitária.</span><span class="sxs-lookup"><span data-stu-id="68d40-146">The **BANNER** element provides the path and file containing the graphics for your advertising banner.</span></span> <span data-ttu-id="68d40-147">Você também pode fornecer um link para um site ou arquivo usando o elemento filho **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="68d40-147">You can also provide a link to a site or file using the **MOREINFO** child element.</span></span> <span data-ttu-id="68d40-148">A URL no elemento **moreinfo** pode fornecer um link para ainda mais anúncios na Web.</span><span class="sxs-lookup"><span data-stu-id="68d40-148">The URL in the **MOREINFO** element can provide a link to even more advertisements on the Web.</span></span> <span data-ttu-id="68d40-149">O exemplo a seguir demonstra como usar esses elementos.</span><span class="sxs-lookup"><span data-stu-id="68d40-149">The following example demonstrates using these elements.</span></span>

<span data-ttu-id="68d40-150">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="68d40-150">Example Code</span></span>


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



<span data-ttu-id="68d40-151">O exemplo a seguir insere o AD anúncio. WMA no fluxo unicast de difusão BallGame quando um cliente recebe um **evento** de comando de script com o atributo **Name** definido como "tempo limite".</span><span class="sxs-lookup"><span data-stu-id="68d40-151">The following example inserts the ad Advert.wma into the broadcast unicast stream BallGame when a client receives a script command **EVENT** with the **NAME** attribute set to "Time-Out".</span></span> <span data-ttu-id="68d40-152">**CLIENTSKIP** é definido como não para impedir que o anúncio em fluxo seja ignorado.</span><span class="sxs-lookup"><span data-stu-id="68d40-152">**CLIENTSKIP** is set to NO to prevent the streamed ad from being skipped.</span></span> <span data-ttu-id="68d40-153">Neste exemplo, o anúncio transmitido deve ser reproduzido antes de retornar ao fluxo original.</span><span class="sxs-lookup"><span data-stu-id="68d40-153">In this example, the streamed ad must be played before returning to the original stream.</span></span> <span data-ttu-id="68d40-154">Quando o anúncio é concluído, o cliente retoma a reprodução do fluxo original.</span><span class="sxs-lookup"><span data-stu-id="68d40-154">When the ad is finished, the client resumes playing the original stream.</span></span>

<span data-ttu-id="68d40-155">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="68d40-155">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="68d40-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68d40-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68d40-157">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="68d40-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="68d40-158">**Usando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="68d40-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="68d40-159">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="68d40-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="68d40-160">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="68d40-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




