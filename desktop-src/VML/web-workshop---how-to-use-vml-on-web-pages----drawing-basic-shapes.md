---
title: Desenhando formas básicas
description: Este artigo descreve o desenho de formas básicas no VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Workshop da Web, desenhando formas
- projetando páginas da Web, desenhando formas
- linguagem VML (VML), desenhando formas
- VML (linguagem VML), desenhando formas
- gráficos vetoriais, formas de desenho
- desenhando formas
- Formas de VML, desenho
- linguagem VML (VML), XML
- VML (linguagem VML),XML
- gráficos vetoriais, XML
- linguagem VML (VML), CSS2
- VML (linguagem VML),CSS2
- gráficos vetoriais, CSS2
- linguagem VML (VML), elementos
- VML (linguagem VML), elementos
- elementos gráficos vetoriais
- Elementos VML, formas de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00701e8ac77bd5bda7156c04ca25427d131646bf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407729"
---
# <a name="drawing-basic-shapes"></a><span data-ttu-id="5f41d-120">Desenhando formas básicas</span><span class="sxs-lookup"><span data-stu-id="5f41d-120">Drawing Basic Shapes</span></span>

<span data-ttu-id="5f41d-121">Este tópico descreve o VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5f41d-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5f41d-122">As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="5f41d-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5f41d-123">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="5f41d-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5f41d-124">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="5f41d-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5f41d-125">Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="5f41d-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5f41d-126">Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="5f41d-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5f41d-127">Neste tópico, ilustramos como é fácil desenhar uma forma usando o VML.</span><span class="sxs-lookup"><span data-stu-id="5f41d-127">In this topic, we will illustrate how easy it is to draw a shape using VML.</span></span>

<span data-ttu-id="5f41d-128">Para criar uma oval vermelha em uma página da Web, conforme mostrado na figura a seguir, você pode desenhar a oval usando uma ferramenta de edição gráfica, salvar o desenho como um bitmap e inserir o bitmap na página da Web:</span><span class="sxs-lookup"><span data-stu-id="5f41d-128">To create a red oval on a Web page, as shown in the following picture, you can draw the oval by using a graphic edit tool, save your drawing as a bitmap, and then insert the bitmap on your Web page:</span></span>

![oval1.gif (627 bytes)](images/oval1.gif)

<span data-ttu-id="5f41d-130">Como alternativa, você pode usar o VML para desenhar gráficos.</span><span class="sxs-lookup"><span data-stu-id="5f41d-130">Alternatively, you can use VML to draw graphics.</span></span> <span data-ttu-id="5f41d-131">No exemplo anterior, você pode digitar as seguintes linhas na região da `<BODY>` página da Web para desenhar a oval vermelha:</span><span class="sxs-lookup"><span data-stu-id="5f41d-131">In the preceding example, you can type the following lines in the `<BODY>` region of your Web page to draw the red oval:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





