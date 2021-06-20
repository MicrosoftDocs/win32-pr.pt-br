---
title: Usando o elemento Stroke
description: Este artigo descreve o uso do elemento Stroke do VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Workshop da Web, elemento stroke
- projetando páginas da Web, elemento stroke
- linguagem VML (VML), elemento stroke
- Elemento VML (linguagem VML),traço
- gráficos vetoriais, elemento stroke
- Elemento stroke
- Elementos VML, traço
- Formas VML, elemento de traço
- linguagem VML (VML), atributo de propriedade dashstyle
- VML (linguagem VML), atributo de propriedade dashstyle
- gráficos vetoriais, atributo de propriedade dashstyle
- Atributo de propriedade dashstyle
- linguagem VML (VML), atributo de propriedade opacity
- VML (linguagem VML), atributo de propriedade opacity
- gráficos vetoriais, atributo de propriedade opacidade
- atributo de propriedade opacity
- linguagem VML (VML), atributo de propriedade linestyle
- VML (linguagem VML), atributo de propriedade linestyle
- gráficos vetoriais, atributo de propriedade linestyle
- atributo de propriedade linestyle
- linguagem VML (VML), atributo de propriedade joinstyle
- VML (linguagem VML), atributo de propriedade joinstyle
- gráficos vetoriais, atributo de propriedade joinstyle
- Atributo de propriedade joinstyle
- linguagem VML (VML), atributo de propriedade filltype
- VML (linguagem VML), atributo de propriedade filltype
- gráficos vetoriais, atributo de propriedade filltype
- atributo de propriedade filltype
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dff7a4b3bc654063fe8156476cc9c52453247a0b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407839"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="681aa-131">Usando o elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="681aa-131">Using the Stroke Element</span></span>

<span data-ttu-id="681aa-132">Este tópico descreve o VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="681aa-132">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="681aa-133">As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="681aa-133">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="681aa-134">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="681aa-134">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="681aa-135">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="681aa-135">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="681aa-136">Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="681aa-136">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="681aa-137">Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="681aa-137">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="681aa-138">Usando `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="681aa-138">Using `<stroke>`</span></span>

<span data-ttu-id="681aa-139">Como você aprendeu, você pode usar os atributos de propriedade **strokecolor** e **strokeweight** de uma forma predefinida – como , , , , , – para especificar a cor e o peso do contorno de uma `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma.</span><span class="sxs-lookup"><span data-stu-id="681aa-139">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="681aa-140">Neste tópico, ilustramos como desenhar uma forma que tenha um contorno mais avançado.</span><span class="sxs-lookup"><span data-stu-id="681aa-140">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="681aa-141">Você pode colocar o subconjunto dentro do , ou ou qualquer elemento de forma predefinido para descrever como desenhar o contorno `<stroke>` `<shape>` da `<shapetype>` forma.</span><span class="sxs-lookup"><span data-stu-id="681aa-141">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="681aa-142">Em seguida, você pode usar os atributos de propriedade – por exemplo, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) – do subconjunto para personalizar o `<stroke>` contorno.</span><span class="sxs-lookup"><span data-stu-id="681aa-142">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="681aa-143">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="681aa-143">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="681aa-144">Dashstyle</span><span class="sxs-lookup"><span data-stu-id="681aa-144">dashstyle</span></span>

<span data-ttu-id="681aa-145">Você pode usar o **atributo de propriedade dashstyle** do `<stroke>` sub-elemento para desenhar um contorno com vários estilos de traço.</span><span class="sxs-lookup"><span data-stu-id="681aa-145">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="681aa-146">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="681aa-146">**Examples:**</span></span>

<span data-ttu-id="681aa-147">Se você especificar `<v:stroke dashstyle="solid" />` dentro do elemento , poderá criar uma linha sólida, conforme mostrado na seguinte representação de `<line>` VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-147">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="681aa-149">Se você alterar o atributo de propriedade **dashstyle** para "ponto", poderá criar uma linha pontilhada, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-149">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 bytes)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="681aa-151">Se você alterar o atributo de propriedade **dashstyle** para "traço", poderá criar uma linha tracejada, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-151">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 bytes)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="681aa-153">Se você alterar o atributo de propriedade **dashstyle** para "dashdot", poderá criar uma linha com um estilo tracejado e pontilhado, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-153">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 bytes)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="681aa-155">Se você alterar o atributo de propriedade **dashstyle** para "longdash", poderá criar uma linha com um estilo longo tracejado, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-155">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 bytes)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="681aa-157">Se você alterar o atributo de propriedade **dashstyle** para "longdashdot", poderá criar uma linha com um estilo longo tracejado e pontilhado, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-157">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 bytes)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="681aa-159">Se você colocar dentro do elemento , poderá criar um retângulo com um contorno tracejado e pontilhado, conforme mostrado na seguinte representação `<v:stroke dashstyle="dashdot" />` `<rect>` de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-159">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="681aa-161">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="681aa-161">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="681aa-162">opacidade</span><span class="sxs-lookup"><span data-stu-id="681aa-162">opacity</span></span>

