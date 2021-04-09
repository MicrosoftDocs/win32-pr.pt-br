---
title: Uma lista de reprodução avançada
description: Uma lista de reprodução avançada
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
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
- Playlists do metarquivo do Windows Media, exemplo de playlist avançada
- listas de reprodução, exemplo de playlist avançada
- playlists de metarquivo, exemplo de playlist avançada
- Exemplos do Windows Media Player, playlist
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, exemplo de playlist avançada
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
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005308"
---
# <a name="an-advanced-playlist"></a><span data-ttu-id="d65e4-125">Uma lista de reprodução avançada</span><span class="sxs-lookup"><span data-stu-id="d65e4-125">An Advanced Playlist</span></span>

<span data-ttu-id="d65e4-126">O exemplo de playlist a seguir mostra como usar um conjunto mais completo de elementos de playlist.</span><span class="sxs-lookup"><span data-stu-id="d65e4-126">The following playlist example shows how to use a more complete set of playlist elements.</span></span> <span data-ttu-id="d65e4-127">Ao escrever seu próprio código, você precisará alterar todas as URLs e nomes de arquivos para nomes de arquivos válidos que sejam acessíveis ao seu Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d65e4-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="d65e4-128">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="d65e4-128">Example Code</span></span>


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="d65e4-129">A tabela a seguir descreve a lista de reprodução avançada anterior.</span><span class="sxs-lookup"><span data-stu-id="d65e4-129">The following table describes the preceding advanced playlist.</span></span>



