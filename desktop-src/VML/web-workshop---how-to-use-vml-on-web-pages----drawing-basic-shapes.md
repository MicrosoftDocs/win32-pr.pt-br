---
title: Formas básicas de desenho
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Web Workshop, formas de desenho
- Criando páginas da Web, formas de desenho
- Linguagem VML (VML), desenhar formas
- VML (linguagem VML), formas de desenho
- gráficos vetoriais, formas de desenho
- desenhando formas
- Formas de VML, desenho
- Linguagem VML (VML), XML
- VML (linguagem VML), XML
- gráficos vetoriais, XML
- Linguagem VML (VML), CSS2
- VML (linguagem VML), CSS2
- gráficos vetoriais, CSS2
- Linguagem VML (VML), elementos
- VML (linguagem VML), elementos
- gráficos vetoriais, elementos
- Elementos de VML, formas de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ab25fc9310750c9f49c5978a063c76639ec4bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454288"
---
# <a name="drawing-basic-shapes"></a><span data-ttu-id="3dd42-121">Formas básicas de desenho</span><span class="sxs-lookup"><span data-stu-id="3dd42-121">Drawing Basic Shapes</span></span>

<span data-ttu-id="3dd42-122">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3dd42-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3dd42-123">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="3dd42-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3dd42-124">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="3dd42-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3dd42-125">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="3dd42-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3dd42-126">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3dd42-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3dd42-127">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3dd42-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3dd42-128">Neste tópico, Ilustraremos como é fácil desenhar uma forma usando a VML.</span><span class="sxs-lookup"><span data-stu-id="3dd42-128">In this topic, we will illustrate how easy it is to draw a shape using VML.</span></span>

<span data-ttu-id="3dd42-129">Para criar uma elipse vermelha em uma página da Web, conforme mostrado na imagem a seguir, você pode desenhar a elipse usando uma ferramenta de edição gráfica, salvar o desenho como um bitmap e, em seguida, inserir o bitmap em sua página da Web:</span><span class="sxs-lookup"><span data-stu-id="3dd42-129">To create a red oval on a Web page, as shown in the following picture, you can draw the oval by using a graphic edit tool, save your drawing as a bitmap, and then insert the bitmap on your Web page:</span></span>

![oval1.gif (627 bytes)](images/oval1.gif)

<span data-ttu-id="3dd42-131">Como alternativa, você pode usar a VML para desenhar gráficos.</span><span class="sxs-lookup"><span data-stu-id="3dd42-131">Alternatively, you can use VML to draw graphics.</span></span> <span data-ttu-id="3dd42-132">No exemplo anterior, você pode digitar as seguintes linhas na `<BODY>` região da página da Web para desenhar a elipse vermelha:</span><span class="sxs-lookup"><span data-stu-id="3dd42-132">In the preceding example, you can type the following lines in the `<BODY>` region of your Web page to draw the red oval:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