<span data-ttu-id="681aa-163">Você pode usar o **atributo de propriedade de opacidade** do subconjunto para desenhar um contorno com vários estilos de `<stroke>` opacidade.</span><span class="sxs-lookup"><span data-stu-id="681aa-163">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="681aa-164">O valor do atributo **de propriedade opacidade** pode ser qualquer número entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="681aa-164">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="681aa-165">Por padrão, é 1, indicando opacidade total.</span><span class="sxs-lookup"><span data-stu-id="681aa-165">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="681aa-166">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="681aa-166">**Examples:**</span></span>

<span data-ttu-id="681aa-167">A seguinte representação de VML cria uma linha com opacidade total:</span><span class="sxs-lookup"><span data-stu-id="681aa-167">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="681aa-169">Se você adicionar dentro do elemento , poderá criar uma linha com `<v:stroke opacity="0.5" />` 50% de opacidade, conforme mostrado na seguinte representação `<line>` de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-169">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="681aa-171">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="681aa-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="681aa-172">Linestyle</span><span class="sxs-lookup"><span data-stu-id="681aa-172">linestyle</span></span>

<span data-ttu-id="681aa-173">Você pode usar o **atributo de propriedade linestyle** do `<stroke>` sub-elemento para desenhar um contorno com vários estilos de linha.</span><span class="sxs-lookup"><span data-stu-id="681aa-173">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="681aa-174">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="681aa-174">**Examples:**</span></span>

<span data-ttu-id="681aa-175">Se você especificar dentro do elemento , poderá criar um retângulo com um único contorno, conforme mostrado na seguinte representação `<v:stroke linestyle="single" />` `<rect>` de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-175">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="681aa-177">Se você alterar o atributo de propriedade **linestyle** para "thinthin", poderá criar um retângulo com o contorno (1:1:1), conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-177">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 bytes)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="681aa-179">Se você alterar o atributo de propriedade **linestyle** para "thinthick", poderá criar um retângulo com o contorno (1:1:2), conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-179">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="681aa-181">Se você alterar o atributo de propriedade **linestyle** para "thickthin", poderá criar um retângulo com o contorno (2:1:1), conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-181">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="681aa-183">Se você alterar o atributo de propriedade **linestyle** para "thickbetweenthin", poderá criar um retângulo com o contorno (1:1:2:1:1), conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-183">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 bytes)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="681aa-185">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="681aa-185">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="681aa-186">joinstyle</span><span class="sxs-lookup"><span data-stu-id="681aa-186">joinstyle</span></span>

<span data-ttu-id="681aa-187">Você pode usar o **atributo joinstyle** do `<stroke>` subconjunto para definir como as linhas são unidas.</span><span class="sxs-lookup"><span data-stu-id="681aa-187">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="681aa-188">Por exemplo, para criar uma forma que tenha o contorno de junção de ida e volta, conforme mostrado na ilustração a seguir, você pode especificar dentro do elemento , conforme mostrado na seguinte representação `<v:stroke joinstyle="round" />` `<polyline>` de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-188">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="681aa-190">Se você alterar o atributo de propriedade **joinstyle** para "bevel", poderá criar uma forma que tenha o contorno de junção de nível, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-190">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 bytes)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="681aa-192">Se você alterar o atributo de propriedade **joinstyle** para "miter", poderá criar uma forma que tenha o contorno miter-join, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-192">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="681aa-194">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="681aa-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="681aa-195">Filltype</span><span class="sxs-lookup"><span data-stu-id="681aa-195">filltype</span></span>

<span data-ttu-id="681aa-196">Você pode usar o **atributo de propriedade filltype** do `<stroke>` sub-elemento para desenhar um contorno com vários efeitos de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="681aa-196">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="681aa-197">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="681aa-197">**Examples:**</span></span>

<span data-ttu-id="681aa-198">Se você especificar dentro do elemento , poderá criar um retângulo arredondado com a estrutura de contorno preenchida sólida, conforme mostrado na seguinte representação `<v:stroke filltype="solid" />` `<roundrect>` de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-198">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 bytes)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="681aa-200">Se você alterar o atributo de propriedade **filltype** para "pattern", aponte o atributo de propriedade **src** para o local do arquivo de imagem padrão e de definir o atributo de propriedade **color2** como a segunda cor padrão, você poderá criar um retângulo arredondado com um contorno de padrão, conforme mostrado na seguinte representação VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-200">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="681aa-202">Se você alterar o atributo de propriedade **filltype** para "bloco" e apontar o atributo de propriedade **src** para o local do arquivo de imagem, poderá criar um retângulo arredondado com um contorno lado a lado, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-202">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="681aa-204">Se você alterar o atributo de propriedade **filltype** para "frame" e apontar o atributo de propriedade **src** para o local do arquivo de imagem, poderá criar um retângulo arredondado com um contorno de imagem, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="681aa-204">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="681aa-206">Para obter mais informações sobre esse elemento, consulte a [especificação de VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span><span class="sxs-lookup"><span data-stu-id="681aa-206">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 