---
title: Apresentando o DirectWrite
description: As pessoas se comunicam com o texto o tempo todo em suas vidas diárias.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite, sobre
- DirectWrite, recursos tipográficos
- tipografia
- DirectWrite, texto internacional
- DirectWrite, fontes OpenType
- Fontes OpenType
- DirectWrite, ClearType
- ClearType
- DirectWrite, visão geral da API
- DirectWrite, IDWriteFontFace
- IDWriteFontFace
- DirectWrite, renderização de texto
- DirectWrite, modos de renderização
- Interoperação DirectWrite, GDI
- DirectWrite, interoperabilidade
- interoperabilidade, DirectWrite
- interoperabilidade, Graphics Device Interface (GDI)
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823960"
---
# <a name="introducing-directwrite"></a><span data-ttu-id="e290c-122">Apresentando o DirectWrite</span><span class="sxs-lookup"><span data-stu-id="e290c-122">Introducing DirectWrite</span></span>

<span data-ttu-id="e290c-123">As pessoas se comunicam com o texto o tempo todo em suas vidas diárias.</span><span class="sxs-lookup"><span data-stu-id="e290c-123">People communicate with text all the time in their daily lives.</span></span> <span data-ttu-id="e290c-124">É a principal maneira para as pessoas consumirem um volume cada vez maior de informações.</span><span class="sxs-lookup"><span data-stu-id="e290c-124">It is the primary way for people to consume an increasing volume of information.</span></span> <span data-ttu-id="e290c-125">Antigamente, costumava ser por meio de conteúdo impresso, principalmente documentos, jornais, livros e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e290c-125">In the past, it used to be through printed content, primarily documents, newspapers, books, and so on.</span></span> <span data-ttu-id="e290c-126">Cada vez mais, é conteúdo online em seu computador Windows.</span><span class="sxs-lookup"><span data-stu-id="e290c-126">Increasingly, it is online content on their Windows PC.</span></span> <span data-ttu-id="e290c-127">Um usuário típico do Windows gasta muito tempo lendo na tela do computador.</span><span class="sxs-lookup"><span data-stu-id="e290c-127">A typical Windows user spends a lot of time reading from their computer screen.</span></span> <span data-ttu-id="e290c-128">Eles podem estar navegando na Web, verificando emails, compondo um relatório, preenchendo uma planilha ou escrevendo software, mas o que eles estão realmente fazendo é ler.</span><span class="sxs-lookup"><span data-stu-id="e290c-128">They might be surfing the Web, scanning e-mail, composing a report, filling in a spreadsheet, or writing software, but what they're really doing is reading.</span></span> <span data-ttu-id="e290c-129">Embora o texto e as fontes percarnem praticamente todas as partes da experiência do usuário no Windows, para a maioria dos usuários, a leitura na tela não é tão agradável quanto a leitura da saída impressa.</span><span class="sxs-lookup"><span data-stu-id="e290c-129">Even though text and fonts permeate nearly every part of the user experience in Windows, for most users, reading on the screen is not as enjoyable as reading printed output.</span></span>

<span data-ttu-id="e290c-130">Para desenvolvedores de aplicativos Windows, escrever código de manipulação de texto é um desafio devido aos maiores requisitos para melhor legibilidade, formatação sofisticada e controle de layout e suporte para os vários idiomas que o aplicativo deve exibir.</span><span class="sxs-lookup"><span data-stu-id="e290c-130">For Windows application developers, writing text-handling code is a challenge because of the increased requirements for better readability, sophisticated formatting and layout control, and support for the multiple languages the application must display.</span></span> <span data-ttu-id="e290c-131">Até mesmo o sistema de manipulação de texto mais básico deve permitir entrada de texto, layout, exibição, edição e cópia e colagem.</span><span class="sxs-lookup"><span data-stu-id="e290c-131">Even the most basic text-handling system must allow for text input, layout, display, editing, and copying and pasting.</span></span> <span data-ttu-id="e290c-132">Os usuários do Windows normalmente esperam ainda mais do que esses recursos básicos, exigindo até mesmo editores simples para dar suporte a várias fontes, vários estilos de parágrafo, imagens inseridas, verificação ortográfica e outros recursos.</span><span class="sxs-lookup"><span data-stu-id="e290c-132">Windows users commonly expect even more than these basic features, requiring even simple editors to support multiple fonts, various paragraph styles, embedded images, spell checking, and other features.</span></span> <span data-ttu-id="e290c-133">O design da interface do usuário moderna também não é mais refinado para formato único, texto sem formatação, mas precisa apresentar uma experiência melhor com fontes avançadas e layouts de texto.</span><span class="sxs-lookup"><span data-stu-id="e290c-133">Modern UI design is also no longer confined to single format, plain text, but needs to present a better experience with rich fonts and text layouts.</span></span>

<span data-ttu-id="e290c-134">Esta é uma introdução ao modo como o [DirectWrite](direct-write-portal.md) permite que os aplicativos do Windows aprimorem a experiência de texto para a interface do usuário e documentos.</span><span class="sxs-lookup"><span data-stu-id="e290c-134">This is an introduction to how [DirectWrite](direct-write-portal.md) enables Windows applications to enhance the text experience for UI and documents.</span></span>

## <a name="improving-the-text-experience"></a><span data-ttu-id="e290c-135">Melhorando a experiência de texto</span><span class="sxs-lookup"><span data-stu-id="e290c-135">Improving the Text Experience</span></span>

<span data-ttu-id="e290c-136">Os aplicativos modernos do Windows têm requisitos sofisticados de texto em sua interface do usuário e documentos.</span><span class="sxs-lookup"><span data-stu-id="e290c-136">Modern Windows applications have sophisticated requirements for text in their UI and documents.</span></span> <span data-ttu-id="e290c-137">Isso inclui melhor legibilidade, suporte para uma grande variedade de linguagens e scripts e desempenho de renderização superior.</span><span class="sxs-lookup"><span data-stu-id="e290c-137">These include better readability, support for a large variety of languages and scripts, and superior rendering performance.</span></span> <span data-ttu-id="e290c-138">Além disso, a maioria dos aplicativos existentes exige uma maneira de postergar os investimentos existentes na base de código WindowsWin32.</span><span class="sxs-lookup"><span data-stu-id="e290c-138">In addition, most existing applications require a way to carry forward existing investments in the WindowsWin32 code base.</span></span>

<span data-ttu-id="e290c-139">O [DirectWrite](direct-write-portal.md) fornece os três recursos a seguir que permitem que os desenvolvedores de aplicativos do Windows aprimorem a experiência de texto em seus aplicativos: independência do sistema de renderização, tipografia de alta qualidade e várias camadas de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="e290c-139">[DirectWrite](direct-write-portal.md) provides the following three features that enable Windows application developers to improve the text experience within their applications: independence from the rendering system, high-quality typography, and multiple layers of functionality.</span></span>

## <a name="rendering-system-independence"></a><span data-ttu-id="e290c-140">Independência de Rendering-System</span><span class="sxs-lookup"><span data-stu-id="e290c-140">Rendering-System Independence</span></span>

