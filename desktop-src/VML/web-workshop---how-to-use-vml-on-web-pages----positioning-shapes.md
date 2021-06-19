---
title: Posicionando formas
description: Este artigo descreve as formas de posicionamento no VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Web Workshop, posicionando formas
- Criando páginas da Web, posicionando formas
- Linguagem VML (VML), posicionando formas
- VML (linguagem VML), posicionando formas
- gráficos vetoriais, posicionando formas
- Formas de VML, posicionamento
- posicionando formas
- Linguagem VML (VML), estilo de posição estática
- VML (linguagem VML), estilo de posição estática
- gráficos vetoriais, estilo de posição estática
- estilo de posição estática
- Linguagem VML (VML), estilo de posição relativa
- VML (linguagem VML), estilo de posição relativa
- gráficos vetoriais, estilo de posição relativa
- estilo de posição relativa
- Linguagem VML (VML), estilo de posição absoluta
- VML (linguagem VML), estilo de posição absoluta
- gráficos vetoriais, estilo de posição absoluta
- estilo de posição absoluta
- Linguagem VML (VML), estilo de posição de índice z
- VML (linguagem VML), z-estilo da posição do índice
- gráficos vetoriais, estilo de posição de índice z
- estilo de posição de índice z
- Linguagem VML (VML), estilo de posição de rotação
- VML (linguagem VML), estilo de posição de rotação
- gráficos vetoriais, estilo de posição de rotação
- estilo de posição de rotação
- Linguagem VML (VML), inverter estilo de posição
- VML (linguagem VML), inverter estilo de posição
- gráficos vetoriais, inverter estilo de posição
- Inverter estilo de posição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c96a8de891ed1bbd1b9bfee9eff52ede946247b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407709"
---
# <a name="positioning-shapes"></a><span data-ttu-id="96419-134">Posicionando formas</span><span class="sxs-lookup"><span data-stu-id="96419-134">Positioning Shapes</span></span>

<span data-ttu-id="96419-135">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="96419-135">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="96419-136">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="96419-136">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="96419-137">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="96419-137">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="96419-138">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="96419-138">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="96419-139">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="96419-139">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="96419-140">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="96419-140">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="96419-141">Você aprendeu como desenhar e colorir formas em uma página da Web usando a VML.</span><span class="sxs-lookup"><span data-stu-id="96419-141">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="96419-142">Neste tópico, você usará a VML para posicionar com precisão elementos gráficos em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="96419-142">In this topic, you'll use VML to precisely position graphics on a Web page.</span></span>

