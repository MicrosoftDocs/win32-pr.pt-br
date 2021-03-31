---
title: Perguntas frequentes sobre a VML
description: Perguntas frequentes sobre a VML
ms.assetid: f7f2ce12-facf-4042-b2a7-acaa3e25816a
keywords:
- Linguagem VML (VML), perguntas frequentes
- VML (linguagem VML), perguntas frequentes
- gráficos vetoriais, perguntas frequentes
- Linguagem VML (VML), perguntas frequentes
- VML (linguagem VML), perguntas frequentes
- gráficos vetoriais, perguntas frequentes
- Linguagem VML (VML), diferenças de GIF
- VML (linguagem VML), diferenças de GIF
- Linguagem VML (VML), diferenças de PNG
- VML (linguagem VML), diferenças de PNG
- gráficos vetoriais, diferenças de formato de rasterização
- Linguagem VML (VML), XML
- VML (linguagem VML), XML
- gráficos vetoriais, XML
- Linguagem VML (VML), animação
- VML (linguagem VML), animação
- gráficos vetoriais, animação
- Linguagem VML (VML), Macromedia Flash
- VML (linguagem VML), Macromedia Flash
- gráficos vetoriais, Macromedia Flash
- formatos de rasterização
- animação
- Flash da Macromedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e108f2055e7a0fbae1c5ed542fe68c59ec9b212b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917518"
---
# <a name="frequently-asked-questions-about-vml"></a><span data-ttu-id="36635-126">Perguntas frequentes sobre a VML</span><span class="sxs-lookup"><span data-stu-id="36635-126">Frequently Asked Questions About VML</span></span>

<span data-ttu-id="36635-127">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="36635-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="36635-128">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="36635-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="36635-129">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="36635-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="36635-130">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="36635-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="36635-131">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="36635-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="36635-132">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="36635-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="does-vml-compete-with-gif-and-png"></a><span data-ttu-id="36635-133">A VML é concorrente com GIF e PNG?</span><span class="sxs-lookup"><span data-stu-id="36635-133">Does VML compete with GIF and PNG?</span></span>

<span data-ttu-id="36635-134">Não.</span><span class="sxs-lookup"><span data-stu-id="36635-134">No.</span></span> <span data-ttu-id="36635-135">GIF e PNG são formatos rasterizados (ou mapeados por bits) que podem ser usados para armazenar gráficos vetoriais.</span><span class="sxs-lookup"><span data-stu-id="36635-135">Both GIF and PNG are raster (or bit-mapped) formats that can be used to store vector graphics.</span></span> <span data-ttu-id="36635-136">Os formatos de varredura armazenam cada pixel, enquanto que os formatos de vetor, como VML, usam descrições matemáticas ou contornos para descrever os gráficos.</span><span class="sxs-lookup"><span data-stu-id="36635-136">Raster formats store every pixel, whereas vector formats such as VML use mathematical descriptions or outlines to describe the graphics.</span></span> <span data-ttu-id="36635-137">Os gráficos vetoriais armazenados em um formato baseado em vetor são mais compactados do que aqueles armazenados em formatos de varredura, resultando em tempos de download mais rápidos para usuários da Web.</span><span class="sxs-lookup"><span data-stu-id="36635-137">Vector graphics stored in a vector-based format are more compact than those stored in raster formats, resulting in faster download times for Web users.</span></span>

<span data-ttu-id="36635-138">Além disso, os elementos gráficos VML são entregues embutidos na página HTML em vez de depender de arquivos externos, como é o caso com GIF e PNG hoje.</span><span class="sxs-lookup"><span data-stu-id="36635-138">In addition, VML graphics are delivered inline to the HTML page rather than relying on external files, as is the case with GIF and PNG today.</span></span> <span data-ttu-id="36635-139">Isso permite que elementos gráficos VML sejam dimensionados e interajam com outros elementos da página da Web à medida que a página é redimensionada, melhorando assim a experiência do usuário final.</span><span class="sxs-lookup"><span data-stu-id="36635-139">This allows VML graphics to scale and interact with other Web page elements as the page is resized, thus improving the end-user experience.</span></span>

<span data-ttu-id="36635-140">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="36635-140">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="why-is-microsoft-supporting-another-xml-based-standard-when-xml-is-hardly-in-use-and-is-young-enough-as-it-is"></a><span data-ttu-id="36635-141">Por que a Microsoft dá suporte a outro padrão baseado em XML quando o XML dificilmente está em uso e é jovem o suficiente como é?</span><span class="sxs-lookup"><span data-stu-id="36635-141">Why is Microsoft supporting another XML-based standard when XML is hardly in use and is young enough as it is?</span></span>