<span data-ttu-id="e290c-141">O [DirectWrite](direct-write-portal.md) é independente de qualquer tecnologia gráfica específica.</span><span class="sxs-lookup"><span data-stu-id="e290c-141">[DirectWrite](direct-write-portal.md) is independent of any particular graphics technology.</span></span> <span data-ttu-id="e290c-142">Os aplicativos são livres para usar a tecnologia de renderização mais adequada às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="e290c-142">Applications are free to use the rendering technology best suited to their needs.</span></span> <span data-ttu-id="e290c-143">Isso dá aos aplicativos a flexibilidade para continuar renderizando algumas partes de seu aplicativo por meio do GDI e de outras partes por meio do Direct3D ou do [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="e290c-143">This gives applications the flexibility to continue rendering some parts of their application through GDI and other parts through Direct3D or [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="e290c-144">Na verdade, um aplicativo poderia optar por renderizar DirectWrite por meio de uma pilha de renderização proprietária.</span><span class="sxs-lookup"><span data-stu-id="e290c-144">In fact, an application could choose to render DirectWrite through a proprietary rendering stack.</span></span>

## <a name="high-quality-typography"></a><span data-ttu-id="e290c-145">Tipografia de High-Quality</span><span class="sxs-lookup"><span data-stu-id="e290c-145">High-Quality Typography</span></span>

<span data-ttu-id="e290c-146">O [DirectWrite](direct-write-portal.md) aproveita os avanços na tecnologia de fonte [OpenType](../intl/opentype-font-format.md) para habilitar a tipografia de alta qualidade em um aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="e290c-146">[DirectWrite](direct-write-portal.md) takes advantage of the advances in [OpenType](../intl/opentype-font-format.md) Font technology to enable high quality typography within a Windows application.</span></span> <span data-ttu-id="e290c-147">O sistema de fontes DirectWrite fornece serviços para lidar com a enumeração de fontes, o fallback de fontes e o cache de fontes, que são todos necessários por aplicativos para lidar com fontes.</span><span class="sxs-lookup"><span data-stu-id="e290c-147">The DirectWrite font system provides services for dealing with font enumeration, font fallback, and font caching, which are all needed by applications for handling fonts.</span></span>

<span data-ttu-id="e290c-148">O suporte a [OpenType](../intl/opentype-font-format.md) fornecido pelo [DirectWrite](direct-write-portal.md) permite que os desenvolvedores adicionem aos seus aplicativos recursos tipográficos avançados e suporte para texto internacional.</span><span class="sxs-lookup"><span data-stu-id="e290c-148">The [OpenType](../intl/opentype-font-format.md) support provided by [DirectWrite](direct-write-portal.md) enables developers to add to their applications advanced typographic features and support for international text.</span></span>

## <a name="support-for-advanced-typographic-features"></a><span data-ttu-id="e290c-149">Suporte para recursos tipográficos avançados</span><span class="sxs-lookup"><span data-stu-id="e290c-149">Support for Advanced Typographic Features</span></span>

<span data-ttu-id="e290c-150">O [DirectWrite](direct-write-portal.md) permite que os desenvolvedores de aplicativos desbloqueiem os recursos das fontes OpenType que não podiam usar em WinForms ou GDI.</span><span class="sxs-lookup"><span data-stu-id="e290c-150">[DirectWrite](direct-write-portal.md) enables application developers to unlock the features of OpenType fonts that they couldn't use in WinForms or GDI.</span></span> <span data-ttu-id="e290c-151">O objeto DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) expõe muitos dos recursos avançados das fontes OpenType, como alternativas estilísticos e traços violentos.</span><span class="sxs-lookup"><span data-stu-id="e290c-151">The DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) object exposes many of the advanced features of OpenType fonts, such as stylistic alternates and swashes.</span></span> <span data-ttu-id="e290c-152">O SDK (Software Development Kit) do Microsoft Windows fornece um conjunto de fontes [OpenType](../intl/opentype-font-format.md) de exemplo projetadas com recursos avançados, como as fontes Pericles e Pescadero.</span><span class="sxs-lookup"><span data-stu-id="e290c-152">The Microsoft Windows Software Development Kit (SDK) provides a set of sample [OpenType](../intl/opentype-font-format.md) fonts that are designed with rich features, such as the Pericles and Pescadero fonts.</span></span> <span data-ttu-id="e290c-153">Para obter mais detalhes sobre os recursos do OpenType, consulte [recursos de fonte OpenType](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e290c-153">For more details on OpenType features, see [OpenType Font Features](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span></span>

## <a name="support-for-international-text"></a><span data-ttu-id="e290c-154">Suporte para texto internacional</span><span class="sxs-lookup"><span data-stu-id="e290c-154">Support for International Text</span></span>

<span data-ttu-id="e290c-155">O [DirectWrite](direct-write-portal.md) usa fontes [OpenType](../intl/opentype-font-format.md) para habilitar amplo suporte para texto internacional.</span><span class="sxs-lookup"><span data-stu-id="e290c-155">[DirectWrite](direct-write-portal.md) uses [OpenType](../intl/opentype-font-format.md) fonts to enable broad support for international text.</span></span> <span data-ttu-id="e290c-156">Há suporte para recursos Unicode, como substitutos, BIDI, quebra de linha e UVS.</span><span class="sxs-lookup"><span data-stu-id="e290c-156">Unicode features such as surrogates, BIDI, line breaking, and UVS are supported.</span></span> <span data-ttu-id="e290c-157">A discriminação de script guiada por idioma, a substituição de números e a modelagem de glifo garantem que o texto em qualquer script tenha o layout e a renderização corretos.</span><span class="sxs-lookup"><span data-stu-id="e290c-157">Language-guided script itemization, number substitution, and glyph shaping ensure that text in any script has the correct layout and rendering.</span></span>

<span data-ttu-id="e290c-158">Os scripts a seguir tem suporte atualmente:</span><span class="sxs-lookup"><span data-stu-id="e290c-158">The following scripts are currently supported:</span></span>

> [!Note]  
> <span data-ttu-id="e290c-159">Para scripts marcados com um \* , não há nenhuma fonte de sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="e290c-159">For scripts marked with an \*, there are no default system fonts.</span></span> <span data-ttu-id="e290c-160">Os aplicativos devem instalar fontes que dão suporte a esses scripts.</span><span class="sxs-lookup"><span data-stu-id="e290c-160">Applications must install fonts that support these scripts.</span></span>

 

-   <span data-ttu-id="e290c-161">Árabe</span><span class="sxs-lookup"><span data-stu-id="e290c-161">Arabic</span></span>
-   <span data-ttu-id="e290c-162">Armênia</span><span class="sxs-lookup"><span data-stu-id="e290c-162">Armenian</span></span>
-   <span data-ttu-id="e290c-163">Bengala</span><span class="sxs-lookup"><span data-stu-id="e290c-163">Bengala</span></span>
-   <span data-ttu-id="e290c-164">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="e290c-164">Bopomofo</span></span>
-   <span data-ttu-id="e290c-165">Braille\*</span><span class="sxs-lookup"><span data-stu-id="e290c-165">Braille\*</span></span>
-   <span data-ttu-id="e290c-166">Silábico canadense Aboriginal</span><span class="sxs-lookup"><span data-stu-id="e290c-166">Canadian aboriginal syllabics</span></span>
-   <span data-ttu-id="e290c-167">Cherokee</span><span class="sxs-lookup"><span data-stu-id="e290c-167">Cherokee</span></span>
-   <span data-ttu-id="e290c-168">Chinês (simplificado & tradicional)</span><span class="sxs-lookup"><span data-stu-id="e290c-168">Chinese (Simplified & Traditional)</span></span>
-   <span data-ttu-id="e290c-169">Cirílico</span><span class="sxs-lookup"><span data-stu-id="e290c-169">Cyrillic</span></span>
-   <span data-ttu-id="e290c-170">Copta\*</span><span class="sxs-lookup"><span data-stu-id="e290c-170">Coptic\*</span></span>
-   <span data-ttu-id="e290c-171">Devanagari</span><span class="sxs-lookup"><span data-stu-id="e290c-171">Devanagari</span></span>
-   <span data-ttu-id="e290c-172">Etíope</span><span class="sxs-lookup"><span data-stu-id="e290c-172">Ethiopic</span></span>
-   <span data-ttu-id="e290c-173">Georgiano</span><span class="sxs-lookup"><span data-stu-id="e290c-173">Georgian</span></span>
-   <span data-ttu-id="e290c-174">Letra\*</span><span class="sxs-lookup"><span data-stu-id="e290c-174">Glagolitic\*</span></span>
-   <span data-ttu-id="e290c-175">Grego</span><span class="sxs-lookup"><span data-stu-id="e290c-175">Greek</span></span>
-   <span data-ttu-id="e290c-176">Guzerate</span><span class="sxs-lookup"><span data-stu-id="e290c-176">Gujarati</span></span>
-   <span data-ttu-id="e290c-177">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="e290c-177">Gurmukhi</span></span>
-   <span data-ttu-id="e290c-178">Hebraico</span><span class="sxs-lookup"><span data-stu-id="e290c-178">Hebrew</span></span>
-   <span data-ttu-id="e290c-179">Japonês</span><span class="sxs-lookup"><span data-stu-id="e290c-179">Japanese</span></span>
-   <span data-ttu-id="e290c-180">canarim</span><span class="sxs-lookup"><span data-stu-id="e290c-180">Kannada</span></span>
-   <span data-ttu-id="e290c-181">Khmer</span><span class="sxs-lookup"><span data-stu-id="e290c-181">Khmer</span></span>
-   <span data-ttu-id="e290c-182">Coreano</span><span class="sxs-lookup"><span data-stu-id="e290c-182">Korean</span></span>
-   <span data-ttu-id="e290c-183">Lao</span><span class="sxs-lookup"><span data-stu-id="e290c-183">Lao</span></span>
-   <span data-ttu-id="e290c-184">Latim</span><span class="sxs-lookup"><span data-stu-id="e290c-184">Latin</span></span>
-   <span data-ttu-id="e290c-185">Malaiala</span><span class="sxs-lookup"><span data-stu-id="e290c-185">Malayalam</span></span>
-   <span data-ttu-id="e290c-186">Mongol</span><span class="sxs-lookup"><span data-stu-id="e290c-186">Mongolian</span></span>
-   <span data-ttu-id="e290c-187">Myanmar</span><span class="sxs-lookup"><span data-stu-id="e290c-187">Myanmar</span></span>
-   <span data-ttu-id="e290c-188">Tai Lue Novo</span><span class="sxs-lookup"><span data-stu-id="e290c-188">New Tai Lue</span></span>
-   <span data-ttu-id="e290c-189">Ogham\*</span><span class="sxs-lookup"><span data-stu-id="e290c-189">Ogham\*</span></span>
-   <span data-ttu-id="e290c-190">Oriá</span><span class="sxs-lookup"><span data-stu-id="e290c-190">Odia</span></span>
-   <span data-ttu-id="e290c-191">' Phags-pa</span><span class="sxs-lookup"><span data-stu-id="e290c-191">'Phags-pa</span></span>
-   <span data-ttu-id="e290c-192">Rúnica\*</span><span class="sxs-lookup"><span data-stu-id="e290c-192">Runic\*</span></span>
-   <span data-ttu-id="e290c-193">Sinhala</span><span class="sxs-lookup"><span data-stu-id="e290c-193">Sinhala</span></span>
-   <span data-ttu-id="e290c-194">Siríaco</span><span class="sxs-lookup"><span data-stu-id="e290c-194">Syriac</span></span>
-   <span data-ttu-id="e290c-195">Tai Le</span><span class="sxs-lookup"><span data-stu-id="e290c-195">Tai Le</span></span>
-   <span data-ttu-id="e290c-196">Tâmil</span><span class="sxs-lookup"><span data-stu-id="e290c-196">Tamil</span></span>
-   <span data-ttu-id="e290c-197">Télugo</span><span class="sxs-lookup"><span data-stu-id="e290c-197">Telugu</span></span>
-   <span data-ttu-id="e290c-198">Thaana</span><span class="sxs-lookup"><span data-stu-id="e290c-198">Thaana</span></span>
-   <span data-ttu-id="e290c-199">Tailandês</span><span class="sxs-lookup"><span data-stu-id="e290c-199">Thai</span></span>
-   <span data-ttu-id="e290c-200">Tibetano</span><span class="sxs-lookup"><span data-stu-id="e290c-200">Tibetan</span></span>
-   <span data-ttu-id="e290c-201">Yi</span><span class="sxs-lookup"><span data-stu-id="e290c-201">Yi</span></span>

## <a name="multiple-layers-of-functionality"></a><span data-ttu-id="e290c-202">Várias camadas de funcionalidade</span><span class="sxs-lookup"><span data-stu-id="e290c-202">Multiple Layers of Functionality</span></span>

<span data-ttu-id="e290c-203">O [DirectWrite](direct-write-portal.md) fornece camadas fatoradas de funcionalidade, com cada camada interagindo sem problemas com o próximo.</span><span class="sxs-lookup"><span data-stu-id="e290c-203">[DirectWrite](direct-write-portal.md) provides factored layers of functionality, with each layer interacting seamlessly with the next.</span></span> <span data-ttu-id="e290c-204">O design de API oferece aos desenvolvedores de aplicativos a liberdade e a flexibilidade para adotar camadas individuais dependendo de suas necessidades e agendas.</span><span class="sxs-lookup"><span data-stu-id="e290c-204">The API design gives application developers the freedom and flexibility to adopt individual layers depending on their needs and schedule.</span></span> <span data-ttu-id="e290c-205">O diagrama a seguir mostra a relação entre essas camadas.</span><span class="sxs-lookup"><span data-stu-id="e290c-205">The following diagram shows the relationship between these layers.</span></span>

![diagrama de camadas DirectWrite e como eles se comunicam com um aplicativo ou estrutura de interface do usuário e a API de gráficos](images/intro-01.png)

<span data-ttu-id="e290c-207">A API de layout de texto fornece a funcionalidade de nível mais alto disponível em [DirectWrite](direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="e290c-207">The text layout API provides the highest level functionality available from [DirectWrite](direct-write-portal.md).</span></span> <span data-ttu-id="e290c-208">Ele fornece serviços para que o aplicativo meça, exiba e interaja com cadeias de caracteres de texto formatadas de formato avançado.</span><span class="sxs-lookup"><span data-stu-id="e290c-208">It provides services for the application to measure, display, and interact with richly formatted text strings.</span></span> <span data-ttu-id="e290c-209">Essa API de texto pode ser usada em aplicativos que atualmente usam o DrawText Win32's para criar uma interface do usuário moderna com texto formatado de formato rico.</span><span class="sxs-lookup"><span data-stu-id="e290c-209">This text API can be used in applications that currently use Win32's DrawText to build a modern UI with richly formatted text.</span></span>

<span data-ttu-id="e290c-210">Aplicativos com uso intensivo de texto que implementam seu próprio mecanismo de layout podem usar a próxima camada abaixo: o processador de script.</span><span class="sxs-lookup"><span data-stu-id="e290c-210">Text-intensive applications that implement their own layout engine may use the next layer down: the script processor.</span></span> <span data-ttu-id="e290c-211">O processador de script divide uma parte do texto em blocos de script e manipula o mapeamento entre representações Unicode para a representação de glifo apropriada na fonte, de modo que o texto do script possa ser exibido corretamente no idioma correto.</span><span class="sxs-lookup"><span data-stu-id="e290c-211">The script processor breaks down a chunk of text into script blocks and handles the mapping between Unicode representations to the appropriate glyph representation in the font so the text of the script can be correctly displayed in the correct language.</span></span> <span data-ttu-id="e290c-212">O sistema de layout usado pela camada de API de layout de texto baseia-se na fonte e no sistema de processamento de scripts.</span><span class="sxs-lookup"><span data-stu-id="e290c-212">The layout system used by the text layout API layer is built upon the font and script processing system.</span></span>

<span data-ttu-id="e290c-213">A camada de renderização de glifo é a camada mais baixa de funcionalidade e fornece a funcionalidade de renderização de glifo para aplicativos que implementam seu próprio mecanismo de layout de texto.</span><span class="sxs-lookup"><span data-stu-id="e290c-213">The glyph-rendering layer is the lowest layer of functionality and provides glyph-rendering functionality for applications that implement their own text layout engine.</span></span> <span data-ttu-id="e290c-214">A camada de renderização de glifo também é útil para aplicativos que implementam um renderizador personalizado para modificar o comportamento de desenho de glifo por meio da função de retorno de chamada na API de formatação de texto [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e290c-214">The glyph rendering layer is also useful for applications that implement a custom renderer to modify the glyph-drawing behavior through the callback function in the [DirectWrite](direct-write-portal.md) text-formatting API.</span></span>

<span data-ttu-id="e290c-215">O sistema de fontes [DirectWrite](direct-write-portal.md) está disponível para todas as camadas funcionais do DirectWrite e permite que um aplicativo acesse informações de fonte e glifo.</span><span class="sxs-lookup"><span data-stu-id="e290c-215">The [DirectWrite](direct-write-portal.md) font system is available to all the DirectWrite functional layers and enables an application to access font and glyph information.</span></span> <span data-ttu-id="e290c-216">Ele foi projetado para lidar com tecnologias de fonte e formatos de dados comuns.</span><span class="sxs-lookup"><span data-stu-id="e290c-216">It is designed to handle common font technologies and data formats.</span></span> <span data-ttu-id="e290c-217">O modelo de fonte DirectWrite segue a prática tipográfica comum de dar suporte a qualquer número de pesos, estilos e ampliações na mesma família de fontes.</span><span class="sxs-lookup"><span data-stu-id="e290c-217">The DirectWrite font model follows the common typographic practice of supporting any number of weights, styles, and stretches in the same font family.</span></span> <span data-ttu-id="e290c-218">Esse modelo, o mesmo modelo seguido pelo WPF e o CSS, especifica que as fontes diferem apenas em peso (negrito, luz e assim por diante), estilo (vertical, itálico ou oblíquo) ou ampliação (estreito, condensada, largo e assim por diante) são considerados membros de uma única família de fontes.</span><span class="sxs-lookup"><span data-stu-id="e290c-218">This model, the same model followed by WPF and CSS, specifies that fonts differing only in weight (bold, light, and so on), style (upright, italic, or oblique) or stretch (narrow, condensed, wide, and so on) are considered to be members of a single font family.</span></span>

### <a name="improved-text-rendering-with-cleartype"></a><span data-ttu-id="e290c-219">Renderização de texto aprimorada com ClearType</span><span class="sxs-lookup"><span data-stu-id="e290c-219">Improved Text Rendering with ClearType</span></span>

<span data-ttu-id="e290c-220">Melhorar a legibilidade na tela é um requisito importante para todos os aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="e290c-220">Improving readability on the screen is a key requirement for all Windows applications.</span></span> <span data-ttu-id="e290c-221">A evidência da pesquisa no cognitiva psicologia indica que precisamos ser capazes de reconhecer cada letra com precisão e que o espaçamento uniforme entre as letras é essencial para o processamento rápido.</span><span class="sxs-lookup"><span data-stu-id="e290c-221">The evidence from research in cognitive psychology indicates that we need to be able to recognize every letter accurately and that even spacing between letters is critical for fast processing.</span></span> <span data-ttu-id="e290c-222">Letras e palavras que não são simétricas são percebidas como ruins e prejudicam a experiência de leitura.</span><span class="sxs-lookup"><span data-stu-id="e290c-222">Letters and words that are not symmetrical are perceived as ugly and degrade the reading experience.</span></span> <span data-ttu-id="e290c-223">Kevin Larson, grupo de tecnologias de leitura avançada da Microsoft, escreveu um artigo sobre o assunto que foi publicado no espectro IEEE.</span><span class="sxs-lookup"><span data-stu-id="e290c-223">Kevin Larson, Microsoft Advanced Reading Technologies group, wrote an article on the subject that was published in Spectrum IEEE.</span></span> <span data-ttu-id="e290c-224">O artigo é chamado "a tecnologia de texto" ( https://www.spectrum.ieee.org/print/5049) .</span><span class="sxs-lookup"><span data-stu-id="e290c-224">The article is called "The Technology of Text" (https://www.spectrum.ieee.org/print/5049).</span></span>

<span data-ttu-id="e290c-225">O texto em [DirectWrite](direct-write-portal.md) é renderizado usando o Microsoft ClearType, o que aumenta a clareza e a legibilidade do texto.</span><span class="sxs-lookup"><span data-stu-id="e290c-225">Text in [DirectWrite](direct-write-portal.md) is rendered using Microsoft ClearType, which enhances the clarity and readability of text.</span></span> <span data-ttu-id="e290c-226">O ClearType aproveita o fato de que monitores de LCD modernos têm faixas RGB para cada pixel que pode ser controlado individualmente.</span><span class="sxs-lookup"><span data-stu-id="e290c-226">ClearType takes advantage of the fact that modern LCD displays have RGB stripes for each pixel that can be controlled individually.</span></span> <span data-ttu-id="e290c-227">O DirectWrite usa os aprimoramentos mais recentes para o ClearType, primeiro incluído com o Windows Vista com Windows Presentation Foundation, que permite que ele avalie não apenas as letras individuais, mas também o espaçamento entre as letras.</span><span class="sxs-lookup"><span data-stu-id="e290c-227">DirectWrite uses the latest enhancements to ClearType, first included with Windows Vista with Windows Presentation Foundation, that enables it to evaluate not just the individual letters but also the spacing between letters.</span></span> <span data-ttu-id="e290c-228">Antes desses aprimoramentos de ClearType, era difícil exibir um texto com um tamanho de "leitura" de 10 ou 12 pontos: poderíamos inserir 1 pixel entre letras, o que geralmente era muito pouco ou 2 pixels, o que geralmente era muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="e290c-228">Before these ClearType enhancements, text with a "reading" size of 10 or 12 points was difficult to display: we could place either 1 pixel in between letters, which was often too little, or 2 pixels, which was often too much.</span></span> <span data-ttu-id="e290c-229">O uso da resolução extra nos subpixels nos fornece espaçamento fracionário, o que melhora o uniformidade e a simetria da página inteira.</span><span class="sxs-lookup"><span data-stu-id="e290c-229">Using the extra resolution in the subpixels provides us with fractional spacing, which improves the evenness and symmetry of the entire page.</span></span>

<span data-ttu-id="e290c-230">As duas ilustrações a seguir mostram como os glifos podem começar em qualquer limite de subpixel quando o posicionamento de subpixel é usado.</span><span class="sxs-lookup"><span data-stu-id="e290c-230">The following two illustration show how glyphs may begin on any sub-pixel boundary when sub-pixel positioning is used.</span></span>

<span data-ttu-id="e290c-231">A ilustração a seguir é renderizada usando a versão GDI do renderizador ClearType, que não emprega o posicionamento de sub-pixel.</span><span class="sxs-lookup"><span data-stu-id="e290c-231">The following illustration is rendered using the GDI version of the ClearType renderer, which did not employ sub-pixel positioning.</span></span>

![ilustração de "tecnologia" renderizada sem posicionamento de sub-pixel](images/intro-03.png)

<span data-ttu-id="e290c-233">A ilustração a seguir é renderizada usando a versão [DirectWrite](direct-write-portal.md) do renderizador ClearType, que usa o posicionamento de sub-pixel.</span><span class="sxs-lookup"><span data-stu-id="e290c-233">The following illustration is rendered using the [DirectWrite](direct-write-portal.md) version of the ClearType renderer, which uses sub-pixel positioning.</span></span>

![ilustração de "tecnologia" renderizada com posicionamento de subpixel](images/intro-04.png)

<span data-ttu-id="e290c-235">Observe que o espaçamento entre as letras h e n é mais uniforme na segunda imagem e a letra o é espaçada além da letra n, mais, mesmo com a letra l.</span><span class="sxs-lookup"><span data-stu-id="e290c-235">Note that the spacing between the letters h and n is more even in the second image and the letter o is spaced further from the letter n, more even with the letter l.</span></span> <span data-ttu-id="e290c-236">Observe também como as hastes das letras l são mais naturais.</span><span class="sxs-lookup"><span data-stu-id="e290c-236">Also note how the stems on the letters l are more natural looking.</span></span>

<span data-ttu-id="e290c-237">O posicionamento de ClearType em subpixel oferece o espaçamento mais preciso de caracteres na tela, especialmente em tamanhos pequenos, em que a diferença entre um sub-pixel e um pixel inteiro representa uma proporção significativa da largura do glifo.</span><span class="sxs-lookup"><span data-stu-id="e290c-237">The subpixel ClearType positioning offers the most accurate spacing of characters on screen, especially at small sizes where the difference between a sub-pixel and a whole pixel represents a significant proportion of glyph width.</span></span> <span data-ttu-id="e290c-238">Ele permite que o texto seja medido no espaço de resolução ideal e renderizado em sua posição natural na faixa de cores do LCD, com granularidade de subpixel.</span><span class="sxs-lookup"><span data-stu-id="e290c-238">It enables text to be measured in ideal resolution space and rendered at its natural position at the LCD color stripe, with subpixel granularity.</span></span> <span data-ttu-id="e290c-239">O texto medido e renderizado usando essa tecnologia é, por definição, independente de resolução, o que significa que exatamente o mesmo layout de texto é obtido na faixa de várias resoluções de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e290c-239">Text measured and rendered using this technology is, by definition, resolution-independent, meaning that the exact same layout of text is achieved across the range of various display resolutions.</span></span>

<span data-ttu-id="e290c-240">Ao contrário de qualquer tipo de renderização de ClearType do GDI, o recurso ClearType de sub-pixel oferece a largura de caracteres mais precisa.</span><span class="sxs-lookup"><span data-stu-id="e290c-240">Unlike either type of GDI ClearType rendering, sub-pixel ClearType offers the most accurate width of characters.</span></span>

<span data-ttu-id="e290c-241">A API de cadeia de caracteres de texto adota a renderização de texto sub-pixel por padrão, o que significa que ele mede o texto em sua resolução ideal, independentemente da resolução de vídeo atual, e produz o resultado de posicionamento de glifo com base nas larguras de adiantamento de glifos e deslocamentos de posicionamento verdadeiramente dimensionados.</span><span class="sxs-lookup"><span data-stu-id="e290c-241">The Text String API adopts sub-pixel text rendering by default, which means it measures text at its ideal resolution independent of the current display resolution, and produces the glyph positioning result based on the truly scaled glyph advance widths and positioning offsets.</span></span>

<span data-ttu-id="e290c-242">Para texto de tamanho grande, o [DirectWrite](direct-write-portal.md) também permite suavização de serrilhado ao longo do eixo y para tornar as bordas mais suaves e renderizar as letras como o designer de fonte pretendido.</span><span class="sxs-lookup"><span data-stu-id="e290c-242">For large-sized text, [DirectWrite](direct-write-portal.md) also enables anti-aliasing along the y-axis to make the edges smoother and render letters as the font designer intended.</span></span> <span data-ttu-id="e290c-243">A ilustração a seguir mostra a suavização de direção y.</span><span class="sxs-lookup"><span data-stu-id="e290c-243">The following illustration shows y-direction anti-aliasing.</span></span>

![ilustração de "ClearType" renderizado como texto GDI e como texto DirectWrite com anti-aliasing na direção y](images/intro-05.png)

<span data-ttu-id="e290c-245">Embora o texto [DirectWrite](direct-write-portal.md) seja posicionado e processado usando o ClearType de sub-pixel por padrão, outras opções de renderização estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e290c-245">Although [DirectWrite](direct-write-portal.md) text is positioned and rendered using sub-pixel ClearType by default, other rendering options are available.</span></span> <span data-ttu-id="e290c-246">Muitos aplicativos existentes usam o GDI para renderizar a maior parte de sua interface do usuário e alguns aplicativos usam controles de edição do sistema que continuam a usar o GDI para a renderização de texto.</span><span class="sxs-lookup"><span data-stu-id="e290c-246">Many existing applications use GDI to render most of their UI, and some applications use system editing controls that continue to use GDI for text rendering.</span></span> <span data-ttu-id="e290c-247">Ao adicionar texto DirectWrite a esses aplicativos, pode ser necessário sacrificar os aprimoramentos da experiência de leitura fornecidos pelo ClearType em subpixel para que o texto tenha uma aparência consistente em todo o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e290c-247">When adding DirectWrite text to these applications, it may be necessary to sacrifice the reading experience improvements provided by sub-pixel ClearType so that text has a consistent appearance across the application.</span></span>

<span data-ttu-id="e290c-248">Para atender a esses requisitos, o [DirectWrite](direct-write-portal.md) também dá suporte às seguintes opções de renderização:</span><span class="sxs-lookup"><span data-stu-id="e290c-248">To meet these requirements, [DirectWrite](direct-write-portal.md) also supports the following rendering options:</span></span>

-   <span data-ttu-id="e290c-249">ClearType de sub-pixel (padrão).</span><span class="sxs-lookup"><span data-stu-id="e290c-249">Sub-pixel ClearType (default).</span></span>
-   <span data-ttu-id="e290c-250">Subpixel ClearType com suavização de serrilhado nas dimensões horizontal e vertical.</span><span class="sxs-lookup"><span data-stu-id="e290c-250">Sub-pixel ClearType with anti-aliasing in both horizontal and vertical dimensions.</span></span>
-   <span data-ttu-id="e290c-251">Texto com alias.</span><span class="sxs-lookup"><span data-stu-id="e290c-251">Aliased text.</span></span>
-   <span data-ttu-id="e290c-252">Largura natural GDI (usada pelo Microsoft Word Modo de Exibição de Leitura, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="e290c-252">GDI natural-width (used by Microsoft Word Reading View, for example).</span></span>
-   <span data-ttu-id="e290c-253">Compatível com GDI-largura (incluindo bitmap do leste asiático Embedded).</span><span class="sxs-lookup"><span data-stu-id="e290c-253">GDI compatible-width (including East Asian embedded bitmap).</span></span>

<span data-ttu-id="e290c-254">Cada um desses modos de renderização pode ser ajustado por meio da API DirectWrite e do novo sintonizador ClearType da caixa de entrada do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e290c-254">Each of these rendering modes can be fine-tuned through the DirectWrite API and through the new Windows 7 inbox ClearType tuner.</span></span>

> [!Note]  
> <span data-ttu-id="e290c-255">A partir do Windows 8, você deve usar a suavização de texto em escala de cinza na maioria dos casos.</span><span class="sxs-lookup"><span data-stu-id="e290c-255">Starting with Windows 8, you should use greyscale text antialiasing in most cases.</span></span> <span data-ttu-id="e290c-256">Para obter mais informações, confira a próxima seção.</span><span class="sxs-lookup"><span data-stu-id="e290c-256">See the next section for more information.</span></span>

 

### <a name="support-for-natural-layout"></a><span data-ttu-id="e290c-257">Suporte para layout natural</span><span class="sxs-lookup"><span data-stu-id="e290c-257">Support for Natural Layout</span></span>

<span data-ttu-id="e290c-258">O layout natural é independente de resolução, portanto, o espaçamento de caracteres não muda à medida que você amplia ou reduz, ou dependendo do DPI da tela.</span><span class="sxs-lookup"><span data-stu-id="e290c-258">Natural layout is resolution-independent, so the spacing of characters doesn't change as you zoom in or out, or depending on the DPI of the display.</span></span> <span data-ttu-id="e290c-259">Uma vantagem secundária é que o espaçamento é verdadeiro para o design da fonte.</span><span class="sxs-lookup"><span data-stu-id="e290c-259">A secondary advantage is that spacing is true to the design of the font.</span></span> <span data-ttu-id="e290c-260">O layout natural é possibilitado pelo suporte do DirectWrite para a renderização natural, o que significa que os glifos individuais podem ser posicionados em uma fração de um pixel.</span><span class="sxs-lookup"><span data-stu-id="e290c-260">Natural layout is made possible by DirectWrite's support for natural rendering, which means individual glyphs can be positioned to a fraction of a pixel.</span></span>

<span data-ttu-id="e290c-261">Embora o layout natural seja o padrão, alguns aplicativos precisam renderizar texto com o mesmo espaçamento e aparência que o GDI.</span><span class="sxs-lookup"><span data-stu-id="e290c-261">While natural layout is the default, some applications need to render text with the same spacing and appearance as GDI.</span></span> <span data-ttu-id="e290c-262">Para tais aplicativos, o DirectWrite fornece modos de medição natural do GDI e GDI clássico e modos de renderização correspondentes.</span><span class="sxs-lookup"><span data-stu-id="e290c-262">For such applications, DirectWrite provides GDI classic and GDI natural measuring modes and corresponding rendering modes.</span></span>

<span data-ttu-id="e290c-263">Qualquer um dos modos de renderização acima pode ser combinado com um dos dois modos de suavização: ClearType ou tons de cinza.</span><span class="sxs-lookup"><span data-stu-id="e290c-263">Any of the above rendering modes can be combined with either of the two antialiasing modes: ClearType or grayscale.</span></span> <span data-ttu-id="e290c-264">As simulações de suavização ClearType têm uma resolução mais alta, manipulando individualmente os valores de cor vermelho, verde e azul de cada pixel.</span><span class="sxs-lookup"><span data-stu-id="e290c-264">ClearType antialiasing simulations a higher resolution by individually manipulating the red, green, and blue color values of each pixel.</span></span> <span data-ttu-id="e290c-265">A suavização de escala de cinza computa apenas um valor de cobertura (ou alfa) para cada pixel.</span><span class="sxs-lookup"><span data-stu-id="e290c-265">Grayscale antialiasing computes only one coverage (or alpha) value for each pixel.</span></span> <span data-ttu-id="e290c-266">ClearType é o padrão, mas a suavização de tons de cinza é recomendada para aplicativos da Windows Store porque é mais rápida e é compatível com anti-aliasing padrão, ainda sendo altamente legível.</span><span class="sxs-lookup"><span data-stu-id="e290c-266">ClearType is the default, but grayscale antialiasing is recommended for Windows Store apps because it is faster and is compatible with standard antialiasing, while still being highly readable.</span></span>

## <a name="api-overview"></a><span data-ttu-id="e290c-267">Visão geral da API</span><span class="sxs-lookup"><span data-stu-id="e290c-267">API Overview</span></span>

<span data-ttu-id="e290c-268">A interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) é o ponto de partida para usar a funcionalidade DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="e290c-268">The [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface is the starting point for using DirectWrite functionality.</span></span> <span data-ttu-id="e290c-269">A fábrica é o objeto raiz que cria um conjunto de objetos que podem ser usados juntos.</span><span class="sxs-lookup"><span data-stu-id="e290c-269">The factory is the root object that creates a set of objects that can be used together.</span></span>

<span data-ttu-id="e290c-270">A operação de formatação e layout é um pré-requisito para as operações, uma vez que o texto precisa ser formatado corretamente e disposto em um conjunto especificado de restrições antes que possa ser desenhado ou testado com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e290c-270">The formatting and layout operation is a prerequisite to the operations, as text needs to be properly formatted and laid out to a specified set of constraints before it can be drawn or hit-tested.</span></span> <span data-ttu-id="e290c-271">Dois objetos principais que você pode criar com um [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) para essa finalidade são [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="e290c-271">Two key objects that you can create with an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) for this purpose are [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="e290c-272">Um objeto **IDWriteTextFormat** representa as informações de formatação para um parágrafo de texto.</span><span class="sxs-lookup"><span data-stu-id="e290c-272">An **IDWriteTextFormat** object represents the formatting information for a paragraph of text.</span></span> <span data-ttu-id="e290c-273">A função [**IDWriteFactory:: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) usa a cadeia de caracteres de entrada, as restrições associadas, como a dimensão do espaço a ser preenchido e o objeto **IDWriteTextFormat** , e coloca o resultado totalmente analisado e formatado em **IDWriteTextLayout** para uso em operações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e290c-273">The [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) function takes the input string, the associated constraints such as the dimension of the space to be filled, and the **IDWriteTextFormat** object, and puts the fully analyzed and formatted result into **IDWriteTextLayout** to use in subsequent operations.</span></span>

<span data-ttu-id="e290c-274">O aplicativo pode renderizar o texto usando a função [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) fornecida pelo [Direct2D](../direct2d/direct2d-portal.md) ou implementando uma função de retorno de chamada que pode usar GDI, Direct2D ou outros sistemas gráficos para renderizar os glifos.</span><span class="sxs-lookup"><span data-stu-id="e290c-274">The application can then render the text using the [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) function provided by [Direct2D](../direct2d/direct2d-portal.md) or by implementing a callback function that can use GDI, Direct2D, or other graphics systems to render the glyphs.</span></span> <span data-ttu-id="e290c-275">Para um único texto de formato, a função [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) no Direct2D fornece uma maneira mais simples de desenhar texto sem precisar primeiro criar um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="e290c-275">For a single format text, the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function on Direct2D provides a simpler way to draw text without having to first create a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a><span data-ttu-id="e290c-276">Formatando e desenhando "Olá, Mundo" usando DirectWrite</span><span class="sxs-lookup"><span data-stu-id="e290c-276">Formatting and Drawing "Hello World" Using DirectWrite</span></span>

<span data-ttu-id="e290c-277">O exemplo de código a seguir mostra como um aplicativo pode formatar um único parágrafo usando [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e desenhá-lo usando a função [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="e290c-277">The following code example shows how an application can format a single paragraph using [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and draw it using the [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function.</span></span>


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a><span data-ttu-id="e290c-278">Acessando o sistema de fontes</span><span class="sxs-lookup"><span data-stu-id="e290c-278">Accessing the Font System</span></span>

<span data-ttu-id="e290c-279">Além de especificar um nome de família de fontes para a cadeia de caracteres de texto usando a interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) no exemplo acima, o [DirectWrite](direct-write-portal.md) fornece aos aplicativos mais controle sobre a seleção de fontes por meio da enumeração de fontes e a capacidade de criar uma coleção de fontes personalizada com base em fontes de documento inseridas.</span><span class="sxs-lookup"><span data-stu-id="e290c-279">In addition to specifying a font family name for the text string by using the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface in the example above, [DirectWrite](direct-write-portal.md) provides applications more control over font selection through font enumeration and the ability to create custom font collection based on embedded document fonts.</span></span>

<span data-ttu-id="e290c-280">O objeto [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) é uma coleção de famílias de fontes.</span><span class="sxs-lookup"><span data-stu-id="e290c-280">The [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) object is a collection of font families.</span></span> <span data-ttu-id="e290c-281">O DirectWrite fornece acesso ao conjunto de fontes instaladas no sistema por meio de uma coleção de fontes especial chamada coleção de fontes do sistema.</span><span class="sxs-lookup"><span data-stu-id="e290c-281">DirectWrite provides access to the set of fonts installed on the system through a special font collection called the system font collection.</span></span> <span data-ttu-id="e290c-282">Isso é obtido chamando o método [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) do objeto [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="e290c-282">This is obtained by calling the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) object.</span></span> <span data-ttu-id="e290c-283">Um aplicativo também pode criar uma coleção de fontes personalizada de um conjunto de fontes enumeradas por um retorno de chamada definido pelo aplicativo, ou seja, fontes privadas instaladas por um aplicativo ou fontes inseridas em um documento.</span><span class="sxs-lookup"><span data-stu-id="e290c-283">An application can also create a custom font collection from a set of fonts enumerated by an application-defined callback, that is, private fonts installed by an application, or fonts embedded in a document.</span></span>

<span data-ttu-id="e290c-284">O aplicativo pode chamar [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) para obter um objeto FontFamily específico dentro da coleção e, em seguida, chamar [**IDWriteFontFamily:: GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) para obter um objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) específico.</span><span class="sxs-lookup"><span data-stu-id="e290c-284">The application can then call [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) to get to a specific FontFamily object within the collection, and then call [**IDWriteFontFamily::GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) to get to a specific [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object.</span></span> <span data-ttu-id="e290c-285">O objeto **IDWriteFont** representa uma fonte em uma coleção de fontes e expõe propriedades e algumas métricas de fontes básicas.</span><span class="sxs-lookup"><span data-stu-id="e290c-285">The **IDWriteFont** object represents a font in a font collection and exposes properties and a few basic font metrics.</span></span>

<span data-ttu-id="e290c-286">O [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) é outro objeto que representa uma fonte e expõe um conjunto completo de métricas em uma fonte.</span><span class="sxs-lookup"><span data-stu-id="e290c-286">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) is another object that represents a font and exposes a full set of metrics on a font.</span></span> <span data-ttu-id="e290c-287">O **IDWriteFontFace** pode ser criado diretamente a partir de um nome de fonte; um aplicativo não precisa obter uma coleção de fontes para acessá-la.</span><span class="sxs-lookup"><span data-stu-id="e290c-287">The **IDWriteFontFace** can be created directly from a font name; an application does not have to get a font collection to access it.</span></span> <span data-ttu-id="e290c-288">É útil para um aplicativo de layout de texto, como o Microsoft Word, que precisa consultar os detalhes de uma fonte específica.</span><span class="sxs-lookup"><span data-stu-id="e290c-288">It is useful for a text layout application such as Microsoft Word that needs to query the details for a specific font.</span></span>

<span data-ttu-id="e290c-289">O diagrama a seguir ilustra a relação entre esses objetos.</span><span class="sxs-lookup"><span data-stu-id="e290c-289">The following diagram illustrates the relationship between these objects.</span></span>

![diagrama da relação entre uma coleção de fontes, uma família de fontes e um tipo de fonte](images/fontcollection.png)

### <a name="idwritefontface"></a><span data-ttu-id="e290c-291">IDWriteFontFace</span><span class="sxs-lookup"><span data-stu-id="e290c-291">IDWriteFontFace</span></span>

<span data-ttu-id="e290c-292">O objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) representa uma fonte e fornece informações mais detalhadas sobre a fonte do que o objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) .</span><span class="sxs-lookup"><span data-stu-id="e290c-292">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object represents a font and provides more detailed information about the font than the [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object does.</span></span> <span data-ttu-id="e290c-293">As métricas de fonte e glifo do **IDWriteFontFace** são úteis para aplicativos que implementam o layout de texto.</span><span class="sxs-lookup"><span data-stu-id="e290c-293">The font and glyph metrics from the **IDWriteFontFace** are useful for applications that implement text layout.</span></span>

<span data-ttu-id="e290c-294">A maioria dos aplicativos principais não usará essas APIs diretamente e, em vez disso, usará [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) ou especificará o nome da família de fontes diretamente.</span><span class="sxs-lookup"><span data-stu-id="e290c-294">Most mainstream applications will not use these APIs directly, and instead will use [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) or specify the font family name directly.</span></span>

<span data-ttu-id="e290c-295">A tabela a seguir resume os cenários de uso para os dois objetos.</span><span class="sxs-lookup"><span data-stu-id="e290c-295">The following table summarizes the usage scenarios for the two objects.</span></span>



| <span data-ttu-id="e290c-296">Categoria</span><span class="sxs-lookup"><span data-stu-id="e290c-296">Category</span></span>                                                                                                         | [<span data-ttu-id="e290c-297">**IDWriteFont**</span><span class="sxs-lookup"><span data-stu-id="e290c-297">**IDWriteFont**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [<span data-ttu-id="e290c-298">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="e290c-298">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="e290c-299">APIs para dar suporte à interação do usuário, como uma interface do usuário do seletor de fonte: Descrição e outras APIs informativas</span><span class="sxs-lookup"><span data-stu-id="e290c-299">APIs to support user interaction such as a font-chooser user interface: description and other informational APIs</span></span> | <span data-ttu-id="e290c-300">Sim</span><span class="sxs-lookup"><span data-stu-id="e290c-300">Yes</span></span>                                        | <span data-ttu-id="e290c-301">Não</span><span class="sxs-lookup"><span data-stu-id="e290c-301">No</span></span>                                                 |
| <span data-ttu-id="e290c-302">APIs para dar suporte ao mapeamento de fontes: família, estilo, peso, ampliação, cobertura de caracteres</span><span class="sxs-lookup"><span data-stu-id="e290c-302">APIs to support font mapping: family, style, weight, stretch, character coverage</span></span>                                 | <span data-ttu-id="e290c-303">Sim</span><span class="sxs-lookup"><span data-stu-id="e290c-303">Yes</span></span>                                        | <span data-ttu-id="e290c-304">Não</span><span class="sxs-lookup"><span data-stu-id="e290c-304">No</span></span>                                                 |
| <span data-ttu-id="e290c-305">API DrawText</span><span class="sxs-lookup"><span data-stu-id="e290c-305">DrawText API</span></span>                                                                                                     | <span data-ttu-id="e290c-306">Sim</span><span class="sxs-lookup"><span data-stu-id="e290c-306">Yes</span></span>                                        | <span data-ttu-id="e290c-307">Não</span><span class="sxs-lookup"><span data-stu-id="e290c-307">No</span></span>                                                 |
| <span data-ttu-id="e290c-308">APIs usadas para renderização</span><span class="sxs-lookup"><span data-stu-id="e290c-308">APIs used for rendering</span></span>                                                                                          | <span data-ttu-id="e290c-309">Não</span><span class="sxs-lookup"><span data-stu-id="e290c-309">No</span></span>                                         | <span data-ttu-id="e290c-310">Sim</span><span class="sxs-lookup"><span data-stu-id="e290c-310">Yes</span></span>                                                |
| <span data-ttu-id="e290c-311">APIs usadas para layout de texto: métricas de glifo e assim por diante</span><span class="sxs-lookup"><span data-stu-id="e290c-311">APIs used for text layout: glyph metrics, and so on</span></span>                                                              | <span data-ttu-id="e290c-312">Não</span><span class="sxs-lookup"><span data-stu-id="e290c-312">No</span></span>                                         | <span data-ttu-id="e290c-313">Sim</span><span class="sxs-lookup"><span data-stu-id="e290c-313">Yes</span></span>                                                |
| <span data-ttu-id="e290c-314">APIs para controle de interface do usuário e layout de texto: métricas de toda a fonte</span><span class="sxs-lookup"><span data-stu-id="e290c-314">APIs for UI control and text layout: font-wide metrics</span></span>                                                           | <span data-ttu-id="e290c-315">Sim</span><span class="sxs-lookup"><span data-stu-id="e290c-315">Yes</span></span>                                        | <span data-ttu-id="e290c-316">Sim</span><span class="sxs-lookup"><span data-stu-id="e290c-316">Yes</span></span>                                                |



 

<span data-ttu-id="e290c-317">Este é um aplicativo de exemplo que enumera as fontes na coleção de fontes do sistema.</span><span class="sxs-lookup"><span data-stu-id="e290c-317">The following is an example application that enumerates the fonts in the system font collection.</span></span>


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a><span data-ttu-id="e290c-318">Renderização de texto</span><span class="sxs-lookup"><span data-stu-id="e290c-318">Text rendering</span></span>

<span data-ttu-id="e290c-319">As APIs de renderização de texto permitem que os glifos em uma fonte [DirectWrite](direct-write-portal.md) sejam renderizados em uma superfície [Direct2D](../direct2d/direct2d-portal.md) ou em um bitmap independente de dispositivo GDI ou sejam convertidos em contornos ou bitmaps.</span><span class="sxs-lookup"><span data-stu-id="e290c-319">The text rendering APIs enable glyphs in a [DirectWrite](direct-write-portal.md) font to be rendered to a [Direct2D](../direct2d/direct2d-portal.md) surface or to a GDI device independent bitmap, or to be converted to outlines or bitmaps.</span></span> <span data-ttu-id="e290c-320">A renderização de ClearType no DirectWrite dá suporte ao posicionamento de subpixel com nitidez aprimorada e contraste em comparação com as implementações anteriores no Windows.</span><span class="sxs-lookup"><span data-stu-id="e290c-320">The ClearType rendering in DirectWrite supports sub-pixel positioning with improved sharpness and contrast compared to previous implementations on Windows.</span></span> <span data-ttu-id="e290c-321">O DirectWrite também dá suporte a texto em preto e branco com alias para dar suporte a cenários que envolvem fontes do leste asiático com bitmaps inseridos ou onde o usuário desabilitou a suavização de fontes de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="e290c-321">DirectWrite also supports aliased black-and-white text to support scenarios involving East Asian fonts with embedded bitmaps, or where the user has disabled font smoothing of any type.</span></span>

<span data-ttu-id="e290c-322">Todas as opções são ajustáveis por todos os botões de ClearType disponíveis acessíveis por meio das APIs do [DirectWrite](direct-write-portal.md) e também expostas por meio do novo miniaplicativo do painel de controle de sintonizador do Windows 7 ClearType.</span><span class="sxs-lookup"><span data-stu-id="e290c-322">All the options are adjustable by all the available ClearType knobs accessible through the [DirectWrite](direct-write-portal.md) APIs, and also exposed via the new Windows 7 ClearType tuner control panel applet.</span></span>

<span data-ttu-id="e290c-323">Há duas APIs disponíveis para renderizar glifos, uma fornecendo renderização acelerada por hardware por meio de [Direct2D](../direct2d/direct2d-portal.md) e a outra fornecendo renderização de software para um bitmap GDI.</span><span class="sxs-lookup"><span data-stu-id="e290c-323">There are two APIs available for rendering glyphs, one providing hardware-accelerated rendering through [Direct2D](../direct2d/direct2d-portal.md) and the other providing software rendering to a GDI bitmap.</span></span> <span data-ttu-id="e290c-324">Um aplicativo usando [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e implementando o retorno de chamada [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) pode chamar qualquer uma dessas funções em resposta a um retorno de chamada [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="e290c-324">An application using [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) and implementing the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) callback can call either of these functions in response to a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback.</span></span> <span data-ttu-id="e290c-325">Além disso, os aplicativos que implementam seu próprio layout ou lidam com dados em nível de glifo podem usar essas APIs.</span><span class="sxs-lookup"><span data-stu-id="e290c-325">Also, applications that implement their own layout or deal with glyph-level data can use these APIs.</span></span>

1.  [<span data-ttu-id="e290c-326">**ID2DRenderTarget::D rawGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="e290c-326">**ID2DRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    <span data-ttu-id="e290c-327">Os aplicativos podem usar a API do [Direct2D](../direct2d/direct2d-portal.md) [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) para fornecer aceleração de hardware para a renderização de texto usando a GPU.</span><span class="sxs-lookup"><span data-stu-id="e290c-327">Applications can use the [Direct2D](../direct2d/direct2d-portal.md) API [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) to provide hardware acceleration for text rendering using the GPU.</span></span> <span data-ttu-id="e290c-328">A aceleração de hardware afeta todas as fases do pipeline de renderização de texto — de Mesclar glifos em execuções de glifos e filtrar o bitmap de execução de glifos, para aplicar o algoritmo de mesclagem ClearType à saída final exibida.</span><span class="sxs-lookup"><span data-stu-id="e290c-328">Hardware acceleration affects all phases of the text rendering pipeline—from merging glyphs into glyph runs and filtering the glyph-run bitmap, to applying the ClearType blending algorithm to the final displayed output.</span></span> <span data-ttu-id="e290c-329">Essa é a API recomendada para obter o melhor desempenho de renderização.</span><span class="sxs-lookup"><span data-stu-id="e290c-329">This is the recommended API for getting the best rendering performance.</span></span>

2.  [<span data-ttu-id="e290c-330">**IDWriteBitmapRenderTarget::D rawGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="e290c-330">**IDWriteBitmapRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    <span data-ttu-id="e290c-331">Os aplicativos podem usar o método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para executar um processamento de software de uma execução de glifos em um bitmap 32-bpp.</span><span class="sxs-lookup"><span data-stu-id="e290c-331">Applications can use the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to perform a software-rendering of a run of glyphs to a 32-bpp bitmap.</span></span> <span data-ttu-id="e290c-332">O objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsula um bitmap e um contexto de dispositivo de memória que pode ser usado para renderizar glifos.</span><span class="sxs-lookup"><span data-stu-id="e290c-332">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object encapsulates a bitmap and a memory device context that can be used for rendering glyphs.</span></span> <span data-ttu-id="e290c-333">Essa API será útil se você quiser se manter com o GDI porque você tem uma base de código existente que é renderizada em GDI.</span><span class="sxs-lookup"><span data-stu-id="e290c-333">This API is useful if you want to stay with GDI because you have an existing code base that renders in GDI.</span></span>

<span data-ttu-id="e290c-334">Se você tiver um aplicativo que tenha código de layout de texto existente que usa GDI e desejar preservar seu código de layout existente, mas usar [DirectWrite](direct-write-portal.md) apenas para a etapa final de processamento de glifos, [**IDWriteGdiInterop:: CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) fornecerá a ponte entre as duas APIs.</span><span class="sxs-lookup"><span data-stu-id="e290c-334">If you have an application that has existing text layout code that uses GDI, and you want to preserve its existing layout code but use [DirectWrite](direct-write-portal.md) just for the final step of rendering glyphs, [**IDWriteGdiInterop::CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) provides the bridge between the two APIs.</span></span> <span data-ttu-id="e290c-335">Antes de chamar essa função, o aplicativo usará a função **IDWriteGdiInterop:: CreateFontFaceFromHdc** para obter uma referência de face de fonte de um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e290c-335">Before calling this function, the application will use the **IDWriteGdiInterop::CreateFontFaceFromHdc** function to get a font-face reference from a device context.</span></span>

> [!Note]  
> <span data-ttu-id="e290c-336">Na maioria dos cenários, os aplicativos podem não precisar usar essas APIs de renderização de glifo.</span><span class="sxs-lookup"><span data-stu-id="e290c-336">For most scenarios, applications may not need to use these glyph-rendering APIs.</span></span> <span data-ttu-id="e290c-337">Depois que um aplicativo cria um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , ele pode usar o método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) para renderizar o texto.</span><span class="sxs-lookup"><span data-stu-id="e290c-337">After an application has created an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, it can use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method to render the text.</span></span>

 

## <a name="custom-rendering-modes"></a><span data-ttu-id="e290c-338">Modos de renderização personalizados</span><span class="sxs-lookup"><span data-stu-id="e290c-338">Custom Rendering Modes</span></span>

<span data-ttu-id="e290c-339">Vários parâmetros afetam A renderização de texto, como gama, nível de ClearType, geometria de pixel e contraste aprimorado.</span><span class="sxs-lookup"><span data-stu-id="e290c-339">A number of parameters affect text rendering, such as gamma, ClearType level, pixel geometry, and enhanced contrast.</span></span> <span data-ttu-id="e290c-340">Os parâmetros de renderização são encapsulados por um objeto, que implementa a interface [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) pública.</span><span class="sxs-lookup"><span data-stu-id="e290c-340">Rendering parameters are encapsulated by an object, which implements the public [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) interface.</span></span> <span data-ttu-id="e290c-341">O objeto de parâmetros de renderização é inicializado automaticamente com base nas propriedades de hardware e/ou nas preferências do usuário especificadas por meio do miniaplicativo do painel de controle ClearType no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e290c-341">The rendering parameters object is automatically initialized based on hardware properties and/or user preferences specified through the ClearType control panel applet in Windows 7.</span></span> <span data-ttu-id="e290c-342">Em geral, se um cliente usar a API de layout [DirectWrite](direct-write-portal.md) , o DirectWrite selecionará automaticamente um modo de renderização que corresponda ao modo de medição especificado.</span><span class="sxs-lookup"><span data-stu-id="e290c-342">Generally, if a client uses the [DirectWrite](direct-write-portal.md) layout API, DirectWrite will automatically select a rendering mode that corresponds to the specified measuring mode.</span></span>

<span data-ttu-id="e290c-343">Os aplicativos que desejam mais controle podem usar [**IDWriteFactory:: CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) para implementar as diferentes opções de renderização.</span><span class="sxs-lookup"><span data-stu-id="e290c-343">Applications that want more control can use [**IDWriteFactory::CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) to implement the different rendering options.</span></span> <span data-ttu-id="e290c-344">Essa função também pode ser usada para definir o gama, a geometria de pixel e o contraste avançado.</span><span class="sxs-lookup"><span data-stu-id="e290c-344">This function can also be used to set the gamma, pixel geometry, and enhanced contrast.</span></span>

<span data-ttu-id="e290c-345">A seguir estão as várias opções de renderização disponíveis:</span><span class="sxs-lookup"><span data-stu-id="e290c-345">The following are the various rendering options available:</span></span>

-   <span data-ttu-id="e290c-346">Suavização de subconjunto de pixel</span><span class="sxs-lookup"><span data-stu-id="e290c-346">Sub-pixel anti-aliasing</span></span>

    <span data-ttu-id="e290c-347">O aplicativo define o parâmetro *RenderingMode* para o \_ modo de renderização DWRITE \_ \_ natural para especificar o processamento com suavização de serrilhado somente na dimensão horizontal.</span><span class="sxs-lookup"><span data-stu-id="e290c-347">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL to specify rendering with anti-aliasing in the horizontal dimension only.</span></span>

-   <span data-ttu-id="e290c-348">Suavização de subconjuntos de subpixel nas dimensões horizontal e vertical.</span><span class="sxs-lookup"><span data-stu-id="e290c-348">Sub-pixel anti-aliasing in both horizontal and vertical dimensions.</span></span>

    <span data-ttu-id="e290c-349">O aplicativo define o parâmetro *RenderingMode* para o \_ modo de renderização DWRITE \_ \_ \_ simétrico natural para especificar a renderização com suavização de serrilhado nas dimensões horizontal e vertical.</span><span class="sxs-lookup"><span data-stu-id="e290c-349">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL\_SYMMETRIC to specify rendering with anti-aliasing in both horizontal and vertical dimensions.</span></span> <span data-ttu-id="e290c-350">Isso faz com que as curvas e as linhas diagonais pareçam mais suaves às custas de alguma suavidade e normalmente são usadas em tamanhos acima de 16 ppem.</span><span class="sxs-lookup"><span data-stu-id="e290c-350">This makes curves and diagonal lines look smoother at the expense of some softness, and is typically used at sizes above 16 ppem.</span></span>

-   <span data-ttu-id="e290c-351">Texto com alias</span><span class="sxs-lookup"><span data-stu-id="e290c-351">Aliased Text</span></span>

    <span data-ttu-id="e290c-352">O aplicativo define o parâmetro *RenderingMode* para o \_ modo de renderização DWRITE \_ \_ com alias para especificar o texto com alias.</span><span class="sxs-lookup"><span data-stu-id="e290c-352">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_ALIASED to specify aliased text.</span></span>

-   <span data-ttu-id="e290c-353">Texto em escala de cinza</span><span class="sxs-lookup"><span data-stu-id="e290c-353">Grayscale Text</span></span>

    <span data-ttu-id="e290c-354">O aplicativo define o parâmetro *pixelGeometry* como DWRITE de \_ geometria de pixel \_ \_ plano para especificar texto em escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="e290c-354">The application sets the *pixelGeometry* parameter to DWRITE\_PIXEL\_GEOMETRY\_FLAT to specify grayscale text.</span></span>

-   <span data-ttu-id="e290c-355">Compatível com GDI-largura (incluindo bitmap do leste asiático Embedded)</span><span class="sxs-lookup"><span data-stu-id="e290c-355">GDI compatible-width (including East Asian embedded bitmap)</span></span>

    <span data-ttu-id="e290c-356">O aplicativo define o parâmetro *RenderingMode* para o \_ modo de renderização DWRITE \_ \_ GDI \_ clássico para especificar a suavização de largura compatível com GDI.</span><span class="sxs-lookup"><span data-stu-id="e290c-356">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC to specify GDI compatible-width anti-aliasing.</span></span>

-   <span data-ttu-id="e290c-357">Largura natural GDI</span><span class="sxs-lookup"><span data-stu-id="e290c-357">GDI natural-width</span></span>

    <span data-ttu-id="e290c-358">O aplicativo define o parâmetro *RenderingMode* para o \_ modo de renderização DWRITE \_ \_ GDI \_ natural para especificar a suavização de serrilhado compatível com a largura natural do GDI.</span><span class="sxs-lookup"><span data-stu-id="e290c-358">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_NATURAL to specify GDI natural-width compatible anti-aliasing.</span></span>

-   <span data-ttu-id="e290c-359">Texto de contorno</span><span class="sxs-lookup"><span data-stu-id="e290c-359">Outline text</span></span>

    <span data-ttu-id="e290c-360">Para renderização em tamanhos grandes, um desenvolvedor de aplicativos pode preferir renderizar usando a estrutura de tópicos da fonte em vez de rasterizar em um bitmap.</span><span class="sxs-lookup"><span data-stu-id="e290c-360">For rendering at large sizes, an application developer might prefer to render by using the font outline rather than by rasterizing into a bitmap.</span></span> <span data-ttu-id="e290c-361">O aplicativo define o parâmetro *RenderingMode* para **a \_ estrutura \_ de \_ Tópicos do modo de renderização DWRITE** para especificar que a renderização deve ignorar o rasterizador e usar os contornos diretamente.</span><span class="sxs-lookup"><span data-stu-id="e290c-361">The application sets the *renderingMode* parameter to **DWRITE\_RENDERING\_MODE\_OUTLINE** to specify that rendering should bypass the rasterizer and use the outlines directly.</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="e290c-362">Interoperabilidade GDI</span><span class="sxs-lookup"><span data-stu-id="e290c-362">GDI Interoperability</span></span>

<span data-ttu-id="e290c-363">A interface [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) fornece interoperabilidade com GDI.</span><span class="sxs-lookup"><span data-stu-id="e290c-363">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface provides interoperability with GDI.</span></span> <span data-ttu-id="e290c-364">Isso permite que os aplicativos continuem seus investimentos existentes em bases de código GDI e usem seletivamente o [DirectWrite](direct-write-portal.md) para renderização ou layout.</span><span class="sxs-lookup"><span data-stu-id="e290c-364">This enables applications to continue their existing investment in GDI code bases and selectively use [DirectWrite](direct-write-portal.md) for either rendering or layout.</span></span>

<span data-ttu-id="e290c-365">A seguir estão as APIs que permitem que um aplicativo migre para ou do sistema de fontes GDI:</span><span class="sxs-lookup"><span data-stu-id="e290c-365">The following are the APIs that enable an application to migrate to or from the GDI font system:</span></span>

-   [<span data-ttu-id="e290c-366">**CreateFontFromLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="e290c-366">**CreateFontFromLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    <span data-ttu-id="e290c-367">Cria um objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) que corresponde às propriedades especificadas pela estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="e290c-367">Creates an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object that matches the properties specified by the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

-   [<span data-ttu-id="e290c-368">**ConvertFontToLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="e290c-368">**ConvertFontToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    <span data-ttu-id="e290c-369">Inicializa uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) com base nas propriedades compatíveis com GDI do [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)especificado.</span><span class="sxs-lookup"><span data-stu-id="e290c-369">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont).</span></span>

-   [<span data-ttu-id="e290c-370">**ConvertFontFaceToLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="e290c-370">**ConvertFontFaceToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    <span data-ttu-id="e290c-371">Inicializa uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) com base nas propriedades compatíveis com GDI do [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)especificado.</span><span class="sxs-lookup"><span data-stu-id="e290c-371">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface).</span></span>

-   [<span data-ttu-id="e290c-372">**CreateFontFaceFromHdc**</span><span class="sxs-lookup"><span data-stu-id="e290c-372">**CreateFontFaceFromHdc**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    <span data-ttu-id="e290c-373">Cria um objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) que corresponde ao **HFONT** selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="e290c-373">Creates an [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object that corresponds to the currently selected **HFONT**.</span></span>

## <a name="conclusion"></a><span data-ttu-id="e290c-374">Conclusão</span><span class="sxs-lookup"><span data-stu-id="e290c-374">Conclusion</span></span>

<span data-ttu-id="e290c-375">Melhorar a experiência de leitura é de grande valor para os usuários, seja na tela ou em papel.</span><span class="sxs-lookup"><span data-stu-id="e290c-375">Improving the reading experience is of great value to users whether it is on the screen or on paper.</span></span> <span data-ttu-id="e290c-376">O [DirectWrite](direct-write-portal.md) fornece a facilidade de uso e o modelo de programação em camadas para que os desenvolvedores de aplicativos aprimorem a experiência de texto para seus aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="e290c-376">[DirectWrite](direct-write-portal.md) provides the ease of use and the layered programming model for application developers to improve the text experience for their Windows applications.</span></span> <span data-ttu-id="e290c-377">Os aplicativos podem usar DirectWrite para renderizar texto formatado de formato rico para sua interface do usuário e documentos com a API de layout.</span><span class="sxs-lookup"><span data-stu-id="e290c-377">Applications can use DirectWrite to render richly formatted text for their UI and documents with the layout API.</span></span> <span data-ttu-id="e290c-378">Para cenários mais complexos, um aplicativo pode trabalhar diretamente com glifos, fontes de acesso e assim por diante e aproveitar a potência do DirectWrite para fornecer uma tipografia de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="e290c-378">For more complex scenarios, an application can work directly with glyphs, access fonts, and so on, and harness the power of DirectWrite to deliver high-quality typography.</span></span>

<span data-ttu-id="e290c-379">Os recursos de interoperabilidade do [DirectWrite](direct-write-portal.md) permitem que os desenvolvedores de aplicativos encaminhem suas bases de código Win32 existentes e adotem DirectWrite seletivamente dentro de seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e290c-379">The interoperability capabilities of [DirectWrite](direct-write-portal.md) enable application developers to carry forward their existing Win32 codebases and adopt DirectWrite selectively within their applications.</span></span>

 

 