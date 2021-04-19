---
title: Uma lista de reprodução básica
description: Uma lista de reprodução básica
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
keywords:
- Listas de reprodução do metarquivo do Windows Media, exemplos de playlist
- listas de reprodução, exemplos de playlist
- listas de reprodução de metarquivo, exemplos de playlist
- Playlists do metarquivo do Windows Media, listas de reprodução de exemplo
- listas de reprodução, exemplos de listas de reprodução
- listas de reprodução de metarquivo, listas de reprodução de exemplo
- Playlists do metarquivo do Windows Media, listas de reprodução de exemplo
- listas de reprodução, listas de reprodução de exemplo
- listas de reprodução de metarquivo, listas de reprodução de exemplo
- Playlists do metarquivo do Windows Media, exemplo de código
- listas de reprodução, exemplo de código
- listas de reprodução de metarquivo, exemplo de código
- Playlists do metarquivo do Windows Media, exemplo de playlist básica
- listas de reprodução, exemplo de playlist básica
- listas de reprodução de metarquivo, exemplo de playlist básica
- Exemplos do Windows Media Player, playlist
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, exemplo de playlist básica
- exemplos de playlist
- exemplos de playlist
- listas de reprodução de exemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 804bc69c9ab3b243030cd2c87545e6362ccfca79
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314779"
---
# <a name="a-basic-playlist"></a><span data-ttu-id="f9618-125">Uma lista de reprodução básica</span><span class="sxs-lookup"><span data-stu-id="f9618-125">A Basic Playlist</span></span>

<span data-ttu-id="f9618-126">O exemplo de playlist a seguir mostra um conjunto básico de elementos da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f9618-126">The following playlist example shows a basic set of playlist elements.</span></span> <span data-ttu-id="f9618-127">Ao escrever seu próprio código, você precisará alterar todas as URLs e nomes de arquivos para nomes de arquivos válidos que sejam acessíveis ao seu Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f9618-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="f9618-128">**Exemplo de código**</span><span class="sxs-lookup"><span data-stu-id="f9618-128">**Code Example**</span></span>


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="f9618-129">A tabela a seguir fornece detalhes sobre o uso de cada elemento no código de exemplo.</span><span class="sxs-lookup"><span data-stu-id="f9618-129">The following table provides details on the use of each element in the example code.</span></span>



| <span data-ttu-id="f9618-130">Linha</span><span class="sxs-lookup"><span data-stu-id="f9618-130">Line</span></span>                                                                                            | <span data-ttu-id="f9618-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9618-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | <span data-ttu-id="f9618-132">O elemento [ASX](asx-element.md) identifica o cliente do (Windows Media Player) que esta é uma lista de reprodução do metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f9618-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="f9618-133">O atributo **version** especifica o número de versão dos elementos de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="f9618-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f9618-134">\<TITLE>Demonstração de playlist básica\</TITLE></span><span class="sxs-lookup"><span data-stu-id="f9618-134">\<TITLE>Basic Playlist Demo\</TITLE></span></span>                                                  | <span data-ttu-id="f9618-135">O elemento [title](title-element--metafile.md) identifica o título da lista de reprodução como um todo.</span><span class="sxs-lookup"><span data-stu-id="f9618-135">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="f9618-136">O Windows Media Player exibe esses metadados como o título de exibição.</span><span class="sxs-lookup"><span data-stu-id="f9618-136">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | <span data-ttu-id="f9618-137">Inicia o elemento de [entrada](entry-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f9618-137">Begins the [ENTRY](entry-element.md) element.</span></span> <span data-ttu-id="f9618-138">Um elemento de **entrada** é uma maneira de definir um clipe específico em uma lista de reprodução</span><span class="sxs-lookup"><span data-stu-id="f9618-138">An **ENTRY** element is a way to define a particular clip in a playlist</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f9618-139">\<TITLE>Uma entrada em uma playlist básica\</TITLE></span><span class="sxs-lookup"><span data-stu-id="f9618-139">\<TITLE>An Entry in a basic playlist\</TITLE></span></span>                                         | <span data-ttu-id="f9618-140">Identifica o título do clipe da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f9618-140">Identifies the title of the playlist clip .</span></span> <span data-ttu-id="f9618-141">Ele é diferente do elemento **title** anterior porque este é aninhado dentro de um elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="f9618-141">It is different than the previous **TITLE** element because this one is nested within an **ENTRY** element.</span></span> <span data-ttu-id="f9618-142">O Windows Media Player exibe esses metadados como o título do clipe.</span><span class="sxs-lookup"><span data-stu-id="f9618-142">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f9618-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span><span class="sxs-lookup"><span data-stu-id="f9618-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span></span>                                              | <span data-ttu-id="f9618-144">O elemento [autor](author-element.md) identifica o autor do clipe de mídia.</span><span class="sxs-lookup"><span data-stu-id="f9618-144">The [AUTHOR](author-element.md) element identifies the author of the media clip .</span></span> <span data-ttu-id="f9618-145">O Windows Media Player exibe esses metadados como o **autor** do clipe.</span><span class="sxs-lookup"><span data-stu-id="f9618-145">Windows Media Player displays this metadata as the clip **AUTHOR**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | <span data-ttu-id="f9618-146">Um comentário.</span><span class="sxs-lookup"><span data-stu-id="f9618-146">A comment.</span></span> <span data-ttu-id="f9618-147">Os [comentários](comments.md) são visíveis somente quando o código é exibido e estão no mesmo formato que os comentários **XML** .</span><span class="sxs-lookup"><span data-stu-id="f9618-147">[Comments](comments.md) are visible only when the code is viewed, and are in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | <span data-ttu-id="f9618-148">Ponteiro real para o arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f9618-148">Actual pointer to the media file.</span></span> <span data-ttu-id="f9618-149">O elemento [ref](ref-element.md) identifica a linha como um ponteiro para conteúdo de mídia, enquanto o atributo **href** é a URL para o arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f9618-149">The [REF](ref-element.md) element identifies the line as a pointer to media content, while the **HREF** attribute is the URL to the media file.</span></span> <span data-ttu-id="f9618-150">Nesse caso, a URL usa o protocolo MMS e, portanto, aponta para um Windows Media Server. Os arquivos de mídia no servidor de mídia geralmente não são mantidos no mesmo local que os documentos HTML.</span><span class="sxs-lookup"><span data-stu-id="f9618-150">In this case, the URL uses the MMS protocol, so it points to a Windows Media server.Media files on your media server are not usually kept in the same location as your HTML documents.</span></span><br/> <span data-ttu-id="f9618-151">Observe o uso do fechamento do tipo XML do elemento, "/>", em vez de " &lt; /ref &gt; ".</span><span class="sxs-lookup"><span data-stu-id="f9618-151">Note the use of the XML-like closing of the element , "/>", instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="f9618-152">Como esse elemento não tem elementos filho, ele se fecha.</span><span class="sxs-lookup"><span data-stu-id="f9618-152">Because this element does not have child elements, it closes itself.</span></span><br/> |
| \</ENTRY>                                                                                  | <span data-ttu-id="f9618-153">Especifica o final do elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="f9618-153">Specifies the end of the **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | <span data-ttu-id="f9618-154">Especifica o fim da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f9618-154">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="f9618-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9618-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9618-156">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="f9618-156">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f9618-157">**Exemplos de playlist**</span><span class="sxs-lookup"><span data-stu-id="f9618-157">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="f9618-158">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="f9618-158">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f9618-159">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f9618-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f9618-160">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f9618-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





