---
title: Formato de área de transferência HTML
description: Esta seção discute o formato de área de transferência HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Interface do usuário do Windows, área de transferência
- área de transferência, recortando dados
- área de transferência, copiando dados
- área de transferência, colando dados
- área de transferência, formatos
- área de transferência, formato HTML
- área de transferência, cortando texto em HTML
- área de transferência, colando texto HTML
- Formato de área de transferência CF_HTML
- área de transferência, formato de CF_HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005691"
---
# <a name="html-clipboard-format"></a><span data-ttu-id="05589-113">Formato de área de transferência HTML</span><span class="sxs-lookup"><span data-stu-id="05589-113">HTML Clipboard Format</span></span>

<span data-ttu-id="05589-114">Os requisitos para transferir texto HTML por meio da área de transferência diferem de acordo com o cenário.</span><span class="sxs-lookup"><span data-stu-id="05589-114">The requirements for transferring HTML text by means of the clipboard differ depending on scenario.</span></span> <span data-ttu-id="05589-115">Este artigo se preocupa com a recorte e colagem de fragmentos de um documento HTML.</span><span class="sxs-lookup"><span data-stu-id="05589-115">This article is concerned with cutting and pasting fragments of an HTML document.</span></span> <span data-ttu-id="05589-116">Pode haver requisitos para transferir documentos HTML inteiros por meio da área de transferência; no entanto, este artigo é orientado por um requisito para transferir fragmentos de texto HTML selecionado.</span><span class="sxs-lookup"><span data-stu-id="05589-116">There may be requirements for transferring entire HTML documents through the clipboard; however, this article is driven by a requirement to transfer fragments of selected HTML text.</span></span> <span data-ttu-id="05589-117">Dessa forma, um método que exigia que todo o documento HTML fosse copiado para a área de transferência é visto como muito pesado.</span><span class="sxs-lookup"><span data-stu-id="05589-117">As such, a method that required the entire HTML document to be copied to the clipboard is seen as too heavyweight.</span></span>

<span data-ttu-id="05589-118">O \_ formato de área de transferência HTML do CF permite que um fragmento de texto HTML bruto e seu contexto sejam armazenados na área de transferência como ASCII.</span><span class="sxs-lookup"><span data-stu-id="05589-118">The CF\_HTML clipboard format allows a fragment of raw HTML text and its context to be stored on the clipboard as ASCII.</span></span> <span data-ttu-id="05589-119">Isso permite que o contexto do fragmento HTML, que consiste em todas as marcas adjacentes anteriores, seja examinado por um aplicativo para que as marcas ao redor do fragmento HTML possam ser observadas com seus atributos.</span><span class="sxs-lookup"><span data-stu-id="05589-119">This allows the context of the HTML fragment, which consists of all preceding surrounding tags, to be examined by an application so that the surrounding tags of the HTML fragment can be noted with their attributes.</span></span> <span data-ttu-id="05589-120">Embora seja preciso que os aplicativos decidam como interpretar esses fragmentos, algumas diretrizes básicas são incluídas aqui com base nas implementações de IE4/MSHTML.</span><span class="sxs-lookup"><span data-stu-id="05589-120">Although it is up to applications to decide how to interpret such fragments, some basic guidelines are included here based on IE4/MSHTML implementations.</span></span>

<span data-ttu-id="05589-121">O nome oficial da área de transferência (a cadeia de caracteres usada por RegisterClipboardFormat) é o formato HTML.</span><span class="sxs-lookup"><span data-stu-id="05589-121">The official name of the clipboard (the string used by RegisterClipboardFormat) is HTML Format.</span></span>

