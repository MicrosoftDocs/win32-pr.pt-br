---
title: Usando formas predefinidas
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Web Workshop, formas predefinidas
- Criando páginas da Web, formas predefinidas
- Linguagem VML (VML), formas predefinidas
- VML (linguagem VML), formas predefinidas
- gráficos vetoriais, formas predefinidas
- Formas de VML, predefinidas
- formas predefinidas
- Linguagem VML (VML), elemento Rect
- VML (linguagem VML), elemento Rect
- gráfico vetorial, elemento Rect
- elemento Rect
- Elementos de VML, Rect
- Linguagem VML (VML), elemento RoundRect
- VML (linguagem VML), elemento RoundRect
- gráficos vetoriais, elemento RoundRect
- elemento RoundRect
- Elementos de VML, RoundRect
- Linguagem VML (VML), elemento de linha
- VML (linguagem VML), elemento de linha
- elementos gráficos vetoriais, elemento line
- elemento de linha
- Elementos de VML, linha
- Linguagem VML (VML), elemento Polyline
- VML (linguagem VML), elemento Polyline
- gráficos vetoriais, elemento Polyline
- elemento Polyline
- Elementos de VML, polilinha
- Linguagem VML (VML), elemento de curva
- VML (linguagem VML), elemento de curva
- gráficos vetoriais, elemento de curva
- elemento Curve
- Elementos de VML, curva
- Linguagem VML (VML), elemento Arc
- VML (linguagem VML), elemento Arc
- gráficos vetoriais, elemento Arc
- elemento Arc
- Elementos de VML, arco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c1cafacf00f6f3f9129c29c56837f3f485aa3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499076"
---
# <a name="using-predefined-shapes"></a><span data-ttu-id="1f6b4-141">Usando formas predefinidas</span><span class="sxs-lookup"><span data-stu-id="1f6b4-141">Using Predefined Shapes</span></span>

<span data-ttu-id="1f6b4-142">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-142">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1f6b4-143">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-143">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1f6b4-144">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-144">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1f6b4-145">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-145">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1f6b4-146">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1f6b4-146">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1f6b4-147">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1f6b4-147">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1f6b4-148">Como você aprendeu, você pode usar o `<oval>` elemento de VML para criar uma elipse simples.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-148">As you've learned, you can use the `<oval>` element of VML to create a simple oval.</span></span> <span data-ttu-id="1f6b4-149">A VML fornece vários outros elementos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-149">VML provides several other predefined elements.</span></span> <span data-ttu-id="1f6b4-150">Neste tópico, Ilustraremos como desenhar gráficos usando esses elementos.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-150">In this topic, we will illustrate how to draw graphics by using these elements.</span></span>

<span data-ttu-id="1f6b4-151">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="1f6b4-151">In this topic:</span></span>