<span data-ttu-id="3dd42-133">`<v:...>` e `</v:...>` são a marca de início e a marca de fim na [sintaxe XML](#xml-structure).`style='width:100pt; height:75pt'`</span><span class="sxs-lookup"><span data-stu-id="3dd42-133">`<v:...>` and `</v:...>` are the start tag and end tag in [XML syntax](#xml-structure).`style='width:100pt; height:75pt'`</span></span> <span data-ttu-id="3dd42-134">fornece [informações de CSS](#css-information).</span><span class="sxs-lookup"><span data-stu-id="3dd42-134">provides [CSS information](#css-information).</span></span> <span data-ttu-id="3dd42-135">**oval** e **FillColor**= "vermelho" são [elementos de VML](#vml-elements).</span><span class="sxs-lookup"><span data-stu-id="3dd42-135">**oval** and **fillcolor**="red" are [VML elements](#vml-elements).</span></span>

<span data-ttu-id="3dd42-136">Você pode alterar os elementos gráficos simplesmente alterando seus atributos de propriedade em VML.</span><span class="sxs-lookup"><span data-stu-id="3dd42-136">You can alter the graphics by simply changing their property attributes in VML.</span></span> <span data-ttu-id="3dd42-137">No exemplo anterior, se você alterar `fillcolor="red"` para `fillcolor="blue"` , conforme mostrado na representação de VML a seguir, a elipse vermelha será alterada para azul:</span><span class="sxs-lookup"><span data-stu-id="3dd42-137">In the preceding example, if you change `fillcolor="red"` to `fillcolor="blue"`, as shown in the following VML representation, the red oval will change to blue:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





<span data-ttu-id="3dd42-138">Os navegadores que oferecem suporte a VML podem renderizar e exibir os gráficos representados em VML sem precisar baixar arquivos de imagem separados.</span><span class="sxs-lookup"><span data-stu-id="3dd42-138">Browsers that support VML can render and display the graphics represented in VML without having to download separate image files.</span></span> <span data-ttu-id="3dd42-139">A maioria dos gráficos representados em VML é renderizada mais rapidamente em navegadores e requer menos espaço em disco e tempo de download.</span><span class="sxs-lookup"><span data-stu-id="3dd42-139">Most graphics represented in VML are rendered faster in browsers, and require less disk space and download time.</span></span>

<span data-ttu-id="3dd42-140">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="3dd42-140">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="xml-structure"></a><span data-ttu-id="3dd42-141">Estrutura XML</span><span class="sxs-lookup"><span data-stu-id="3dd42-141">XML Structure</span></span>

<span data-ttu-id="3dd42-142">A VML é formatada de acordo com as regras de linguagem XML (XML).</span><span class="sxs-lookup"><span data-stu-id="3dd42-142">VML is formatted according to the rules of Extensible Markup Language (XML).</span></span> <span data-ttu-id="3dd42-143">Qualquer analisador XML padrão pode analisar a VML e entregar os dados resultantes a um processador específico da VML.</span><span class="sxs-lookup"><span data-stu-id="3dd42-143">Any standard XML parser can parse VML and hand off the resulting data to a VML-specific processor.</span></span> <span data-ttu-id="3dd42-144">Para permitir que os navegadores saibam como entregar os dados a um processador específico da VML, você precisa digitar algumas informações, como [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) e [objetos personalizados incorporados](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span><span class="sxs-lookup"><span data-stu-id="3dd42-144">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) and [embedded custom objects](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span></span> <span data-ttu-id="3dd42-145">Em seguida, você pode usar a VML para digitar elementos gráficos na `<BODY>` região, assim como fazia no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="3dd42-145">You can then use VML to type graphics in the `<BODY>` region just as you did in the preceding example.</span></span>

<span data-ttu-id="3dd42-146">O `"v:"` prefixo em cada marca XML identifica a marca como VML.</span><span class="sxs-lookup"><span data-stu-id="3dd42-146">The `"v:"` prefix on each XML tag identifies the tag as VML.</span></span> <span data-ttu-id="3dd42-147">O `"v:"` prefixo na `<BODY>` região deve ser consistente com `<html xmlns:v="...">` .</span><span class="sxs-lookup"><span data-stu-id="3dd42-147">The `"v:"` prefix in the `<BODY>` region should be consistent with `<html xmlns:v="...">`.</span></span>

<span data-ttu-id="3dd42-148">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="3dd42-148">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="css-information"></a><span data-ttu-id="3dd42-149">Informações de CSS</span><span class="sxs-lookup"><span data-stu-id="3dd42-149">CSS Information</span></span>

<span data-ttu-id="3dd42-150">A VML usa [folhas de estilos em cascata, nível 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) para determinar o tamanho dos gráficos e para posicionar os gráficos em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="3dd42-150">VML uses [Cascading Style Sheets, Level 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) to determine the size of the graphics and to position the graphics on a Web page.</span></span> <span data-ttu-id="3dd42-151">No exemplo anterior, especificamos o tamanho da oval como 100 pontos (largura) por 75 pontos (altura) ( `style='width:100pt;height:75pt'` ).</span><span class="sxs-lookup"><span data-stu-id="3dd42-151">In the preceding example, we specified the size of the oval as 100 points (width) by 75 points (height) (`style='width:100pt;height:75pt'` ).</span></span>

<span data-ttu-id="3dd42-152">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="3dd42-152">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vml-elements"></a><span data-ttu-id="3dd42-153">Elementos VML</span><span class="sxs-lookup"><span data-stu-id="3dd42-153">VML Elements</span></span>

<span data-ttu-id="3dd42-154">No exemplo anterior, usamos um elemento predefinido VML `<oval>` para desenhar uma oval.</span><span class="sxs-lookup"><span data-stu-id="3dd42-154">In the preceding example, we used a VML predefined `<oval>` element to draw an oval.</span></span> <span data-ttu-id="3dd42-155">Em seguida, usamos o atributo da propriedade **FillColor** do `<oval>` elemento para preencher a oval com vermelho.</span><span class="sxs-lookup"><span data-stu-id="3dd42-155">We then used the **fillcolor** property attribute of the `<oval>` element to fill the oval with red.</span></span>

<span data-ttu-id="3dd42-156">Com base nas [marcas de início, marcas de fim e Empty-Element](https://www.w3.org/TR/REC-xml#sec-starttags) seção de marcas da [especificação XML 1,0](https://www.w3.org/TR/REC-xml), as marcas de elemento vazio podem ser usadas para qualquer elemento que não tenha conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3dd42-156">Based upon the [Start-Tags, End-Tags, and Empty-Element Tags](https://www.w3.org/TR/REC-xml#sec-starttags) section of [XML 1.0 specification](https://www.w3.org/TR/REC-xml), empty-element tags may be used for any element that has no content.</span></span> <span data-ttu-id="3dd42-157">Por exemplo, conforme mostrado na representação de VML a seguir, não há nenhum conteúdo (subelemento) dentro do `<oval>` elemento.</span><span class="sxs-lookup"><span data-stu-id="3dd42-157">For example, as shown in the following VML representation, there is no content (sub-element) within the `<oval>` element.</span></span> <span data-ttu-id="3dd42-158">(Observe que **Style** e **FillColor** são os atributos do `<oval>` elemento; eles não são subelementos.)</span><span class="sxs-lookup"><span data-stu-id="3dd42-158">(Note that the **style** and **fillcolor** are the attributes of the `<oval>` element; they are not sub-elements.)</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



<span data-ttu-id="3dd42-159">Portanto, você pode usar a marca de elemento vazio, conforme mostrado na representação de VML a seguir, para representar a mesma coisa que a linha acima.</span><span class="sxs-lookup"><span data-stu-id="3dd42-159">Therefore, you can use the empty-element tag, as shown in the following VML representation, to represent the same thing as the above line.</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



<span data-ttu-id="3dd42-160">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="3dd42-160">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="3dd42-161">Resumo</span><span class="sxs-lookup"><span data-stu-id="3dd42-161">Summary</span></span>

<span data-ttu-id="3dd42-162">Você pode usar a VML para desenhar gráficos em uma página da Web e, em seguida, personalizar esses gráficos simplesmente alterando seus atributos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="3dd42-162">You can use VML to draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span> <span data-ttu-id="3dd42-163">Além disso, a maioria dos gráficos representados em VML é renderizada mais rapidamente em navegadores e leva menos tempo para download e espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="3dd42-163">Also, most graphics represented in VML are rendered faster in browsers, and take less download time and disk space.</span></span>

 

 