| <span data-ttu-id="d65e4-130">Linha</span><span class="sxs-lookup"><span data-stu-id="d65e4-130">Line</span></span>                                                                                            | <span data-ttu-id="d65e4-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="d65e4-131">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | <span data-ttu-id="d65e4-132">O elemento [ASX](asx-element.md) identifica o cliente do (Windows Media Player) que esta é uma lista de reprodução do metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d65e4-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="d65e4-133">O atributo **version** especifica o número de versão dos elementos de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="d65e4-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | <span data-ttu-id="d65e4-134">O elemento [title](title-element--metafile.md) identifica o título da lista de reprodução como um todo.</span><span class="sxs-lookup"><span data-stu-id="d65e4-134">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="d65e4-135">O Windows Media Player exibe esses metadados como o título de exibição.</span><span class="sxs-lookup"><span data-stu-id="d65e4-135">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | <span data-ttu-id="d65e4-136">O elemento [abstract](abstract-element.md) fornece a dica de ferramenta para o título show.</span><span class="sxs-lookup"><span data-stu-id="d65e4-136">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the show title.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | <span data-ttu-id="d65e4-137">O elemento [moreinfo](moreinfo-element.md) vincula o título de mostrar a uma URL.</span><span class="sxs-lookup"><span data-stu-id="d65e4-137">The [MOREINFO](moreinfo-element.md) element links the show title to an URL.</span></span> <span data-ttu-id="d65e4-138">Pausar o ponteiro do mouse sobre o título mostrar acessa a dica de ferramenta, se definido.</span><span class="sxs-lookup"><span data-stu-id="d65e4-138">Pausing the mouse pointer over the show title accesses the ToolTip, if defined.</span></span> <span data-ttu-id="d65e4-139">Selecionar o título mostrar irá abrir a URL designada.</span><span class="sxs-lookup"><span data-stu-id="d65e4-139">Selecting the show title will then open the designated URL.</span></span>                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | <span data-ttu-id="d65e4-140">O elemento [banner](banner-element.md) cria uma faixa de anúncio no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d65e4-140">The [BANNER](banner-element.md) element creates an advertising banner in Windows Media Player.</span></span> <span data-ttu-id="d65e4-141">O atributo **href** especifica o gráfico de faixa (que deve ter de 194 pixels de largura por 32 pixels de altura).</span><span class="sxs-lookup"><span data-stu-id="d65e4-141">The **HREF** attribute specifies the banner graphic (which must be 194 pixels wide by 32 pixels tall).</span></span>                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | <span data-ttu-id="d65e4-142">O elemento [abstract](abstract-element.md) fornece a dica de ferramenta para a **faixa**.</span><span class="sxs-lookup"><span data-stu-id="d65e4-142">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the **BANNER**.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | <span data-ttu-id="d65e4-143">O elemento [moreinfo](moreinfo-element.md) vincula o gráfico de **faixa** a uma URL.</span><span class="sxs-lookup"><span data-stu-id="d65e4-143">The [MOREINFO](moreinfo-element.md) element links the **BANNER** graphic to a URL.</span></span> <span data-ttu-id="d65e4-144">Manter o ponteiro do mouse sobre a **faixa** acessa uma dica de ferramenta, se definido.</span><span class="sxs-lookup"><span data-stu-id="d65e4-144">Holding the mouse pointer over the **BANNER** accesses a ToolTip, if defined.</span></span> <span data-ttu-id="d65e4-145">A seleção da **faixa** abrirá a URL designada.</span><span class="sxs-lookup"><span data-stu-id="d65e4-145">Selecting the **BANNER** will open the designated URL.</span></span>                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | <span data-ttu-id="d65e4-146">O elemento [param](param-element.md) define um parâmetro personalizado.</span><span class="sxs-lookup"><span data-stu-id="d65e4-146">The [PARAM](param-element.md) element defines a custom parameter.</span></span> <span data-ttu-id="d65e4-147">O atributo **Name** define o nome do parâmetro personalizado como "Track".</span><span class="sxs-lookup"><span data-stu-id="d65e4-147">The **name** attribute defines the name of the custom parameter as "track".</span></span> <span data-ttu-id="d65e4-148">O atributo **Value** define o valor de "Track" como "1".</span><span class="sxs-lookup"><span data-stu-id="d65e4-148">The **value** attribute defines the value of "track" to be "1".</span></span>                                                                                                                          |
| `</BANNER>`                                                                                 | <span data-ttu-id="d65e4-149">Fecha o elemento de **faixa**</span><span class="sxs-lookup"><span data-stu-id="d65e4-149">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | <span data-ttu-id="d65e4-150">Inicia o bloco do elemento de [entrada](entry-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d65e4-150">Begins the [ENTRY](entry-element.md) element block.</span></span> <span data-ttu-id="d65e4-151">Esse elemento define um clipe em uma lista de reprodução especificando um link no elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="d65e4-151">This element defines a clip in a playlist by specifying a link in the **REF** element.</span></span> <span data-ttu-id="d65e4-152">Definir **ClientSkip** como "não" significa que o usuário não pode avançar ou ir para o próximo clipe</span><span class="sxs-lookup"><span data-stu-id="d65e4-152">Setting **ClientSkip** to "no" means that the user cannot fast forward or jump to the next clip</span></span>                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | <span data-ttu-id="d65e4-153">Cria uma faixa de anúncio.</span><span class="sxs-lookup"><span data-stu-id="d65e4-153">Creates an advertising banner.</span></span> <span data-ttu-id="d65e4-154">O **href** é o gráfico de faixa (194x32 pixels).</span><span class="sxs-lookup"><span data-stu-id="d65e4-154">The **HREF** is the banner graphic (194x32 pixels).</span></span>                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | <span data-ttu-id="d65e4-155">Fornece a dica de ferramenta para a faixa.</span><span class="sxs-lookup"><span data-stu-id="d65e4-155">Provides the ToolTip for the banner.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="d65e4-156">Fornece um link para a URL da faixa.</span><span class="sxs-lookup"><span data-stu-id="d65e4-156">Provides a link to the URL for the banner.</span></span> <span data-ttu-id="d65e4-157">A seleção da faixa se conecta à URL.</span><span class="sxs-lookup"><span data-stu-id="d65e4-157">Selecting the banner connects to the URL.</span></span>                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | <span data-ttu-id="d65e4-158">Fecha o elemento de **faixa**</span><span class="sxs-lookup"><span data-stu-id="d65e4-158">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="d65e4-159">Fornece um link para a URL do texto do **título** do clipe.</span><span class="sxs-lookup"><span data-stu-id="d65e4-159">Provides a link to the URL for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | <span data-ttu-id="d65e4-160">Um comentário.</span><span class="sxs-lookup"><span data-stu-id="d65e4-160">A comment.</span></span> <span data-ttu-id="d65e4-161">Os [comentários](comments.md) só estarão visíveis quando o código for exibido.</span><span class="sxs-lookup"><span data-stu-id="d65e4-161">[Comments](comments.md) are only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | <span data-ttu-id="d65e4-162">Fornece a dica de ferramenta para o texto do **título** do clipe.</span><span class="sxs-lookup"><span data-stu-id="d65e4-162">Provides the ToolTip for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | <span data-ttu-id="d65e4-163">Identifica o título do clipe.</span><span class="sxs-lookup"><span data-stu-id="d65e4-163">Identifies the title of the clip.</span></span> <span data-ttu-id="d65e4-164">É o **título** do clipe porque ele está aninhado dentro de um elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="d65e4-164">It is the clip **TITLE** because it is nested within an **ENTRY** element.</span></span> <span data-ttu-id="d65e4-165">O Windows Media Player exibe esses metadados como o título do clipe.</span><span class="sxs-lookup"><span data-stu-id="d65e4-165">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | <span data-ttu-id="d65e4-166">Identifica o autor do clipe de mídia.</span><span class="sxs-lookup"><span data-stu-id="d65e4-166">Identifies the author of the media clip.</span></span> <span data-ttu-id="d65e4-167">Esses metadados são exibidos como o **autor** do clipe pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d65e4-167">This metadata is displayed as the clip **AUTHOR** by Windows Media Player.</span></span>                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | <span data-ttu-id="d65e4-168">O elemento de [direitos autorais](copyright-element.md) especifica os direitos autorais associados ao clipe de mídia.</span><span class="sxs-lookup"><span data-stu-id="d65e4-168">The [COPYRIGHT](copyright-element.md) element specifies the copyrights associated with the media clip.</span></span> <span data-ttu-id="d65e4-169">O Windows Media Player exibe esses metadados como o clipe COPYRIGHT.</span><span class="sxs-lookup"><span data-stu-id="d65e4-169">Windows Media Player displays this metadata as the clip COPYRIGHT.</span></span>                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="d65e4-170">Um comentário, no mesmo formato que comentários **XML** .</span><span class="sxs-lookup"><span data-stu-id="d65e4-170">A comment, in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | <span data-ttu-id="d65e4-171">URL para o conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d65e4-171">URL for the media content.</span></span> <span data-ttu-id="d65e4-172">O elemento [ref](ref-element.md) identifica a linha como um ponteiro para conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d65e4-172">The [REF](ref-element.md) element identifies the line as a pointer to media content.</span></span> <span data-ttu-id="d65e4-173">O atributo **href** é a URL para o arquivo. Observe o uso do fechamento do tipo XML do elemento "/>" em vez de " &lt; /ref &gt; ".</span><span class="sxs-lookup"><span data-stu-id="d65e4-173">The **HREF** attribute is the URL to the file.Note the use of the XML-like closing of the element , "/>" instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="d65e4-174">Como esse elemento não tem elementos filho, ele se fecha.</span><span class="sxs-lookup"><span data-stu-id="d65e4-174">Because this element does not have child elements, it closes itself.</span></span><br/> |
| `</ENTRY>`                                                                                  | <span data-ttu-id="d65e4-175">Especifica o final do primeiro elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="d65e4-175">Specifies the end of the of the first **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | <span data-ttu-id="d65e4-176">Inicia o segundo elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="d65e4-176">Begins the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | <span data-ttu-id="d65e4-177">Identifica o título do segundo clipe.</span><span class="sxs-lookup"><span data-stu-id="d65e4-177">Identifies the title of the second clip.</span></span>                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | <span data-ttu-id="d65e4-178">Identifica o autor do segundo clipe de mídia.</span><span class="sxs-lookup"><span data-stu-id="d65e4-178">Identifies the author of the second media clip.</span></span>                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | <span data-ttu-id="d65e4-179">Um comentário.</span><span class="sxs-lookup"><span data-stu-id="d65e4-179">A comment.</span></span> <span data-ttu-id="d65e4-180">Ele só ficará visível quando o código for exibido.</span><span class="sxs-lookup"><span data-stu-id="d65e4-180">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | <span data-ttu-id="d65e4-181">Este é o texto de dica de ferramenta para o texto do **título** do clipe.</span><span class="sxs-lookup"><span data-stu-id="d65e4-181">This is the ToolTip text for the **TITLE** text of the clip.</span></span>                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="d65e4-182">Um comentário.</span><span class="sxs-lookup"><span data-stu-id="d65e4-182">A comment.</span></span> <span data-ttu-id="d65e4-183">Ele só ficará visível quando o código for exibido.</span><span class="sxs-lookup"><span data-stu-id="d65e4-183">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | <span data-ttu-id="d65e4-184">Identifica a linha como um ponteiro para conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d65e4-184">Identifies the line as a pointer to media content.</span></span> <span data-ttu-id="d65e4-185">O atributo **href** é a URL para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d65e4-185">The **HREF** attribute is the URL to the file.</span></span>                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | <span data-ttu-id="d65e4-186">Especifica o final do segundo elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="d65e4-186">Specifies the end of the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | <span data-ttu-id="d65e4-187">Especifica o fim da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="d65e4-187">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="d65e4-188">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d65e4-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d65e4-189">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="d65e4-189">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="d65e4-190">**Exemplos de playlist**</span><span class="sxs-lookup"><span data-stu-id="d65e4-190">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="d65e4-191">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="d65e4-191">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="d65e4-192">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d65e4-192">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d65e4-193">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d65e4-193">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





