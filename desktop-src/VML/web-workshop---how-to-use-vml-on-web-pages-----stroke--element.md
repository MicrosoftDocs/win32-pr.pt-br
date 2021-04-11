---
title: Usando o elemento Stroke
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Web Workshop, elemento Stroke
- Criando páginas da Web, elemento Stroke
- Linguagem VML (VML), elemento Stroke
- VML (linguagem VML), elemento Stroke
- gráfico vetorial, elemento Stroke
- elemento Stroke
- Elementos de VML, traço
- Formas VML, elemento Stroke
- Linguagem VML (VML), atributo de propriedade DashStyle
- VML (linguagem VML), atributo de propriedade DashStyle
- gráficos vetoriais, atributo de propriedade DashStyle
- atributo de propriedade DashStyle
- Linguagem VML (VML), atributo de propriedade Opacity
- VML (linguagem VML), atributo de propriedade Opacity
- gráficos vetoriais, atributo de propriedade Opacity
- atributo de propriedade Opacity
- Linguagem VML (VML), atributo de propriedade LineStyle
- VML (linguagem VML), atributo de propriedade LineStyle
- gráficos vetoriais, atributo de propriedade LineStyle
- atributo de propriedade LineStyle
- Linguagem VML (VML), atributo de propriedade joinstyle
- VML (linguagem VML), atributo de propriedade joinstyle
- gráficos vetoriais, atributo de propriedade joinstyle
- atributo de propriedade joinstyle
- Linguagem VML (VML), atributo de propriedade FillType
- VML (linguagem VML), atributo de propriedade FillType
- gráfico vetorial, atributo de propriedade FillType
- atributo de propriedade FillType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b58e02945884ea63ad1be01e67cfc156951cd5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294466"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="f6263-132">Usando o elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="f6263-132">Using the Stroke Element</span></span>

<span data-ttu-id="f6263-133">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f6263-133">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f6263-134">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="f6263-134">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f6263-135">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="f6263-135">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f6263-136">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="f6263-136">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f6263-137">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f6263-137">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f6263-138">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f6263-138">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f6263-139">Usando `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="f6263-139">Using `<stroke>`</span></span>

<span data-ttu-id="f6263-140">Como você aprendeu, você pode usar os atributos de propriedade **strokecolor** e **strokeweight** de uma forma predefinida, como,,,, `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` , `<roundrect>` , `<arc>` --para especificar a cor e o peso do contorno de uma forma.</span><span class="sxs-lookup"><span data-stu-id="f6263-140">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="f6263-141">Neste tópico, Ilustraremos como desenhar uma forma que tenha uma estrutura de tópicos mais avançada.</span><span class="sxs-lookup"><span data-stu-id="f6263-141">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="f6263-142">Você pode posicionar o `<stroke>` subelemento dentro do `<shape>` , ou `<shapetype>` ou qualquer elemento Shape predefinido para descrever como desenhar o contorno da forma.</span><span class="sxs-lookup"><span data-stu-id="f6263-142">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="f6263-143">Em seguida, você pode usar os atributos de propriedade, por exemplo, [DashStyle](#dashstyle), [Opacity](#opacity), [LineStyle](#linestyle), [joinstyle](#joinstyle), [FillType](#filltype) --do `<stroke>` subelemento para personalizar a estrutura de tópicos.</span><span class="sxs-lookup"><span data-stu-id="f6263-143">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="f6263-144">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f6263-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="f6263-145">DashStyle</span><span class="sxs-lookup"><span data-stu-id="f6263-145">dashstyle</span></span>

<span data-ttu-id="f6263-146">Você pode usar o atributo de propriedade **DashStyle** do `<stroke>` subelemento para desenhar um contorno com vários estilos de traço.</span><span class="sxs-lookup"><span data-stu-id="f6263-146">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="f6263-147">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="f6263-147">**Examples:**</span></span>

<span data-ttu-id="f6263-148">Se você especificar `<v:stroke dashstyle="solid" />` dentro do `<line>` elemento, poderá criar uma linha sólida, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-148">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="f6263-150">Se você alterar o atributo da propriedade **DashStyle** para "ponto", poderá criar uma linha pontilhada, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-150">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 bytes)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="f6263-152">Se você alterar o atributo da propriedade **DashStyle** para "Dash", poderá criar uma linha tracejada, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-152">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 bytes)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="f6263-154">Se você alterar o atributo da propriedade **DashStyle** para "travessão ponto", poderá criar uma linha com um estilo tracejado e pontilhado, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-154">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 bytes)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="f6263-156">Se você alterar o atributo da propriedade **DashStyle** para "longdash", poderá criar uma linha com um estilo tracejado longo, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-156">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 bytes)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="f6263-158">Se você alterar o atributo da propriedade **DashStyle** para "longdashdot", poderá criar uma linha com um estilo tracejado longo e pontilhado, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-158">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 bytes)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="f6263-160">Se você posicionar `<v:stroke dashstyle="dashdot" />` dentro do `<rect>` elemento, poderá criar um retângulo que tenha um esboço tracejado e pontilhado, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-160">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="f6263-162">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f6263-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="f6263-163">opacidade</span><span class="sxs-lookup"><span data-stu-id="f6263-163">opacity</span></span>