<span data-ttu-id="36635-142">O XML é uma maneira poderosa, mas simples, de representar dados estruturados na Web e complementa totalmente o HTML para exibição.</span><span class="sxs-lookup"><span data-stu-id="36635-142">XML is a powerful yet simple way to represent structured data on the Web, and fully complements HTML for display.</span></span> <span data-ttu-id="36635-143">A VML é um exemplo dos muitos formatos baseados em XML, específicos do aplicativo que serão desenvolvidos e implementados nos próximos meses.</span><span class="sxs-lookup"><span data-stu-id="36635-143">VML is one example of the many application-specific, XML-based formats that will be developed and implemented in the coming months.</span></span> <span data-ttu-id="36635-144">Por exemplo, na próxima versão do Office, a VML será usada para anotar documentos HTML – para preservar as informações de formatação dos gráficos de arte do Office entre o formato de arquivo nativo do Office e o HTML, permitindo que os usuários do Office alternem diretamente entre os dois formatos.</span><span class="sxs-lookup"><span data-stu-id="36635-144">For instance, in the next version of Office, VML will be used to annotate HTML documents -- to preserve formatting information of Office Art graphics between the native Office file format and HTML, thus enabling Office users to switch seamlessly between the two formats.</span></span>

<span data-ttu-id="36635-145">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="36635-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="who-will-support-vml"></a><span data-ttu-id="36635-146">Quem dará suporte a VML?</span><span class="sxs-lookup"><span data-stu-id="36635-146">Who will support VML?</span></span>

<span data-ttu-id="36635-147">Esperamos que muitos fornecedores ofereçam suporte a VML.</span><span class="sxs-lookup"><span data-stu-id="36635-147">We expect many vendors to support VML.</span></span> <span data-ttu-id="36635-148">Por exemplo, Autodesk, Hewlett-Packard, Macromedia e VISIO têm suporte de VML em versões futuras de seus produtos.</span><span class="sxs-lookup"><span data-stu-id="36635-148">For example, Autodesk, Hewlett-Packard, Macromedia, and VISIO have pledged support for VML in future versions of their products.</span></span> <span data-ttu-id="36635-149">A Microsoft penhorou o suporte para VML em versões futuras de suas plataformas, como o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="36635-149">Microsoft has pledged support for VML in future versions of its platforms such as Internet Explorer.</span></span> <span data-ttu-id="36635-150">Além disso, o VML será usado na próxima geração do Office para habilitar "ida e volta" entre o formato do Office e o HTML.</span><span class="sxs-lookup"><span data-stu-id="36635-150">In addition, VML will be used in the next generation of Office to enable "round-tripping" between the Office format and HTML.</span></span>

<span data-ttu-id="36635-151">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="36635-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-support-animation"></a><span data-ttu-id="36635-152">A VML dá suporte à animação?</span><span class="sxs-lookup"><span data-stu-id="36635-152">Does VML support animation?</span></span>

<span data-ttu-id="36635-153">Não, atualmente não.</span><span class="sxs-lookup"><span data-stu-id="36635-153">No, it currently doesn't.</span></span> <span data-ttu-id="36635-154">No entanto, estamos trabalhando com nossos parceiros de VML para adicionar capacidade de animação no formato VML.</span><span class="sxs-lookup"><span data-stu-id="36635-154">However, we are working with our VML partners to add animation capability into the VML format.</span></span> <span data-ttu-id="36635-155">Como a VML é baseada em XML, o conjunto de marcas pode ser facilmente estendido para funcionalidade adicional.</span><span class="sxs-lookup"><span data-stu-id="36635-155">Since VML is based on XML, the tag set can be easily extended for additional functionality.</span></span>

<span data-ttu-id="36635-156">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="36635-156">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-replace-macromedia-flash-didnt-macromedia-just-submit-their-flash-format-for-vector-graphics-to-the-w3c"></a><span data-ttu-id="36635-157">A VML substitui o Macromedia Flash?</span><span class="sxs-lookup"><span data-stu-id="36635-157">Does VML replace Macromedia Flash?</span></span> <span data-ttu-id="36635-158">Não a Macromedia não enviasse apenas seu formato Flash para gráficos vetoriais para o W3C?</span><span class="sxs-lookup"><span data-stu-id="36635-158">Didn't Macromedia just submit their Flash format for vector graphics to the W3C?</span></span>

<span data-ttu-id="36635-159">Não.</span><span class="sxs-lookup"><span data-stu-id="36635-159">No.</span></span> <span data-ttu-id="36635-160">A VML é um formato de entrega e distribuição baseado em texto para gráficos vetoriais, enquanto o flash é um formato binário para a entrega de gráficos e animações baseados em vetores.</span><span class="sxs-lookup"><span data-stu-id="36635-160">VML is a text-based interchange and delivery format for vector graphics, whereas Flash is a binary format for the delivery of vector-based graphics and animation.</span></span>

<span data-ttu-id="36635-161">A Macromedia não enviou seu formato de arquivo para o W3C.</span><span class="sxs-lookup"><span data-stu-id="36635-161">Macromedia did not submit their file format to the W3C.</span></span> <span data-ttu-id="36635-162">No entanto, eles abriram seu formato de arquivo para desenvolvedores de aplicativos, desenvolvedores da Web e usuários finais.</span><span class="sxs-lookup"><span data-stu-id="36635-162">However, they did open their file format up for application developers, Web developers and end users.</span></span> <span data-ttu-id="36635-163">Consulte <https://www.macromedia.com> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="36635-163">See <https://www.macromedia.com> for more information.</span></span>

[<span data-ttu-id="36635-164">Voltar para a visão geral da VML</span><span class="sxs-lookup"><span data-stu-id="36635-164">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

 