-   [<span data-ttu-id="05589-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="05589-122">Description</span></span>](#description)
-   [<span data-ttu-id="05589-123">Cenários</span><span class="sxs-lookup"><span data-stu-id="05589-123">Scenarios</span></span>](#scenarios)

## <a name="description"></a><span data-ttu-id="05589-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="05589-124">Description</span></span>

<span data-ttu-id="05589-125">\_O HTML do CF é totalmente um formato de texto (para ser, entre outras coisas, no espírito HTML, e usa UTF-8) e inclui um `description` , um opcional `context` e, dentro do contexto, o `fragment` .</span><span class="sxs-lookup"><span data-stu-id="05589-125">CF\_HTML is entirely text format (to be, among other things, in the HTML spirit, and uses UTF-8) and includes a `description`, an optional `context`, and, within the context, the `fragment`.</span></span>

<span data-ttu-id="05589-126">Veja a seguir um exemplo de uma área de transferência:</span><span class="sxs-lookup"><span data-stu-id="05589-126">The following is an example of a clipboard:</span></span>


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



<span data-ttu-id="05589-127">A descrição inclui o número de versão da área de transferência e os deslocamentos, indicando onde o contexto e o início e término do fragmento.</span><span class="sxs-lookup"><span data-stu-id="05589-127">The description includes the clipboard version number and offsets, indicating where the context and the fragment start and end.</span></span> <span data-ttu-id="05589-128">A descrição é uma lista de palavras-chave de texto ASCII (min/Maj não é significativa) seguida por uma cadeia de caracteres e separados por dois-pontos (:).</span><span class="sxs-lookup"><span data-stu-id="05589-128">The description is a list of ASCII text keywords (min/maj is not meaningful) followed by a string and separated by a colon (:).</span></span>

<span data-ttu-id="05589-129">**Versão**: VV número de versão da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="05589-129">**Version**: vv version number of the clipboard.</span></span> <span data-ttu-id="05589-130">A versão inicial é 0,9.</span><span class="sxs-lookup"><span data-stu-id="05589-130">Starting version is 0.9.</span></span>

<span data-ttu-id="05589-131">**StartHTML**: byteCount desde o início da área de transferência até o início do contexto, ou-1 se nenhum contexto.</span><span class="sxs-lookup"><span data-stu-id="05589-131">**StartHTML**: bytecount from the beginning of the clipboard to the start of the context, or -1 if no context.</span></span>

<span data-ttu-id="05589-132">**Endhtml**: byteCount desde o início da área de transferência até o final do contexto, ou-1, se não houver nenhum contexto.</span><span class="sxs-lookup"><span data-stu-id="05589-132">**EndHTML**: bytecount from the beginning of the clipboard to the end of the context, or -1 if no context.</span></span>

<span data-ttu-id="05589-133">**StartFragment**: byteCount desde o início da área de transferência até o início do fragmento.</span><span class="sxs-lookup"><span data-stu-id="05589-133">**StartFragment**: bytecount from the beginning of the clipboard to the start of the fragment.</span></span>

<span data-ttu-id="05589-134">**EndFragment**: byteCount desde o início da área de transferência até o fim do fragmento.</span><span class="sxs-lookup"><span data-stu-id="05589-134">**EndFragment**: bytecount from the beginning of the clipboard to the end of the fragment.</span></span>

<span data-ttu-id="05589-135">**StartSelection**: byteCount desde o início da área de transferência até o início da seleção.</span><span class="sxs-lookup"><span data-stu-id="05589-135">**StartSelection**: bytecount from the beginning of the clipboard to the start of the selection.</span></span>

<span data-ttu-id="05589-136">**Endselecting**: byteCount desde o início da área de transferência até o fim da seleção.</span><span class="sxs-lookup"><span data-stu-id="05589-136">**EndSelection**: bytecount from the beginning of the clipboard to the end of the selection.</span></span>

<span data-ttu-id="05589-137">As palavras-chave StartSelection e endseleções são opcionais e devem ser omitidas se você não quiser que o aplicativo gere essas informações.</span><span class="sxs-lookup"><span data-stu-id="05589-137">The StartSelection and EndSelection keywords are optional and must both be omitted if you do not want the application to generate this information.</span></span>

<span data-ttu-id="05589-138">Outras informações desse tipo podem ser adicionadas aqui mais tarde, pois o HTML começa no StartHTMLoffset.</span><span class="sxs-lookup"><span data-stu-id="05589-138">Other information of this kind could be added here later, since the HTML starts at the StartHTMLoffset.</span></span> <span data-ttu-id="05589-139">Por exemplo, vários pares de StartFragment/endfrager podem ser adicionados posteriormente para dar suporte à seleção não contígua de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="05589-139">For example, multiple pairs of StartFragment / EndFragment could be added later to support noncontiguous selection of fragments.</span></span>

<span data-ttu-id="05589-140">Para a conveniência dos programas que geram os bytecounts, os bytecounts podem ser preenchidos por zeros.</span><span class="sxs-lookup"><span data-stu-id="05589-140">For the convenience of the programs generating the bytecounts, bytecounts could be left padded by zeros.</span></span> <span data-ttu-id="05589-141">Por exemplo, os programas que geram os bytecounts poderiam afetar arbitrariamente dez (10) zeros para cada palavra-chave (StartHTML: 0000000000) e, em seguida, quando o StartHTML byteCount exato é conhecido (digamos, 71), o programa pode substituir o número apropriado de zeros pelo byteCount (StartHTML: 0000000071).</span><span class="sxs-lookup"><span data-stu-id="05589-141">For example, programs generating the bytecounts could arbitrarily affect ten (10) zeros to each keyword (StartHTML: 0000000000) and then, when the exact StartHTML bytecount is known (say, 71), the program can replace the appropriate number of zeros by the bytecount (StartHTML: 0000000071).</span></span>

<span data-ttu-id="05589-142">O único conjunto de caracteres com suporte na área de transferência é Unicode em sua codificação UTF-8.</span><span class="sxs-lookup"><span data-stu-id="05589-142">The only character set supported by the clipboard is Unicode in its UTF-8 encoding.</span></span> <span data-ttu-id="05589-143">Como os primeiros caracteres de UTF-8 e ASCII correspondem, a descrição é sempre ASCII, mas os bytes do contexto (começando em StartHTML) podem estar usando outros caracteres codificados em UTF-8.</span><span class="sxs-lookup"><span data-stu-id="05589-143">Because the first characters of UTF-8 and ASCII match, the description is always ASCII, but the bytes of the context (starting at StartHTML) could be using any other characters coded in UTF-8.</span></span>

<span data-ttu-id="05589-144">O fim das linhas no cabeçalho de formato da área de transferência pode ser CR ou CR/LF ou LF.</span><span class="sxs-lookup"><span data-stu-id="05589-144">End of lines in the clipboard format header could be CR or CR/LF or LF.</span></span>

<span data-ttu-id="05589-145">O fragmento contém HTML puro e válido representando a área que o usuário selecionou (para copiar, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="05589-145">The fragment contains pure, valid HTML representing the area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="05589-146">Ele contém o texto selecionado, além das marcas de abertura e os atributos de qualquer elemento que tenha uma marca de fim dentro do texto selecionado e marcas de fim no final do fragmento para qualquer marca de início incluída.</span><span class="sxs-lookup"><span data-stu-id="05589-146">This contains the selected text plus the opening tags and attributes of any element that has an end tag within the selected text, and end tags at the end of the fragment for any start tag included.</span></span> <span data-ttu-id="05589-147">Todas as informações são necessárias para a colagem básica de um fragmento HTML.</span><span class="sxs-lookup"><span data-stu-id="05589-147">This is all information required for basic pasting of an HTML fragment.</span></span>

<span data-ttu-id="05589-148">O fragmento deve ser precedido e seguido pelos comentários HTML</span><span class="sxs-lookup"><span data-stu-id="05589-148">The fragment should be preceded and followed by the HTML comments</span></span> <!--StartFragment--> <span data-ttu-id="05589-149">e</span><span class="sxs-lookup"><span data-stu-id="05589-149">and</span></span> <!--EndFragment--> <span data-ttu-id="05589-150">(nenhum espaço é permitido entre o!--e o texto) para indicar convenientemente onde o fragmento começa e termina.</span><span class="sxs-lookup"><span data-stu-id="05589-150">(no space allowed between the !-- and the text) to conveniently indicate where the fragment starts and ends.</span></span> <span data-ttu-id="05589-151">Portanto, o início e o fim do fragmento são indicados pela presença desses comentários e por contagens de bytes StartFragment e endfrag na descrição.</span><span class="sxs-lookup"><span data-stu-id="05589-151">Thus the start and end of the fragment are indicated by the presence of these comments and by StartFragment and EndFragment byte counts in the description.</span></span> <span data-ttu-id="05589-152">As ferramentas devem produzir essas informações.</span><span class="sxs-lookup"><span data-stu-id="05589-152">Tools are expected to produce this information.</span></span> <span data-ttu-id="05589-153">Essa redundância foi introduzida para conseguir encontrar rapidamente o início do fragmento (da contagem de bytes) e marcar a posição do fragmento diretamente na árvore HTML.</span><span class="sxs-lookup"><span data-stu-id="05589-153">This redundancy has been introduced to be able to rapidly find the start of the fragment (from the byte count) and mark the position of the fragment directly in the HTML tree.</span></span>

<span data-ttu-id="05589-154">A seleção indica dentro do fragmento a área HTML exata que o usuário selecionou (para copiar, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="05589-154">The selection indicates inside the fragment the exact HTML area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="05589-155">Isso adiciona mais informações ao fragmento indicando o texto exato selecionado, sem as marcas de abertura e marcas de fim que foram adicionadas para garantir que o fragmento seja um HTML bem formado.</span><span class="sxs-lookup"><span data-stu-id="05589-155">This adds more information to the fragment by indicating the exact selected text, without the opening tags and end tags that have been added to ensure the fragment is well-formed HTML.</span></span>

<span data-ttu-id="05589-156">A seleção é opcional, já que informações suficientes são incluídas no fragmento para a colagem básica.</span><span class="sxs-lookup"><span data-stu-id="05589-156">The selection is optional, as sufficient information is included in the fragment for basic pasting.</span></span> <span data-ttu-id="05589-157">Se a seleção não for armazenada, StartSelection e EndSelect não serão armazenadas no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="05589-157">If the selection is not stored, both StartSelection and EndSelection are not stored in the header.</span></span>

<span data-ttu-id="05589-158">O contexto é um documento HTML válido e completo.</span><span class="sxs-lookup"><span data-stu-id="05589-158">The context is a valid, complete HTML document.</span></span> <span data-ttu-id="05589-159">Este artigo contém o fragmento e todas as marcas adjacentes anteriores (marcas de início e de término; elas antes das marcas ao redor representam todos os nós pai do fragmento, até o nó HTML).</span><span class="sxs-lookup"><span data-stu-id="05589-159">This article contains the fragment and all preceding surrounding tags (start and end tags; these preceding surrounding tags represent all the parent nodes of the fragment, until the HTML node).</span></span> <span data-ttu-id="05589-160">O artigo também contém o cabeçalho completo e permite que os elementos BASE e título, por exemplo, sejam incluídos para que essas informações adicionais possam ser obtidas.</span><span class="sxs-lookup"><span data-stu-id="05589-160">The article also contains the complete HEAD, and allows the BASE and TITLE elements, for example, to be included so this additional information can be obtained.</span></span> <span data-ttu-id="05589-161">Um aplicativo que copia um fragmento de HTML para a área de transferência pode optar por criar um elemento BASE para incluir no contexto se esse elemento ainda não estiver presente, de modo que as URLs parciais no fragmento possam ser resolvidas.</span><span class="sxs-lookup"><span data-stu-id="05589-161">An application copying a fragment of HTML to the clipboard can choose to create a BASE element to include in the context if such an element is not already present so that partial URLs in the fragment can be resolved.</span></span>

<span data-ttu-id="05589-162">O contexto é opcional, pois informações suficientes são incluídas no fragmento para a colagem básica de um fragmento de HTML para ocorrer.</span><span class="sxs-lookup"><span data-stu-id="05589-162">The context is optional, as sufficient information is included in the fragment for basic pasting of an HTML fragment to take place.</span></span> <span data-ttu-id="05589-163">Se o contexto não for armazenado, o fragmento somente será armazenado e o StartHTML = endhtml =-1.</span><span class="sxs-lookup"><span data-stu-id="05589-163">If the context is not stored, the fragment only is stored and the StartHTML=EndHTML=-1.</span></span>

## <a name="scenarios"></a><span data-ttu-id="05589-164">Cenários</span><span class="sxs-lookup"><span data-stu-id="05589-164">Scenarios</span></span>

<span data-ttu-id="05589-165">Os cenários a seguir descrevem como o editor de HTML IE4/MSHTML trata do HTML recortar e colar; outros aplicativos podem ou não seguir esses cenários.</span><span class="sxs-lookup"><span data-stu-id="05589-165">The following scenarios describe how the IE4/MSHTML HTML editor handles HTML cut and paste; other applications may or may not follow these scenarios.</span></span> <span data-ttu-id="05589-166">O formato da área de transferência descrito aqui destina-se a permitir a flexibilidade de como um aplicativo opta por funcionar.</span><span class="sxs-lookup"><span data-stu-id="05589-166">The clipboard format described here is intended to allow flexibility for how an application chooses to function.</span></span> <span data-ttu-id="05589-167">(Esses cenários mostram apenas um bom HTML, ou seja, não há marcas sobrepostas.)</span><span class="sxs-lookup"><span data-stu-id="05589-167">(These scenarios show only good HTML, that is, no overlapping tags.)</span></span>

1.  <span data-ttu-id="05589-168">Fragmento simples de HTML.</span><span class="sxs-lookup"><span data-stu-id="05589-168">Simple Fragment of HTML.</span></span>
    -   -   <span data-ttu-id="05589-169">Texto HTML:</span><span class="sxs-lookup"><span data-stu-id="05589-169">HTML text:</span></span>

            <span data-ttu-id="05589-170"><BODY>Isso é normal. isso é <B>negrito </B>e <I> <B>negrito </B></I> é itálico</BODY></span><span class="sxs-lookup"><span data-stu-id="05589-170"><BODY>This is normal <B>This is bold </B><I><B>This is bold italic </B>This is italic </I></BODY></span></span>

        -   <span data-ttu-id="05589-171">Aparece como:</span><span class="sxs-lookup"><span data-stu-id="05589-171">Appears as:</span></span>

            <span data-ttu-id="05589-172">Isso é normal. isso é **negrito** e    \* **negrito** é itálico   \*</span><span class="sxs-lookup"><span data-stu-id="05589-172">This is normal **This is bold**  \***This is bold italic**  This is italic\*</span></span>

        -   <span data-ttu-id="05589-173">O texto entre o \* \* é selecionado e copiado para a área de transferência:</span><span class="sxs-lookup"><span data-stu-id="05589-173">The text between the \*\* is selected and copied to the clipboard:</span></span>

            <span data-ttu-id="05589-174">Isso é normal. este é **um negrito em** \* \*     \* **itálico**   este \* \* \* *é itálico*</span><span class="sxs-lookup"><span data-stu-id="05589-174">This is normal **This is** \*\* **bold**   \***This is bold italic**  This\*\*\* *is italic*</span></span>

        -   <span data-ttu-id="05589-175">É isso que estará na área de transferência (Observe que é a interpretação de IE4/MSHTML):</span><span class="sxs-lookup"><span data-stu-id="05589-175">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <span data-ttu-id="05589-176">Versão: 0,9</span><span class="sxs-lookup"><span data-stu-id="05589-176">Version:0.9</span></span>

            <span data-ttu-id="05589-177">StartHTML: 71</span><span class="sxs-lookup"><span data-stu-id="05589-177">StartHTML:71</span></span>

            <span data-ttu-id="05589-178">Endhtml: 160</span><span class="sxs-lookup"><span data-stu-id="05589-178">EndHTML:160</span></span>

            <span data-ttu-id="05589-179">StartFragment: 130</span><span class="sxs-lookup"><span data-stu-id="05589-179">StartFragment:130</span></span>

            <span data-ttu-id="05589-180">EndFragment: 150</span><span class="sxs-lookup"><span data-stu-id="05589-180">EndFragment:150</span></span>

            <span data-ttu-id="05589-181">**StartSelection: 130**</span><span class="sxs-lookup"><span data-stu-id="05589-181">**StartSelection:130**</span></span>

            <span data-ttu-id="05589-182">**Fim da seleção: 150**</span><span class="sxs-lookup"><span data-stu-id="05589-182">**EndSelection:150**</span></span>

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            <span data-ttu-id="05589-183">**<B>negrito</B><I><B>este é negrito e itálico</B></I>**</span><span class="sxs-lookup"><span data-stu-id="05589-183">**<B>bold</B><I><B>This is bold italic</B>This</I>**</span></span>

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   <span data-ttu-id="05589-184">Nesse cenário, apenas a marca BODY e a marca HTML aparecem no contexto, pois ele precede o fragmento selecionado.</span><span class="sxs-lookup"><span data-stu-id="05589-184">In this scenario only the BODY tag and the HTML tag appear in the context as it precedes the selected fragment.</span></span> <span data-ttu-id="05589-185">Observe que as marcas de início e as marcas de fim são incluídas no contexto.</span><span class="sxs-lookup"><span data-stu-id="05589-185">Note that start tags and end tags are included in the context.</span></span> <span data-ttu-id="05589-186">A seleção, como delimitada por StartSelection e endselectation, é mostrada em negrito.</span><span class="sxs-lookup"><span data-stu-id="05589-186">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

2.  <span data-ttu-id="05589-187">Fragmento de uma tabela em HTML.</span><span class="sxs-lookup"><span data-stu-id="05589-187">Fragment of a table in HTML.</span></span>
    -   -   <span data-ttu-id="05589-188">Texto HTML:</span><span class="sxs-lookup"><span data-stu-id="05589-188">HTML text:</span></span>

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="05589-189">Head1</span><span class="sxs-lookup"><span data-stu-id="05589-189">Head1</span></span></TH><TD><span data-ttu-id="05589-190">Item 1</span><span class="sxs-lookup"><span data-stu-id="05589-190">Item 1</span></span></TD><TD><span data-ttu-id="05589-191">Item 2</span><span class="sxs-lookup"><span data-stu-id="05589-191">Item 2</span></span></TD><TD><span data-ttu-id="05589-192">Item 3</span><span class="sxs-lookup"><span data-stu-id="05589-192">Item 3</span></span></TD><TD><span data-ttu-id="05589-193">Item 4</span><span class="sxs-lookup"><span data-stu-id="05589-193">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="05589-194">Item 5</span><span class="sxs-lookup"><span data-stu-id="05589-194">Item 5</span></span></TD><TD><span data-ttu-id="05589-195">Item 6</span><span class="sxs-lookup"><span data-stu-id="05589-195">Item 6</span></span></TD><TD><span data-ttu-id="05589-196">Item 7</span><span class="sxs-lookup"><span data-stu-id="05589-196">Item 7</span></span></TD><TD><span data-ttu-id="05589-197">Item 8</span><span class="sxs-lookup"><span data-stu-id="05589-197">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="05589-198">Head2</span><span class="sxs-lookup"><span data-stu-id="05589-198">Head2</span></span></TH><TD><span data-ttu-id="05589-199">Item 9</span><span class="sxs-lookup"><span data-stu-id="05589-199">Item 9</span></span></TD><TD><span data-ttu-id="05589-200">Item 10</span><span class="sxs-lookup"><span data-stu-id="05589-200">Item 10</span></span></TD><TD><span data-ttu-id="05589-201">Item 11</span><span class="sxs-lookup"><span data-stu-id="05589-201">Item 11</span></span></TD><TD><span data-ttu-id="05589-202">Item 12</span><span class="sxs-lookup"><span data-stu-id="05589-202">Item 12</span></span></TD></TR></TABLE></BODY>

        -   <span data-ttu-id="05589-203">Aparece como: ></span><span class="sxs-lookup"><span data-stu-id="05589-203">Appears as: ></span></span><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="05589-204">Head1</span><span class="sxs-lookup"><span data-stu-id="05589-204">Head1</span></span></TH><TD><span data-ttu-id="05589-205">Item 1</span><span class="sxs-lookup"><span data-stu-id="05589-205">Item 1</span></span></TD><TD><span data-ttu-id="05589-206">Item 2</span><span class="sxs-lookup"><span data-stu-id="05589-206">Item 2</span></span></TD><TD><span data-ttu-id="05589-207">Item 3</span><span class="sxs-lookup"><span data-stu-id="05589-207">Item 3</span></span></TD><TD><span data-ttu-id="05589-208">Item 4</span><span class="sxs-lookup"><span data-stu-id="05589-208">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="05589-209">Item 5</span><span class="sxs-lookup"><span data-stu-id="05589-209">Item 5</span></span></TD><TD><span data-ttu-id="05589-210">Item 6</span><span class="sxs-lookup"><span data-stu-id="05589-210">Item 6</span></span></TD><TD><span data-ttu-id="05589-211">Item 7</span><span class="sxs-lookup"><span data-stu-id="05589-211">Item 7</span></span></TD><TD><span data-ttu-id="05589-212">Item 8</span><span class="sxs-lookup"><span data-stu-id="05589-212">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="05589-213">Head2</span><span class="sxs-lookup"><span data-stu-id="05589-213">Head2</span></span></TH><TD><span data-ttu-id="05589-214">Item 9</span><span class="sxs-lookup"><span data-stu-id="05589-214">Item 9</span></span></TD><TD><span data-ttu-id="05589-215">Item 10</span><span class="sxs-lookup"><span data-stu-id="05589-215">Item 10</span></span></TD><TD><span data-ttu-id="05589-216">Item 11</span><span class="sxs-lookup"><span data-stu-id="05589-216">Item 11</span></span></TD><TD><span data-ttu-id="05589-217">Item 12</span><span class="sxs-lookup"><span data-stu-id="05589-217">Item 12</span></span></TD></TR></TABLE><span data-ttu-id="05589-218"><! \[ CDATA\[\]\]></span><span class="sxs-lookup"><span data-stu-id="05589-218"><!\[CDATA\[\]\]></span></span>
        -   <span data-ttu-id="05589-219">Os elementos item 6, Item7, item 10 e item 11 da tabela são selecionados como um bloco e copiados para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="05589-219">The Item 6, Item7, Item 10, and Item 11 elements of the table are selected as a block and copied to the clipboard.</span></span>
        -   <span data-ttu-id="05589-220">É isso que estará na área de transferência (Observe que é a interpretação de IE4/MSHTML):</span><span class="sxs-lookup"><span data-stu-id="05589-220">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            <span data-ttu-id="05589-221">**<TR><TD>Item 6 </TD> <TD> item 7 item </TD> </TR> <TR> <TD> 10 </TD> <TD> Item 11</TD></TR>**</span><span class="sxs-lookup"><span data-stu-id="05589-221">**<TR><TD>Item 6</TD><TD>Item 7</TD></TR><TR><TD>Item 10</TD><TD>Item 11</TD></TR>**</span></span>

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  <span data-ttu-id="05589-222">Colando um fragmento de uma lista ordenada em texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="05589-222">Pasting a fragment of an ordered list into plain text.</span></span>
    -   -   <span data-ttu-id="05589-223">Texto HTML:</span><span class="sxs-lookup"><span data-stu-id="05589-223">HTML text:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="05589-224">Item 1</span><span class="sxs-lookup"><span data-stu-id="05589-224">Item 1</span></span><LI><span data-ttu-id="05589-225">Item 2</span><span class="sxs-lookup"><span data-stu-id="05589-225">Item 2</span></span><LI><span data-ttu-id="05589-226">Item 3</span><span class="sxs-lookup"><span data-stu-id="05589-226">Item 3</span></span><LI><span data-ttu-id="05589-227">Item 4</span><span class="sxs-lookup"><span data-stu-id="05589-227">Item 4</span></span><LI><span data-ttu-id="05589-228">Item 5</span><span class="sxs-lookup"><span data-stu-id="05589-228">Item 5</span></span><LI><span data-ttu-id="05589-229">Item 6</span><span class="sxs-lookup"><span data-stu-id="05589-229">Item 6</span></span></OL></BODY>

        -   <span data-ttu-id="05589-230">Aparece como:</span><span class="sxs-lookup"><span data-stu-id="05589-230">Appears as:</span></span>
            1.  <span data-ttu-id="05589-231">Item 1</span><span class="sxs-lookup"><span data-stu-id="05589-231">Item 1</span></span>
            2.  <span data-ttu-id="05589-232">Item 2</span><span class="sxs-lookup"><span data-stu-id="05589-232">Item 2</span></span>
            3.  <span data-ttu-id="05589-233">Item 3</span><span class="sxs-lookup"><span data-stu-id="05589-233">Item 3</span></span>
            4.  <span data-ttu-id="05589-234">Item 4</span><span class="sxs-lookup"><span data-stu-id="05589-234">Item 4</span></span>
            5.  <span data-ttu-id="05589-235">Item 5</span><span class="sxs-lookup"><span data-stu-id="05589-235">Item 5</span></span>
            6.  <span data-ttu-id="05589-236">Item 6</span><span class="sxs-lookup"><span data-stu-id="05589-236">Item 6</span></span>
        -   <span data-ttu-id="05589-237">O usuário seleciona e copia os itens de 3 a 5 para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="05589-237">The user selects and copies items 3 through 5 to the clipboard.</span></span> <span data-ttu-id="05589-238">O HTML a seguir está na área de transferência:</span><span class="sxs-lookup"><span data-stu-id="05589-238">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="05589-239"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="05589-239"><DOCTYPE...><HTML><BODY></span></span><OL TYPE = a>

            <!-- StartFragment-->

            <span data-ttu-id="05589-240">**<LI>Item 3 item <LI> 4 <LI> item 5**</span><span class="sxs-lookup"><span data-stu-id="05589-240">**<LI>Item 3<LI>Item 4<LI>Item 5**</span></span>

            <!-- EndFragment-->

            </OL></BODY></HTML>

            <span data-ttu-id="05589-241">A seleção, como delimitada por StartSelection e endselectation, é mostrada em negrito.</span><span class="sxs-lookup"><span data-stu-id="05589-241">The selection, as delimited by StartSelection and EndSelection, is show in bold.</span></span>

        -   <span data-ttu-id="05589-242">Se esse fragmento for agora colado em um documento vazio, o seguinte HTML será criado:</span><span class="sxs-lookup"><span data-stu-id="05589-242">If this fragment is now pasted into an empty document, the following HTML will be created:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="05589-243">Item 3</span><span class="sxs-lookup"><span data-stu-id="05589-243">Item 3</span></span><LI><span data-ttu-id="05589-244">Item 4</span><span class="sxs-lookup"><span data-stu-id="05589-244">Item 4</span></span><LI><span data-ttu-id="05589-245">Item 5</span><span class="sxs-lookup"><span data-stu-id="05589-245">Item 5</span></span></OL></BODY>

        -   <span data-ttu-id="05589-246">Aparecendo como:</span><span class="sxs-lookup"><span data-stu-id="05589-246">Appearing as:</span></span>
            1.  <span data-ttu-id="05589-247">Item 3</span><span class="sxs-lookup"><span data-stu-id="05589-247">Item 3</span></span>
            2.  <span data-ttu-id="05589-248">Item 4</span><span class="sxs-lookup"><span data-stu-id="05589-248">Item 4</span></span>
            3.  <span data-ttu-id="05589-249">Item 5</span><span class="sxs-lookup"><span data-stu-id="05589-249">Item 5</span></span>

4.  <span data-ttu-id="05589-250">Colando uma região parcialmente selecionada.</span><span class="sxs-lookup"><span data-stu-id="05589-250">Pasting a partially selected region.</span></span>
    -   -   <span data-ttu-id="05589-251">Texto HTML:</span><span class="sxs-lookup"><span data-stu-id="05589-251">HTML text:</span></span>

            <P> <span data-ttu-id="05589-252">IE4/MSHTML é um editor WYSIWYG que dá suporte a:</span><span class="sxs-lookup"><span data-stu-id="05589-252">IE4/MSHTML is a WYSIWYG Editor that supports :</span></span><UL><LI><span data-ttu-id="05589-253">Recortar</span><span class="sxs-lookup"><span data-stu-id="05589-253">Cut</span></span><LI><span data-ttu-id="05589-254">Copiar</span><span class="sxs-lookup"><span data-stu-id="05589-254">Copy</span></span><LI><span data-ttu-id="05589-255">Colar</span><span class="sxs-lookup"><span data-stu-id="05589-255">Paste</span></span></UL><P><span data-ttu-id="05589-256">Essa é uma excelente ferramenta!</span><span class="sxs-lookup"><span data-stu-id="05589-256">This is a Great Tool !</span></span>

        -   <span data-ttu-id="05589-257">Aparece como: IE4/MSHTML é um editor WYSIWYG que dá suporte a:</span><span class="sxs-lookup"><span data-stu-id="05589-257">Appears as:IE4/MSHTML is a WYSIWYG Editor that supports :</span></span>
            -   -   <span data-ttu-id="05589-258">Recortar</span><span class="sxs-lookup"><span data-stu-id="05589-258">Cut</span></span>
                -   <span data-ttu-id="05589-259">Copiar</span><span class="sxs-lookup"><span data-stu-id="05589-259">Copy</span></span>
                -   <span data-ttu-id="05589-260">Colar</span><span class="sxs-lookup"><span data-stu-id="05589-260">Paste</span></span>

        -   <span data-ttu-id="05589-261">O usuário seleciona "WYSIWYG" até "Cop". O HTML a seguir está na área de transferência:</span><span class="sxs-lookup"><span data-stu-id="05589-261">The user selects from "WYSIWYG" until "Cop".The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="05589-262"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="05589-262"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <P>

            <span data-ttu-id="05589-263">**Editor WYSIWYG, que dá suporte a**</span><span class="sxs-lookup"><span data-stu-id="05589-263">**WYSIWYG Editor, which supports**</span></span>

            <span data-ttu-id="05589-264">**<UL><LI>Recortar <LI> COP**</span><span class="sxs-lookup"><span data-stu-id="05589-264">**<UL><LI>Cut<LI>Cop**</span></span>

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   <span data-ttu-id="05589-265">O usuário seleciona "opiar" até "ótimo".</span><span class="sxs-lookup"><span data-stu-id="05589-265">The user selects from "opy" until "Great".</span></span>

            <span data-ttu-id="05589-266">O HTML a seguir está na área de transferência:</span><span class="sxs-lookup"><span data-stu-id="05589-266">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="05589-267"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="05589-267"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <UL><LI>

            <span data-ttu-id="05589-268">**opiar <LI> colar </UL> <P> este é um ótimo**</span><span class="sxs-lookup"><span data-stu-id="05589-268">**opy<LI>Paste</UL><P> This is a Great**</span></span>

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            <span data-ttu-id="05589-269">A seleção, como delimitada por StartSelection e endselectation, é mostrada em negrito.</span><span class="sxs-lookup"><span data-stu-id="05589-269">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

 

 




