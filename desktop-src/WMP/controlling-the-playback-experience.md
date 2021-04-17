---
title: Controlando a experiência de reprodução
description: Controlando a experiência de reprodução
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Playlists do metarquivo do Windows Media, controlando a reprodução
- listas de reprodução, controlando a reprodução
- listas de reprodução de metarquivo, controlando a reprodução
- Playlists do metarquivo do Windows Media, problemas de reprodução
- listas de reprodução, problemas de reprodução
- listas de reprodução de metarquivo, problemas de reprodução
- controlando a reprodução
- Windows Media Player, controlando a reprodução
- Windows Media Player, problemas de reprodução
- HTMLView, problemas de reprodução
- HTMLView, controle de reprodução
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6877b869be8ca38ef9266aedf9318103d0e547ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759729"
---
# <a name="controlling-the-playback-experience"></a><span data-ttu-id="810c9-114">Controlando a experiência de reprodução</span><span class="sxs-lookup"><span data-stu-id="810c9-114">Controlling the Playback Experience</span></span>

<span data-ttu-id="810c9-115">Esta seção aborda alguns dos problemas de reprodução que você pode encontrar ao usar o recurso HTMLView.</span><span class="sxs-lookup"><span data-stu-id="810c9-115">This section discusses some of the playback issues you may encounter when using the HTMLView feature.</span></span>

## <a name="requiring-the-user-to-view-web-based-content"></a><span data-ttu-id="810c9-116">Exigindo que o usuário exiba o conteúdo baseado na Web</span><span class="sxs-lookup"><span data-stu-id="810c9-116">Requiring the user to view Web-based content</span></span>

<span data-ttu-id="810c9-117">Você pode decidir que só deseja que os usuários possam desfrutar do conteúdo de mídia digital quando o conteúdo baseado na Web do HTMLView também é exibido.</span><span class="sxs-lookup"><span data-stu-id="810c9-117">You may decide that you only want users to be able to enjoy your digital media content when the HTMLView Web-based content is also displayed.</span></span> <span data-ttu-id="810c9-118">Você pode incluir o código de script em sua página da Web do HTMLView que parará a reprodução do conteúdo de mídia digital se o usuário mudar para o recurso que agora está em **execução** .</span><span class="sxs-lookup"><span data-stu-id="810c9-118">You can include script code in your HTMLView webpage that stops playback of the digital media content if the user switches away from the **Now Playing** feature.</span></span> <span data-ttu-id="810c9-119">Para fazer isso, você pode especificar um manipulador de eventos para o evento **Unload** como parte do elemento **Body** , como demonstra o código HTML a seguir:</span><span class="sxs-lookup"><span data-stu-id="810c9-119">To do this, you can specify an event handler for the **unload** event as part of the **BODY** element, as the following HTML code demonstrates:</span></span>


```XML
<BODY onunload = "UnloadMe();">

```



<span data-ttu-id="810c9-120">Em seguida, você pode incluir o código de script em sua função de manipulador de eventos para fechar o arquivo no Player.</span><span class="sxs-lookup"><span data-stu-id="810c9-120">Then you can include script code in your event handler function to close the file in the Player.</span></span> <span data-ttu-id="810c9-121">O código de exemplo a seguir faz isso:</span><span class="sxs-lookup"><span data-stu-id="810c9-121">The following example code does this:</span></span>


```XML
function UnloadMe()
{
   Player.close();
}

```



<span data-ttu-id="810c9-122">Quando o usuário sai do **momento em execução** clicando em um botão para abrir outro recurso do Windows Media Player, como a biblioteca, o Player fecha o navegador inserido.</span><span class="sxs-lookup"><span data-stu-id="810c9-122">When the user switches away from **Now Playing** by clicking a button to open another Windows Media Player feature, such as the library, the Player closes the embedded browser.</span></span> <span data-ttu-id="810c9-123">Isso faz com que o evento **OnUnload** ocorra, executando o script na função chamada **UnloadMe**.</span><span class="sxs-lookup"><span data-stu-id="810c9-123">This causes the **onunload** event to occur, running the script in the function named **UnloadMe**.</span></span> <span data-ttu-id="810c9-124">O método [Player. Close](player-close.md) interrompe a reprodução e descarrega o arquivo de mídia digital atual.</span><span class="sxs-lookup"><span data-stu-id="810c9-124">The [Player.close](player-close.md) method stops playback and unloads the current digital media file.</span></span> <span data-ttu-id="810c9-125">Para exibir o conteúdo novamente, o usuário deve reabrir o arquivo. asx original.</span><span class="sxs-lookup"><span data-stu-id="810c9-125">To view the content again, the user must reopen the original .asx file.</span></span> <span data-ttu-id="810c9-126">Essa técnica também interrompe a reprodução quando o usuário navega para fora da página da Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="810c9-126">This technique also stops playback when the user navigates away from the HTMLView webpage.</span></span> <span data-ttu-id="810c9-127">Observe que essa técnica não pode impedir que o usuário exiba o conteúdo de mídia digital quando ele alterna para o modo de capa.</span><span class="sxs-lookup"><span data-stu-id="810c9-127">Note that this technique cannot prevent the user from viewing the digital media content when he or she switches to skin mode.</span></span>