<span data-ttu-id="f6263-164">Você pode usar o atributo de propriedade **Opacity** do `<stroke>` subelemento para desenhar um contorno com vários estilos de opacidade.</span><span class="sxs-lookup"><span data-stu-id="f6263-164">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="f6263-165">O valor do atributo de propriedade **Opacity** pode ser qualquer número entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="f6263-165">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="f6263-166">Por padrão, é 1, indicando a opacidade total.</span><span class="sxs-lookup"><span data-stu-id="f6263-166">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="f6263-167">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="f6263-167">**Examples:**</span></span>

<span data-ttu-id="f6263-168">A seguinte representação de VML cria uma linha com opacidade total:</span><span class="sxs-lookup"><span data-stu-id="f6263-168">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="f6263-170">Se você adicionar `<v:stroke opacity="0.5" />` dentro do `<line>` elemento, poderá criar uma linha com opacidade de 50%, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-170">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="f6263-172">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f6263-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="f6263-173">estilo</span><span class="sxs-lookup"><span data-stu-id="f6263-173">linestyle</span></span>

<span data-ttu-id="f6263-174">Você pode usar o atributo de propriedade **LineStyle** do `<stroke>` subelemento para desenhar um contorno com vários estilos de linha.</span><span class="sxs-lookup"><span data-stu-id="f6263-174">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="f6263-175">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="f6263-175">**Examples:**</span></span>

<span data-ttu-id="f6263-176">Se você especificar `<v:stroke linestyle="single" />` dentro do `<rect>` elemento, poderá criar um retângulo com um único contorno, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-176">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="f6263-178">Se você alterar o atributo da propriedade **LineStyle** para "thinthin", poderá criar um retângulo com a estrutura de tópicos (1:1:1), conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-178">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 bytes)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="f6263-180">Se você alterar o atributo da propriedade **LineStyle** para "thinthick", poderá criar um retângulo com a estrutura de tópicos (1:1:2), conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-180">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="f6263-182">Se você alterar o atributo da propriedade **LineStyle** para "thickthin", poderá criar um retângulo com a estrutura de tópicos (2:1:1), conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-182">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="f6263-184">Se você alterar o atributo da propriedade **LineStyle** para "thickbetweenthin", poderá criar um retângulo com a estrutura de tópicos (1:1:2:1:1), conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-184">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 bytes)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="f6263-186">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f6263-186">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="f6263-187">joinstyle</span><span class="sxs-lookup"><span data-stu-id="f6263-187">joinstyle</span></span>

<span data-ttu-id="f6263-188">Você pode usar o atributo **joinstyle** do `<stroke>` subelemento para definir como as linhas são unidas.</span><span class="sxs-lookup"><span data-stu-id="f6263-188">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="f6263-189">Por exemplo, para criar uma forma que tenha a estrutura de tópicos de junção redonda, conforme mostrado na ilustração a seguir, você pode especificar `<v:stroke joinstyle="round" />` dentro do `<polyline>` elemento, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-189">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="f6263-191">Se você alterar o atributo da propriedade **joinstyle** para "bisel", poderá criar uma forma que tenha a estrutura de tópicos de junção chanfrada, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-191">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 bytes)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="f6263-193">Se você alterar o atributo da propriedade **joinstyle** para "Mitre", poderá criar uma forma que tenha a estrutura de tópicos de junção de Mitre, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-193">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="f6263-195">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="f6263-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="f6263-196">FillType</span><span class="sxs-lookup"><span data-stu-id="f6263-196">filltype</span></span>

<span data-ttu-id="f6263-197">Você pode usar o atributo de propriedade **FillType** do `<stroke>` subelemento para desenhar um contorno com vários efeitos de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="f6263-197">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="f6263-198">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="f6263-198">**Examples:**</span></span>

<span data-ttu-id="f6263-199">Se você especificar `<v:stroke filltype="solid" />` dentro do `<roundrect>` elemento, poderá criar um retângulo arredondado com a estrutura de tópicos preenchida de forma sólida, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-199">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 bytes)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="f6263-201">Se você alterar o atributo da propriedade **FillType** para "Pattern", apontar o atributo da propriedade **src** para o local do arquivo de imagem padrão e definir o atributo da propriedade **color2** para a segunda cor de padrão, poderá criar um retângulo arredondado com um contorno de padrão, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-201">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="f6263-203">Se você alterar o atributo de propriedade **FillType** para "tile" e apontar o atributo da propriedade **src** para o local do arquivo de imagem, poderá criar um retângulo arredondado com um contorno lado a lado, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-203">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="f6263-205">Se você alterar o atributo de propriedade **FillType** para "frame" e apontar o atributo da propriedade **src** para o local do arquivo de imagem, poderá criar um retângulo arredondado com um contorno de imagem, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="f6263-205">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="f6263-207">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span><span class="sxs-lookup"><span data-stu-id="f6263-207">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 