-   [<span data-ttu-id="1f6b4-152">Rect</span><span class="sxs-lookup"><span data-stu-id="1f6b4-152">rect</span></span>](#roundrect)
-   [<span data-ttu-id="1f6b4-153">RoundRect</span><span class="sxs-lookup"><span data-stu-id="1f6b4-153">roundrect</span></span>](#roundrect)
-   [<span data-ttu-id="1f6b4-154">descritos</span><span class="sxs-lookup"><span data-stu-id="1f6b4-154">line</span></span>](#polyline)
-   [<span data-ttu-id="1f6b4-155">múltipla</span><span class="sxs-lookup"><span data-stu-id="1f6b4-155">polyline</span></span>](#polyline)
-   [<span data-ttu-id="1f6b4-156">curva</span><span class="sxs-lookup"><span data-stu-id="1f6b4-156">curve</span></span>](#curve)
-   [<span data-ttu-id="1f6b4-157">arco</span><span class="sxs-lookup"><span data-stu-id="1f6b4-157">arc</span></span>](#arc)
-   [<span data-ttu-id="1f6b4-158">Resumo</span><span class="sxs-lookup"><span data-stu-id="1f6b4-158">Summary</span></span>](#summary)

## <a name="rect"></a><span data-ttu-id="1f6b4-159">rect</span><span class="sxs-lookup"><span data-stu-id="1f6b4-159">rect</span></span>

<span data-ttu-id="1f6b4-160">Você pode usar o `<rect>` elemento para desenhar um retângulo.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-160">You can use the `<rect>` element to draw a rectangle.</span></span> <span data-ttu-id="1f6b4-161">Em seguida, você pode personalizar o retângulo especificando atributos de propriedade diferentes.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-161">You can then customize the rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="1f6b4-162">Por exemplo, você pode desenhar um retângulo que é preenchido com azul especificando **FillColor**= "Blue" e dar a ele um esboço vermelho de 3,5 pontos especificando **strokecolor**= "Red" **strokeweight**= "3.5 pt", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="1f6b4-162">For example, you can draw a rectangle that is filled with blue by specifying **fillcolor**="blue", and give it a 3.5-point red outline by specifying **strokecolor**="red" **strokeweight**="3.5pt", as shown in the following VML representation:</span></span>

![rect1.gif (485 bytes)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





<span data-ttu-id="1f6b4-164">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="1f6b4-164">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span> <span data-ttu-id="1f6b4-165">(Observação: a especificação de VML não tem um indicador para o `<rect>` elemento.)</span><span class="sxs-lookup"><span data-stu-id="1f6b4-165">(Note: The VML specification doesn't have a bookmark for the `<rect>` element.)</span></span>

<span data-ttu-id="1f6b4-166">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="1f6b4-166">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="roundrect"></a><span data-ttu-id="1f6b4-167">RoundRect</span><span class="sxs-lookup"><span data-stu-id="1f6b4-167">roundrect</span></span>

<span data-ttu-id="1f6b4-168">Você pode usar o `<roundrect>` elemento para desenhar um retângulo com cantos arredondados.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-168">You can use the `<roundrect>` element to draw a rectangle with rounded corners.</span></span> <span data-ttu-id="1f6b4-169">Em seguida, você pode personalizar o retângulo arredondado especificando atributos de propriedade diferentes.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-169">You can then customize the rounded rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="1f6b4-170">Por exemplo, você pode desenhar um retângulo com cantos arredondados 30% da metade da dimensão menor do retângulo, especificando **arcoize**= "0,3", preenchê-lo com amarelo especificando **FillColor**= "amarelo" e dê a ele um contorno vermelho de dois pontos especificando **strokecolor**= "Red" **strokeweight**= "2PT", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="1f6b4-170">For example, you can draw a rectangle that has rounded corners 30% of half the smaller dimension of the rectangle by specifying **arcsize**="0.3", fill it with yellow by specifying **fillcolor**="yellow", and give it a 2-point red outline by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![roundrect1.gif (622 bytes)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="1f6b4-172">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="1f6b4-172">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span>

<span data-ttu-id="1f6b4-173">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="1f6b4-173">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="line"></a><span data-ttu-id="1f6b4-174">line</span><span class="sxs-lookup"><span data-stu-id="1f6b4-174">line</span></span>

<span data-ttu-id="1f6b4-175">Você pode usar o `<line>` elemento para criar uma linha reta.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-175">You can use the `<line>` element to create a straight line.</span></span> <span data-ttu-id="1f6b4-176">Em seguida, você pode personalizar a linha especificando atributos de propriedade diferentes.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-176">You can then customize the line by specifying different property attributes.</span></span>

<span data-ttu-id="1f6b4-177">Por exemplo, você pode desenhar uma linha horizontal especificando **from**= "20pt, 20pt" **to**= "100pt, 20pt" e torná-lo 2 e vermelho especificando **strokecolor**= "Red" **strokeweight**= "2PT", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="1f6b4-177">For example, you can draw a horizontal line by specifying **from**="20pt,20pt" **to**="100pt,20pt", and make it 2-point and red by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![line1.gif (88 bytes)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="1f6b4-179">Você pode desenhar uma linha vertical ou diagonal simplesmente especificando valores diferentes para os atributos **de propriedade from** e **to** , conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="1f6b4-179">You can draw a vertical or diagonal line by simply specifying different values for the **from** and **to** property attributes, as shown in the following VML representation:</span></span>

![line2.gif (86 bytes)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="1f6b4-181">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span><span class="sxs-lookup"><span data-stu-id="1f6b4-181">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span></span>

<span data-ttu-id="1f6b4-182">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="1f6b4-182">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="polyline"></a><span data-ttu-id="1f6b4-183">múltipla</span><span class="sxs-lookup"><span data-stu-id="1f6b4-183">polyline</span></span>

<span data-ttu-id="1f6b4-184">Você pode usar o `<polyline>` elemento para definir formas que são criadas a partir de segmentos de linha conectados.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-184">You can use the `<polyline>` element to define shapes that are created from connected line segments.</span></span> <span data-ttu-id="1f6b4-185">Em seguida, você pode personalizar a forma especificando atributos de propriedade diferentes.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-185">You can then customize the shape by specifying different property attributes.</span></span>

<span data-ttu-id="1f6b4-186">Por exemplo, para desenhar a forma mostrada na imagem a seguir, você pode digitar a seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="1f6b4-186">For example, to draw the shape shown in the following picture, you can type the following VML representation:</span></span>

![polyline1.gif (957 bytes)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="1f6b4-188">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span><span class="sxs-lookup"><span data-stu-id="1f6b4-188">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span></span>

<span data-ttu-id="1f6b4-189">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="1f6b4-189">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="curve"></a><span data-ttu-id="1f6b4-190">curva</span><span class="sxs-lookup"><span data-stu-id="1f6b4-190">curve</span></span>

<span data-ttu-id="1f6b4-191">Você pode usar o `<curve>` elemento para desenhar uma curva Bézier cúbica.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-191">You can use the `<curve>` element to draw a cubic bézier curve.</span></span> <span data-ttu-id="1f6b4-192">Em seguida, você pode personalizar a curva especificando atributos de propriedade diferentes.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-192">You can then customize the curve by specifying different property attributes.</span></span>

<span data-ttu-id="1f6b4-193">Por exemplo, para desenhar uma curva, conforme mostrado na imagem a seguir, você pode digitar a seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="1f6b4-193">For example, to draw a curve as shown in the following picture, you can type the following VML representation:</span></span>

![curve1.gif (992 bytes)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





<span data-ttu-id="1f6b4-195">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span><span class="sxs-lookup"><span data-stu-id="1f6b4-195">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span></span>

<span data-ttu-id="1f6b4-196">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="1f6b4-196">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="arc"></a><span data-ttu-id="1f6b4-197">arco</span><span class="sxs-lookup"><span data-stu-id="1f6b4-197">arc</span></span>

<span data-ttu-id="1f6b4-198">Você pode usar o `<arc>` elemento para desenhar um arco que é definido como um segmento de uma oval.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-198">You can use the `<arc>` element to draw an arc that is defined as a segment of an oval.</span></span> <span data-ttu-id="1f6b4-199">O arco é definido pela interseção da elipse com os vetores RADIUS inicial e final fornecidos pelos ângulos.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-199">The arc is defined by the intersection of the oval with the start and end radius vectors given by the angles.</span></span> <span data-ttu-id="1f6b4-200">Os ângulos são calculados usando as propriedades de um círculo (largura igual à altura) e, em seguida, escalados anisotropicamente para a largura e a altura desejadas.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-200">The angles are calculated by using the properties of a circle (width equal to height), then scaled anisotropically to the desired width and height.</span></span>

<span data-ttu-id="1f6b4-201">Por exemplo, você pode desenhar um arco que começa com 0 graus e termina em 90 graus especificando **StartAngle**= "0" **EndAngle**= "90", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="1f6b4-201">For example, you can draw an arc that starts at 0 degrees and ends at 90 degrees by specifying **startangle**="0" **endangle**="90", as shown in the following VML representation:</span></span>

![arc1.gif (410 bytes)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="1f6b4-203">Você pode alterar o arco especificando diferentes valores de **StartAngle** e de **ângulo de endangular** , conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="1f6b4-203">You can change the arc by specifying different **startangle** and **endangle** values, as shown in the following VML representation:</span></span>

![arc2.gif (608 bytes)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 bytes)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="1f6b4-206">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span><span class="sxs-lookup"><span data-stu-id="1f6b4-206">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span></span>

<span data-ttu-id="1f6b4-207">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="1f6b4-207">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="1f6b4-208">Resumo</span><span class="sxs-lookup"><span data-stu-id="1f6b4-208">Summary</span></span>

<span data-ttu-id="1f6b4-209">Você pode usar elementos predefinidos da VML, como,,,,, `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` e `<arc>` para desenhar gráficos facilmente em uma página da Web e, em seguida, personalizar esses gráficos simplesmente alterando seus atributos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1f6b4-209">You can use VML predefined elements such as `<oval>`, `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` to easily draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span>

 

 