<span data-ttu-id="810c9-128">Você se lembrará de que o parâmetro HTMLView pode ser aplicado a cada elemento de **entrada** em um arquivo. asx.</span><span class="sxs-lookup"><span data-stu-id="810c9-128">You will recall that the HTMLView parameter can be applied to each **ENTRY** element in an .asx file.</span></span> <span data-ttu-id="810c9-129">Você pode aproveitar esse recurso para garantir que o conteúdo do HTMLView seja exibido toda vez que um novo arquivo de mídia digital for iniciado.</span><span class="sxs-lookup"><span data-stu-id="810c9-129">You can take advantage of this feature to ensure that your HTMLView content is displayed each time a new digital media file starts.</span></span> <span data-ttu-id="810c9-130">Para fazer isso, associe um elemento **param** para HtmlView com cada entrada na sua lista de reprodução. asx.</span><span class="sxs-lookup"><span data-stu-id="810c9-130">To do this, associate a **PARAM** element for HTMLView with each entry in your .asx playlist.</span></span> <span data-ttu-id="810c9-131">Quando cada entrada é reproduzida, o Player retorna para o modo completo e exibe o conteúdo de HTMLView especificado na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="810c9-131">When each entry plays, the Player returns to full mode and displays the HTMLView content you specified in the playlist.</span></span>

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a><span data-ttu-id="810c9-132">Os tipos de comando de script de URL e arquivo estão desabilitados por padrão</span><span class="sxs-lookup"><span data-stu-id="810c9-132">URL and FILE script command types are disabled by default</span></span>

<span data-ttu-id="810c9-133">O Windows Media Player 9 Series ou posterior fornece configurações que permitem que o usuário especifique se os comandos de script de tipo de arquivo e URL podem ser executados.</span><span class="sxs-lookup"><span data-stu-id="810c9-133">Windows Media Player 9 Series or later provides settings that enable the user to specify whether URL and FILE type script commands are able to run.</span></span> <span data-ttu-id="810c9-134">Por padrão, ambos os tipos de comando de script não são executados.</span><span class="sxs-lookup"><span data-stu-id="810c9-134">By default, both of these script command types do not run.</span></span> <span data-ttu-id="810c9-135">Se você usar tipos de comando de script personalizados, eles continuarão a ser executados, independentemente da configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="810c9-135">If you use custom script command types, they will continue to run, regardless of the user setting.</span></span> <span data-ttu-id="810c9-136">Se for necessário usar comandos de script de tipo de URL e de arquivo, você deverá solicitar que o usuário altere as configurações.</span><span class="sxs-lookup"><span data-stu-id="810c9-136">If you must use URL and FILE type script commands, you must prompt the user to change the settings.</span></span> <span data-ttu-id="810c9-137">Para alterar as configurações, clique em **ferramentas**, em **Opções** e em **segurança**.</span><span class="sxs-lookup"><span data-stu-id="810c9-137">To change the settings, click **Tools**, then **Options**, and then **Security**.</span></span>

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a><span data-ttu-id="810c9-138">A reabertura de um HTMLView não recarrega a página da Web</span><span class="sxs-lookup"><span data-stu-id="810c9-138">Reopening an HTMLView does not reload the webpage</span></span>

<span data-ttu-id="810c9-139">Quando o usuário abre um arquivo. asx que inclui um parâmetro HTMLView e, subsequentemente, reabre o mesmo arquivo, o Windows Media Player não atualiza a página da Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="810c9-139">When the user opens an .asx file that includes an HTMLView parameter and subsequently reopens the same file, Windows Media Player does not refresh the HTMLView webpage.</span></span> <span data-ttu-id="810c9-140">Isso também significa que, se você tiver permitido que os usuários naveguem para longe da página da Web do HTMLView, o Player não retornará o navegador incorporado para a página da Web HTMLView inicial.</span><span class="sxs-lookup"><span data-stu-id="810c9-140">This also means that if you have allowed users to navigate away from your HTMLView webpage, the Player does not return the embedded browser to the initial HTMLView webpage.</span></span>

## <a name="hiding-the-content-location"></a><span data-ttu-id="810c9-141">Ocultando o local do conteúdo</span><span class="sxs-lookup"><span data-stu-id="810c9-141">Hiding the content location</span></span>

<span data-ttu-id="810c9-142">Você pode decidir que não quer que o Windows Media Player exiba o local do seu conteúdo de mídia digital enquanto ele está reproduzindo um arquivo. asx.</span><span class="sxs-lookup"><span data-stu-id="810c9-142">You might decide that you don't want Windows Media Player to display the location of your digital media content while it is playing an .asx file.</span></span> <span data-ttu-id="810c9-143">Normalmente, o Windows Media Player mostra apenas informações sobre a própria lista de reprodução ao transmitir conteúdo da Internet.</span><span class="sxs-lookup"><span data-stu-id="810c9-143">Usually, Windows Media Player only shows information about the playlist itself when streaming content from the Internet.</span></span> <span data-ttu-id="810c9-144">No entanto, há outras etapas que você pode executar para impedir que os usuários determinem o local do seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="810c9-144">However, there are further steps you can take to prevent users from determining the location of your content.</span></span> <span data-ttu-id="810c9-145">Por exemplo, uma maneira de garantir que o Player não exiba o caminho para seu conteúdo é transmitir seu conteúdo usando as listas de reprodução do lado do servidor dos serviços de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="810c9-145">For example, one way to ensure that the Player does not display the path to your content is to stream your content using Windows Media Services server-side playlists.</span></span> <span data-ttu-id="810c9-146">Dessa forma, quando o usuário exibir as propriedades do conteúdo, ele verá a URL do servidor e não a URL do seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="810c9-146">That way, when the user views the properties for the content, he or she sees the URL of the server and not the URL of your content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="810c9-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="810c9-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="810c9-148">**Exibindo páginas da Web no Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="810c9-148">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="810c9-149">**Elemento PARAM**</span><span class="sxs-lookup"><span data-stu-id="810c9-149">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