<span data-ttu-id="5f41d-132">`<v:...>` e `</v:...>` são a marca de início e a marca de término na sintaxe [XML](#xml-structure).`style='width:100pt; height:75pt'`</span><span class="sxs-lookup"><span data-stu-id="5f41d-132">`<v:...>` and `</v:...>` are the start tag and end tag in [XML syntax](#xml-structure).`style='width:100pt; height:75pt'`</span></span> <span data-ttu-id="5f41d-133">fornece [informações css](#css-information).</span><span class="sxs-lookup"><span data-stu-id="5f41d-133">provides [CSS information](#css-information).</span></span> <span data-ttu-id="5f41d-134">**oval** e **fillcolor**="red" são [elementos VML](#vml-elements).</span><span class="sxs-lookup"><span data-stu-id="5f41d-134">**oval** and **fillcolor**="red" are [VML elements](#vml-elements).</span></span>

<span data-ttu-id="5f41d-135">Você pode alterar os gráficos simplesmente alterando seus atributos de propriedade no VML.</span><span class="sxs-lookup"><span data-stu-id="5f41d-135">You can alter the graphics by simply changing their property attributes in VML.</span></span> <span data-ttu-id="5f41d-136">No exemplo anterior, se você alterar para , conforme mostrado na seguinte representação de VML, a oval vermelha `fillcolor="red"` mudará para `fillcolor="blue"` azul:</span><span class="sxs-lookup"><span data-stu-id="5f41d-136">In the preceding example, if you change `fillcolor="red"` to `fillcolor="blue"`, as shown in the following VML representation, the red oval will change to blue:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





<span data-ttu-id="5f41d-137">Navegadores que suportam VML podem renderizar e exibir os gráficos representados no VML sem precisar baixar arquivos de imagem separados.</span><span class="sxs-lookup"><span data-stu-id="5f41d-137">Browsers that support VML can render and display the graphics represented in VML without having to download separate image files.</span></span> <span data-ttu-id="5f41d-138">A maioria dos gráficos representados no VML é renderizada mais rapidamente em navegadores e exige menos espaço em disco e tempo de download.</span><span class="sxs-lookup"><span data-stu-id="5f41d-138">Most graphics represented in VML are rendered faster in browsers, and require less disk space and download time.</span></span>

<span data-ttu-id="5f41d-139">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="5f41d-139">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="xml-structure"></a><span data-ttu-id="5f41d-140">Estrutura XML</span><span class="sxs-lookup"><span data-stu-id="5f41d-140">XML Structure</span></span>

<span data-ttu-id="5f41d-141">O VML é formatado de acordo com as regras de linguagem XML (XML).</span><span class="sxs-lookup"><span data-stu-id="5f41d-141">VML is formatted according to the rules of Extensible Markup Language (XML).</span></span> <span data-ttu-id="5f41d-142">Qualquer analisador XML padrão pode analisar o VML e entregar os dados resultantes para um processador específico do VML.</span><span class="sxs-lookup"><span data-stu-id="5f41d-142">Any standard XML parser can parse VML and hand off the resulting data to a VML-specific processor.</span></span> <span data-ttu-id="5f41d-143">Para permitir que os navegadores saibam como entregar dados para um processador específico do VML, você precisa digitar algumas informações, como [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) e [objetos personalizados inseridos.](web-workshop---how-to-use-vml-on-web-pages----appendix.md)</span><span class="sxs-lookup"><span data-stu-id="5f41d-143">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) and [embedded custom objects](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span></span> <span data-ttu-id="5f41d-144">Em seguida, você pode usar o VML para digitar gráficos na região, assim como `<BODY>` fez no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="5f41d-144">You can then use VML to type graphics in the `<BODY>` region just as you did in the preceding example.</span></span>

<span data-ttu-id="5f41d-145">O `"v:"` prefixo em cada marca XML identifica a marca como VML.</span><span class="sxs-lookup"><span data-stu-id="5f41d-145">The `"v:"` prefix on each XML tag identifies the tag as VML.</span></span> <span data-ttu-id="5f41d-146">O `"v:"` prefixo na `<BODY>` região deve ser consistente com `<html xmlns:v="...">` .</span><span class="sxs-lookup"><span data-stu-id="5f41d-146">The `"v:"` prefix in the `<BODY>` region should be consistent with `<html xmlns:v="...">`.</span></span>

<span data-ttu-id="5f41d-147">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="5f41d-147">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="css-information"></a><span data-ttu-id="5f41d-148">Informações de CSS</span><span class="sxs-lookup"><span data-stu-id="5f41d-148">CSS Information</span></span>

<span data-ttu-id="5f41d-149">O VML [usa folhas de estilos em cascata, Nível 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) para determinar o tamanho dos gráficos e posicionar os gráficos em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="5f41d-149">VML uses [Cascading Style Sheets, Level 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) to determine the size of the graphics and to position the graphics on a Web page.</span></span> <span data-ttu-id="5f41d-150">No exemplo anterior, especificamos o tamanho da oval como 100 pontos (largura) em 75 pontos (altura) ( `style='width:100pt;height:75pt'` ).</span><span class="sxs-lookup"><span data-stu-id="5f41d-150">In the preceding example, we specified the size of the oval as 100 points (width) by 75 points (height) (`style='width:100pt;height:75pt'` ).</span></span>

<span data-ttu-id="5f41d-151">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="5f41d-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vml-elements"></a><span data-ttu-id="5f41d-152">Elementos VML</span><span class="sxs-lookup"><span data-stu-id="5f41d-152">VML Elements</span></span>

<span data-ttu-id="5f41d-153">No exemplo anterior, utilizamos um elemento predefinido de VML `<oval>` para desenhar uma oval.</span><span class="sxs-lookup"><span data-stu-id="5f41d-153">In the preceding example, we used a VML predefined `<oval>` element to draw an oval.</span></span> <span data-ttu-id="5f41d-154">Em seguida, utilizamos o atributo de propriedade **fillcolor** `<oval>` do elemento para preencher a oval com vermelho.</span><span class="sxs-lookup"><span data-stu-id="5f41d-154">We then used the **fillcolor** property attribute of the `<oval>` element to fill the oval with red.</span></span>

<span data-ttu-id="5f41d-155">Com base na seção Marcas de [início,](https://www.w3.org/TR/REC-xml#sec-starttags) marcas de extremidade e marcas Empty-Element da especificação [XML 1.0](https://www.w3.org/TR/REC-xml), as marcas de elemento vazio podem ser usadas para qualquer elemento que não tenha conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5f41d-155">Based upon the [Start-Tags, End-Tags, and Empty-Element Tags](https://www.w3.org/TR/REC-xml#sec-starttags) section of [XML 1.0 specification](https://www.w3.org/TR/REC-xml), empty-element tags may be used for any element that has no content.</span></span> <span data-ttu-id="5f41d-156">Por exemplo, conforme mostrado na representação VML a seguir, não há nenhum conteúdo (sub-elemento) dentro do `<oval>` elemento .</span><span class="sxs-lookup"><span data-stu-id="5f41d-156">For example, as shown in the following VML representation, there is no content (sub-element) within the `<oval>` element.</span></span> <span data-ttu-id="5f41d-157">(Observe que o **estilo e** **fillcolor** são os atributos do `<oval>` elemento; eles não são sub-elementos.)</span><span class="sxs-lookup"><span data-stu-id="5f41d-157">(Note that the **style** and **fillcolor** are the attributes of the `<oval>` element; they are not sub-elements.)</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



<span data-ttu-id="5f41d-158">Portanto, você pode usar a marca de elemento vazio, conforme mostrado na representação VML a seguir, para representar a mesma coisa que a linha acima.</span><span class="sxs-lookup"><span data-stu-id="5f41d-158">Therefore, you can use the empty-element tag, as shown in the following VML representation, to represent the same thing as the above line.</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



<span data-ttu-id="5f41d-159">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="5f41d-159">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="5f41d-160">Resumo</span><span class="sxs-lookup"><span data-stu-id="5f41d-160">Summary</span></span>

<span data-ttu-id="5f41d-161">Você pode usar o VML para desenhar gráficos em uma página da Web e, em seguida, personalizar esses gráficos simplesmente alterando seus atributos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5f41d-161">You can use VML to draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span> <span data-ttu-id="5f41d-162">Além disso, a maioria dos gráficos representados no VML é renderizada mais rapidamente em navegadores e leva menos tempo de download e espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="5f41d-162">Also, most graphics represented in VML are rendered faster in browsers, and take less download time and disk space.</span></span>

 

 