<span data-ttu-id="96419-143">A VML usa a mesma sintaxe definida nas seções [modelo de caixa](https://www.w3.org/TR/PR-CSS2/box.mdl) e modelo de [renderização visual](https://www.w3.org/TR/PR-CSS2/visuren.mdl) de [CSS2](https://www.w3.org/TR/PR-CSS2/) para posicionar formas em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="96419-143">VML uses the same syntax defined in the [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) and [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) sections of [CSS2](https://www.w3.org/TR/PR-CSS2/) to position shapes on a Web page.</span></span> <span data-ttu-id="96419-144">Você pode usar [estático](#static), [relativo](#relative)ou [absoluto](#absolute) para determinar onde o ponto base está localizado em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="96419-144">You can use [static](#static), [relative](#relative), or [absolute](#absolute) to determine where the base point is located on a Web page.</span></span> <span data-ttu-id="96419-145">Você pode usar os atributos de estilo **superior** e **esquerdo** para especificar o deslocamento do ponto de base no qual a caixa de contenção da forma será posicionada.</span><span class="sxs-lookup"><span data-stu-id="96419-145">You can then use the **top** and **left** style attributes to specify the offset from the base point at which the containing box for the shape will be positioned.</span></span>

<span data-ttu-id="96419-146">Você também pode usar o [z-index](#z-index) para especificar a ordem z das formas em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="96419-146">You can also use [z-index](#z-index) to specify the z-order of shapes on a Web page.</span></span>

<span data-ttu-id="96419-147">Além disso, a VML fornece [rotação](#rotation) e [inverter](#flip) para girar ou inverter formas.</span><span class="sxs-lookup"><span data-stu-id="96419-147">In addition, VML provides [rotation](#rotation) and [flip](#flip) to rotate or flip shapes.</span></span>

<span data-ttu-id="96419-148">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="96419-148">In this topic:</span></span>

-   [<span data-ttu-id="96419-149">static</span><span class="sxs-lookup"><span data-stu-id="96419-149">static</span></span>](#static)
-   [<span data-ttu-id="96419-150">relative</span><span class="sxs-lookup"><span data-stu-id="96419-150">relative</span></span>](#relative)
-   [<span data-ttu-id="96419-151">absolute</span><span class="sxs-lookup"><span data-stu-id="96419-151">absolute</span></span>](#absolute)
-   [<span data-ttu-id="96419-152">índice z</span><span class="sxs-lookup"><span data-stu-id="96419-152">z-index</span></span>](#z-index)
-   [<span data-ttu-id="96419-153">gira</span><span class="sxs-lookup"><span data-stu-id="96419-153">rotation</span></span>](#rotation)
-   [<span data-ttu-id="96419-154">flip</span><span class="sxs-lookup"><span data-stu-id="96419-154">flip</span></span>](#flip)
-   [<span data-ttu-id="96419-155">Resumo</span><span class="sxs-lookup"><span data-stu-id="96419-155">Summary</span></span>](#summary)

## <a name="static"></a><span data-ttu-id="96419-156">static</span><span class="sxs-lookup"><span data-stu-id="96419-156">static</span></span>

<span data-ttu-id="96419-157">O estilo de posição padrão é estático, o que instrui os navegadores a posicionar a forma no ponto atual (o ponto base) no fluxo de texto e ignorar as configurações nos atributos de estilo **superior** e **esquerdo** .</span><span class="sxs-lookup"><span data-stu-id="96419-157">The default position style is static, which instructs browsers to position the shape at the current point (the base point) in the text flow and ignore the settings in the **top** and **left** style attributes.</span></span>

<span data-ttu-id="96419-158">Por exemplo, na representação de VML a seguir, a elipse vermelha é posicionada imediatamente após o texto "início da forma:", conforme mostrado na figura a seguir:</span><span class="sxs-lookup"><span data-stu-id="96419-158">For example, in the following VML representation, the red oval is positioned immediately after the text "Beginning of the shape:", as shown in the following picture:</span></span>

![\-ps.gif Shape1 (2123 bytes)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="96419-160">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="96419-160">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="relative"></a><span data-ttu-id="96419-161">relative</span><span class="sxs-lookup"><span data-stu-id="96419-161">relative</span></span>

<span data-ttu-id="96419-162">Definir o atributo de estilo de posição como "relativo" permite que você coloque a caixa de conteúdo com um deslocamento do ponto atual (o ponto base) no fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="96419-162">Setting the position style attribute to "relative" allows you to place the containing box with an offset from the current point (the base point) in the text flow.</span></span> <span data-ttu-id="96419-163">O deslocamento é determinado pelas configurações nos atributos de estilo **superior** e **esquerdo** .</span><span class="sxs-lookup"><span data-stu-id="96419-163">The offset is determined by the settings in the **top** and **left** style attributes.</span></span> <span data-ttu-id="96419-164">Lembre-se de que a caixa que a contém posicionada como relativa ocupa espaço no fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="96419-164">Be aware that the containing box that is positioned as relative takes up space in the text flow.</span></span>

<span data-ttu-id="96419-165">Por exemplo, na representação de VML a seguir, a elipse vermelha é posicionada em 20 pontos à esquerda e 10 pontos da parte superior em relação ao ponto atual no fluxo de texto, conforme mostrado na figura a seguir:</span><span class="sxs-lookup"><span data-stu-id="96419-165">For example, in the following VML representation, the red oval is positioned 20 points from the left and 10 points from the top relative to the current point in the text flow, as shown in the following picture:</span></span>

![shape3.gif (2048 bytes)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="96419-167">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="96419-167">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="absolute"></a><span data-ttu-id="96419-168">absoluto</span><span class="sxs-lookup"><span data-stu-id="96419-168">absolute</span></span>

<span data-ttu-id="96419-169">Definir o atributo de estilo de posição como "absoluto" permite colocar a caixa de conteúdo em uma distância exata do canto superior esquerdo (o ponto de base) de seu elemento pai (o elemento posicionado que contém a forma).</span><span class="sxs-lookup"><span data-stu-id="96419-169">Setting the position style attribute to "absolute" allows you to place the containing box an exact distance from the top left corner (the base point) of its parent element (the positioned element that contains the shape).</span></span> <span data-ttu-id="96419-170">Lembre-se de que a caixa que o contém está posicionada como absoluta não ocupa espaço no fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="96419-170">Be aware that the containing box that is positioned as absolute doesn't take up space in the text flow.</span></span>

<span data-ttu-id="96419-171">Por exemplo, na representação de VML a seguir, a elipse vermelha está contida no `<body>` elemento (a página da Web inteira); portanto, o ponto base está no canto superior esquerdo da página da Web.</span><span class="sxs-lookup"><span data-stu-id="96419-171">For example, in the following VML representation, the red oval is contained within the `<body>` element (the entire Web page); therefore, the base point is at the top left corner of the Web page.</span></span> <span data-ttu-id="96419-172">A caixa que o contém para a oval é posicionada exatamente 20 pontos da esquerda e 10 pontos da parte superior, em relação ao canto superior esquerdo da página da Web, conforme mostrado na figura a seguir:</span><span class="sxs-lookup"><span data-stu-id="96419-172">The containing box for the oval is positioned exactly 20 points from the left and 10 points from the top, relative to the top left corner of the Web page, as shown in the following picture:</span></span>

![shape2.gif (2006 bytes)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="96419-174">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="96419-174">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="z-index"></a><span data-ttu-id="96419-175">z-index</span><span class="sxs-lookup"><span data-stu-id="96419-175">z-index</span></span>

<span data-ttu-id="96419-176">É possível posicionar uma forma que se sobrepõe a outra forma.</span><span class="sxs-lookup"><span data-stu-id="96419-176">It is possible to position a shape that overlaps another shape.</span></span> <span data-ttu-id="96419-177">Normalmente, o elemento gráfico listado por último no código HTML aparece na parte superior.</span><span class="sxs-lookup"><span data-stu-id="96419-177">Normally, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="96419-178">Na VML, você pode controlar a ordem z usando o atributo **z-index** Style.</span><span class="sxs-lookup"><span data-stu-id="96419-178">In VML, you can control the z-order by using the **z-index** style attribute.</span></span> <span data-ttu-id="96419-179">O valor desse atributo pode ser zero, um inteiro positivo ou um inteiro negativo.</span><span class="sxs-lookup"><span data-stu-id="96419-179">The value of this attribute can be zero, a positive integer, or a negative integer.</span></span> <span data-ttu-id="96419-180">O gráfico que tem um valor maior de índice z é exibido na parte superior do gráfico que tem um valor menor de índice z.</span><span class="sxs-lookup"><span data-stu-id="96419-180">The graphic that has a larger z-index value is displayed on top of the graphic that has a smaller z-index value.</span></span> <span data-ttu-id="96419-181">Quando ambos os elementos gráficos tiverem o mesmo valor de índice z, o gráfico listado por último no código HTML aparecerá na parte superior.</span><span class="sxs-lookup"><span data-stu-id="96419-181">When both graphics have the same z-index value, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="96419-182">Por exemplo, na representação de VML a seguir, a elipse vermelha é exibida na parte superior do retângulo azul.</span><span class="sxs-lookup"><span data-stu-id="96419-182">For example, in the following VML representation, the red oval is displayed on top of the blue rectangle.</span></span> <span data-ttu-id="96419-183">Isso ocorre porque o valor do índice z da elipse vermelha é maior que o valor do índice z do retângulo azul.</span><span class="sxs-lookup"><span data-stu-id="96419-183">This is because the z-index value of the red oval is greater than the z-index value of the blue rectangle.</span></span>

![shape4.gif (572 bytes)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





<span data-ttu-id="96419-185">Se você alterar o índice z, conforme mostrado na representação de VML a seguir, a elipse vermelha se moverá para trás do retângulo azul.</span><span class="sxs-lookup"><span data-stu-id="96419-185">If you change the z-index, as shown in the following VML representation, the red oval would move behind the blue rectangle.</span></span>

![shape5.gif (469 bytes)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





<span data-ttu-id="96419-187">Se você fornecer um inteiro negativo, poderá usar o índice z para posicionar gráficos atrás do fluxo de texto normal, conforme mostrado na representação de VML a seguir.</span><span class="sxs-lookup"><span data-stu-id="96419-187">If you supply a negative integer, you can use z-index to position graphics behind the normal text flow, as shown in the following VML representation.</span></span>

![shape6.gif (2125 bytes)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="96419-189">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="96419-189">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rotation"></a><span data-ttu-id="96419-190">rotação</span><span class="sxs-lookup"><span data-stu-id="96419-190">rotation</span></span>

<span data-ttu-id="96419-191">Você pode usar o atributo de estilo de **rotação** para especificar quantos graus você deseja que uma forma ative em seu eixo.</span><span class="sxs-lookup"><span data-stu-id="96419-191">You can use the **rotation** style attribute to specify how many degrees you want a shape to turn on its axis.</span></span> <span data-ttu-id="96419-192">Um valor positivo indica uma rotação horária; um valor negativo indica uma rotação no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="96419-192">A positive value indicates a clockwise rotation; a negative value indicates a counter-clockwise rotation.</span></span>

<span data-ttu-id="96419-193">Por exemplo, se você especificar **Style**= '... rotação: 90 ', você pode girar a forma 90 graus no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="96419-193">For example, if you specify **style**='... rotation:90', you can rotate the shape 90 degrees clockwise.</span></span>

<span data-ttu-id="96419-194">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="96419-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="flip"></a><span data-ttu-id="96419-195">flip</span><span class="sxs-lookup"><span data-stu-id="96419-195">flip</span></span>

<span data-ttu-id="96419-196">Você pode usar o atributo **flip** Style para inverter uma forma em seu eixo x ou y de acordo com a tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="96419-196">You can use the **flip** style attribute to flip a shape on its x or y axis according to the following table:</span></span>



| <span data-ttu-id="96419-197">Valor</span><span class="sxs-lookup"><span data-stu-id="96419-197">Value</span></span> | <span data-ttu-id="96419-198">Descrição</span><span class="sxs-lookup"><span data-stu-id="96419-198">Description</span></span>                                                  |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="96419-199">x</span><span class="sxs-lookup"><span data-stu-id="96419-199">x</span></span>     | <span data-ttu-id="96419-200">Virar a forma girada sobre o eixo y (Inverter x ordenada)</span><span class="sxs-lookup"><span data-stu-id="96419-200">Flip the rotated shape about the y axis (invert x ordinates)</span></span> |
| <span data-ttu-id="96419-201">a</span><span class="sxs-lookup"><span data-stu-id="96419-201">y</span></span>     | <span data-ttu-id="96419-202">Virar a forma girada sobre o eixo x (inverter as ordenada y)</span><span class="sxs-lookup"><span data-stu-id="96419-202">Flip the rotated shape about the x axis (invert y ordinates)</span></span> |



 

<span data-ttu-id="96419-203">X e y podem ser especificados na propriedade flip.</span><span class="sxs-lookup"><span data-stu-id="96419-203">Both x and y may be specified in the flip property.</span></span>

<span data-ttu-id="96419-204">Por exemplo, se você digitar **Style**= '... virar: x y ', você inverterá a forma em ambos os eixos x e y.</span><span class="sxs-lookup"><span data-stu-id="96419-204">For example, if you type **style**='... flip:x y', you will flip the shape on both its x and y axis.</span></span>

<span data-ttu-id="96419-205">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="96419-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="96419-206">Resumo</span><span class="sxs-lookup"><span data-stu-id="96419-206">Summary</span></span>

<span data-ttu-id="96419-207">Com base no que você aprendeu, você pode posicionar precisamente uma forma em uma página da Web seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="96419-207">Based on what you've learned, you can precisely position a shape on a Web page by following these steps:</span></span>

1.  <span data-ttu-id="96419-208">Decida onde você deseja que a forma apareça em uma página da Web e o tamanho da forma.</span><span class="sxs-lookup"><span data-stu-id="96419-208">Decide where you want the shape to appear on a Web page, and the size of the shape.</span></span>
2.  <span data-ttu-id="96419-209">Especifique **Style**= ' posição: relativa (ou relativa) ' para determinar o ponto base.</span><span class="sxs-lookup"><span data-stu-id="96419-209">Specify **style**='position:relative (or relative)' to determine the base point.</span></span>
3.  <span data-ttu-id="96419-210">Use **Left** e **Top** para especificar o deslocamento do ponto de base.</span><span class="sxs-lookup"><span data-stu-id="96419-210">Use **left** and **top** to specify the offset from the base point.</span></span>
4.  <span data-ttu-id="96419-211">Use **largura** e **altura** para especificar o tamanho da caixa que contém para a forma.</span><span class="sxs-lookup"><span data-stu-id="96419-211">Use **width** and **height** to specify the size of the containing box for the shape.</span></span>
5.  <span data-ttu-id="96419-212">Use **z-index** para especificar a ordem z da forma.</span><span class="sxs-lookup"><span data-stu-id="96419-212">Use **z-index** to specify the z-order of the shape.</span></span>

 

 