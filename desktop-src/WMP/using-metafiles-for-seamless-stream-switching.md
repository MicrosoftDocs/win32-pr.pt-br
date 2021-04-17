---
title: Usando os metaarquivos para alternância de fluxo contínuo
description: Usando os metaarquivos para alternância de fluxo contínuo
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
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
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763028"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a><span data-ttu-id="60527-118">Usando os metaarquivos para alternância de fluxo contínuo</span><span class="sxs-lookup"><span data-stu-id="60527-118">Using Metafiles for Seamless Stream Switching</span></span>

<span data-ttu-id="60527-119">Você pode facilitar a alternância de fluxo contínuo usando listas de reprodução de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="60527-119">You can facilitate seamless stream switching using metafile playlists.</span></span> <span data-ttu-id="60527-120">Normalmente, quando uma parte do conteúdo termina, o buffer ocorre no próximo clipe ou fluxo antes de ser aberto (se for o conteúdo recebido de um servidor de mídia de streaming).</span><span class="sxs-lookup"><span data-stu-id="60527-120">Usually, when a piece of content ends, buffering occurs for the next clip or stream before it opens (if it is content received from a streaming media server).</span></span> <span data-ttu-id="60527-121">O Microsoft Windows Media Services permite que você elimine, ou pelo menos minimize, esse tempo de buffer e que outra parte do conteúdo transmitido comece a tocar quase imediatamente.</span><span class="sxs-lookup"><span data-stu-id="60527-121">Microsoft Windows Media Services enables you to eliminate, or at least minimize, this buffering time and have another piece of streamed content begin playing nearly immediately.</span></span> <span data-ttu-id="60527-122">O modo normal de operação do Windows Media Player é abrir o próximo fluxo de mídia referenciado pela playlist 20 segundos antes do final do fluxo processado no momento.</span><span class="sxs-lookup"><span data-stu-id="60527-122">The normal mode of operation for Windows Media Player is to open the next media stream referenced by the playlist 20 seconds before the end of the currently rendered stream.</span></span> <span data-ttu-id="60527-123">Isso geralmente fornece uma transição direta entre fluxos de mídia, dependendo de outros fatores, como tempos de acesso à Web.</span><span class="sxs-lookup"><span data-stu-id="60527-123">This generally provides a seamless transition between media streams, depending on other factors such as Web access times.</span></span>

<span data-ttu-id="60527-124">Use o elemento **Event** em uma playlist em conjunto com comandos OpenEvent do codificador para facilitar a alternância direta entre fluxos ou arquivos.</span><span class="sxs-lookup"><span data-stu-id="60527-124">Use the **EVENT** element in a playlist in conjunction with OPENEVENT commands from the encoder to facilitate seamless switching between streams or files.</span></span> <span data-ttu-id="60527-125">O envio de um comando OPENEVENT de 20 segundos ou mais antes do comando de evento pode minimizar atrasos na alternância de fluxo.</span><span class="sxs-lookup"><span data-stu-id="60527-125">Sending an OPENEVENT command 20 seconds or more prior to the EVENT command can minimize delays in stream switching.</span></span> <span data-ttu-id="60527-126">Em seguida, o Windows Media Player é capaz de pré-carregar uma parte do próximo conteúdo de streaming em um buffer.</span><span class="sxs-lookup"><span data-stu-id="60527-126">Then Windows Media Player is able to preload a portion of the upcoming streaming content into a buffer.</span></span>

<span data-ttu-id="60527-127">Use o Windows Media Encoder para enviar um comando de script no fluxo usando o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="60527-127">Use Windows Media Encoder to send a script command in the stream using the following format:</span></span>


```XML
OPENEVENT eventname 

```



<span data-ttu-id="60527-128">O nome do evento deve ser aquele definido no elemento **Event** na playlist.</span><span class="sxs-lookup"><span data-stu-id="60527-128">The event name must be the one defined in the **EVENT** element in the playlist.</span></span> <span data-ttu-id="60527-129">Quando o Windows Media Player recebe um comando de script OPENEVENT do codificador, ele procura o elemento de **evento** na lista de reprodução e começa a armazenar em buffer o clipe ou fluxo definido no elemento de **evento** .</span><span class="sxs-lookup"><span data-stu-id="60527-129">When Windows Media Player receives an OPENEVENT script command from the encoder, it looks to the **EVENT** element in the playlist and begins buffering the clip or stream defined in the **EVENT** element.</span></span> <span data-ttu-id="60527-130">Em seguida, o Windows Media Player mantém essas informações até o evento real de mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="60527-130">Windows Media Player then holds this information until the actual event of the same name.</span></span> <span data-ttu-id="60527-131">Quando o evento nomeado é recebido, o Windows Media Player alterna para o conteúdo anteriormente armazenado em buffer.</span><span class="sxs-lookup"><span data-stu-id="60527-131">When the named event is received, Windows Media Player switches to that previously buffered content.</span></span>

> [!Note]  
> <span data-ttu-id="60527-132">Você não pode usar caracteres Unicode para o comando de script OPENEVENT no arquivo de mídia ou no elemento de **evento** na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="60527-132">You cannot use Unicode characters for the OPENEVENT script command in the media file or the **EVENT** element in the playlist.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="60527-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60527-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60527-134">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="60527-134">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="60527-135">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="60527-135">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="60527-136">**Evento Player. ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="60527-136">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="60527-137">**Usando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="60527-137">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="60527-138">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="60527-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="60527-139">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="60527-139">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




