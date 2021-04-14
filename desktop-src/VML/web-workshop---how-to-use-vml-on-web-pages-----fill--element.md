---
title: Usar o elemento Fill
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Web Workshop, elemento Fill
- Criando páginas da Web, elemento Fill
- Linguagem VML (VML), elemento Fill
- VML (linguagem VML), elemento Fill
- gráfico vetorial, elemento Fill
- elemento Fill
- Elementos de VML, preenchimento
- Formas de VML, elemento Fill
- Linguagem VML (VML), preenchimento gradual
- VML (linguagem VML), preenchimento gradual
- gráficos vetoriais, preenchimento gradual
- Formas de VML, preenchimento gradual
- formas preenchidas com gradiente
- Linguagem VML (VML), preenchimento de padrão
- VML (linguagem VML), preenchimento de padrão
- gráficos vetoriais, preenchimento de padrão
- Formas de VML, preenchimento de padrão
- formas preenchidas por padrão
- Linguagem VML (VML), preenchimento de imagem
- VML (linguagem VML), preenchimento de imagem
- gráficos vetoriais, preenchimento de imagem
- Formas de VML, preenchimento de imagem
- formas preenchidas por imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf497a3120f53e24f1cff2bf7084469754bbaf7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104552511"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="35d27-127">Usar o elemento Fill</span><span class="sxs-lookup"><span data-stu-id="35d27-127">Using the Fill Element</span></span>

<span data-ttu-id="35d27-128">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="35d27-128">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="35d27-129">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="35d27-129">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="35d27-130">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="35d27-130">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="35d27-131">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="35d27-131">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="35d27-132">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="35d27-132">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="35d27-133">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="35d27-133">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="35d27-134">Como você aprendeu, você pode usar o atributo da propriedade **FillColor** de um elemento Shape predefinido, como,,,,, `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` , `<arc>` --para especificar a cor usada para preencher a forma.</span><span class="sxs-lookup"><span data-stu-id="35d27-134">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="35d27-135">Neste tópico, Ilustraremos como desenhar uma forma que é preenchida com efeitos mais avançados.</span><span class="sxs-lookup"><span data-stu-id="35d27-135">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="35d27-136">Você pode posicionar o `<fill>` subelemento dentro do `<shape>` , ou `<shapetype>` ou qualquer elemento Shape predefinido para descrever como preencher a forma.</span><span class="sxs-lookup"><span data-stu-id="35d27-136">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="35d27-137">Você pode usar os atributos de Propriedade do `<fill>` subelemento para personalizar o efeito de preenchimento, como preenchimento de [gradiente](#gradient-fill), [preenchimento de padrão](#pattern-fill), [preenchimento de imagem](#picture-fill).</span><span class="sxs-lookup"><span data-stu-id="35d27-137">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="35d27-138">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="35d27-138">In this topic:</span></span>

-   [<span data-ttu-id="35d27-139">Preenchimento gradual</span><span class="sxs-lookup"><span data-stu-id="35d27-139">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="35d27-140">Preenchimento de padrão</span><span class="sxs-lookup"><span data-stu-id="35d27-140">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="35d27-141">Preenchimento de imagem</span><span class="sxs-lookup"><span data-stu-id="35d27-141">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="35d27-142">Preenchimento gradual</span><span class="sxs-lookup"><span data-stu-id="35d27-142">Gradient Fill</span></span>

<span data-ttu-id="35d27-143">Para desenhar uma forma preenchida com gradiente, você pode definir o atributo de propriedade **Type** do `<fill>` subelemento como "gradation" ou "gradientRadial" e, em seguida, especificar outros atributos de Propriedade do `<fill>` subelemento, como **Method**, **color2**, **Focus** e **Angle**.</span><span class="sxs-lookup"><span data-stu-id="35d27-143">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="35d27-144">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="35d27-144">**Examples:**</span></span>

<span data-ttu-id="35d27-145">Para criar uma forma que seja preenchida com gradiente horizontalmente, você pode definir o atributo da propriedade **Type** como "gradation", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="35d27-145">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 bytes)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="35d27-147">Se você alterar o atributo da propriedade **FillColor** da forma, a forma será preenchida com gradiente com uma cor diferente.</span><span class="sxs-lookup"><span data-stu-id="35d27-147">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="35d27-148">Você pode adicionar uma segunda cor especificando o atributo de propriedade **color2** do `<fill>` subelemento.</span><span class="sxs-lookup"><span data-stu-id="35d27-148">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="35d27-149">Por exemplo, para criar uma forma que seja preenchida com gradiente em duas cores, você pode adicionar uma segunda cor especificando o atributo da propriedade **color2** do `<fill>` subelemento, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="35d27-149">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 bytes)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="35d27-151">Você pode definir o atributo de Propriedade do **método** como "linear" ou "Sigma" ou "any" ou "None".</span><span class="sxs-lookup"><span data-stu-id="35d27-151">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="35d27-152">O efeito do gradiente é ligeiramente diferente.</span><span class="sxs-lookup"><span data-stu-id="35d27-152">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="35d27-153">Além disso, você pode usar o atributo de propriedade **Angle**,**Focus**,**focussize** ou **focusposition** para alterar a forma como o gradiente é.</span><span class="sxs-lookup"><span data-stu-id="35d27-153">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="35d27-154">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="35d27-154">**Examples:**</span></span>

 

<span data-ttu-id="35d27-155">Para criar uma forma que seja preenchida com gradiente verticalmente, você pode definir o atributo de Propriedade Angle como Angle = "-90", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="35d27-155">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 bytes)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="35d27-157">Para criar uma forma que seja preenchida com gradiente da diagonal se movendo para cima, você pode definir o atributo de propriedade **Angle** como Angle = "-135", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="35d27-157">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 bytes)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="35d27-159">Para criar uma forma que seja preenchida com gradiente de uma diagonal para baixo, você pode definir o atributo de propriedade **Angle** como Angle = "-45", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="35d27-159">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 bytes)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="35d27-161">Para criar uma forma que seja preenchida com gradiente do centro, você pode especificar `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="35d27-161">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 bytes)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="35d27-163">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="35d27-163">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="35d27-164">Preenchimento de padrão</span><span class="sxs-lookup"><span data-stu-id="35d27-164">Pattern Fill</span></span>

<span data-ttu-id="35d27-165">Para desenhar uma forma preenchida por padrão, você pode definir o atributo de propriedade **Type** do `<fill>` subelemento como "Pattern" e, em seguida, especificar outros atributos de Propriedade do `<fill>` subelemento, como **src** e **color2**.</span><span class="sxs-lookup"><span data-stu-id="35d27-165">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="35d27-166">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="35d27-166">**Examples:**</span></span>

<span data-ttu-id="35d27-167">Para criar uma forma que é preenchida com uma imagem de padrão, você pode especificar o atributo de propriedade **Type** como "Pattern" e apontar o atributo de propriedade **src** para o local do arquivo de imagem de padrão, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="35d27-167">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 bytes)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="35d27-169">Se você apontar o atributo de propriedade **src** para um arquivo de padrão diferente, poderá criar uma forma que é preenchida com um padrão diferente.</span><span class="sxs-lookup"><span data-stu-id="35d27-169">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="35d27-170">Além disso, você pode alterar a cor especificando um valor diferente para o atributo de propriedade **FillColor** ou **color2** , conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="35d27-170">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 bytes)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="35d27-172">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="35d27-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="35d27-173">Preenchimento de imagem</span><span class="sxs-lookup"><span data-stu-id="35d27-173">Picture Fill</span></span>

<span data-ttu-id="35d27-174">Para desenhar uma forma preenchida por imagem, você pode definir o atributo de propriedade **Type** do `<fill>` subelemento como "frame" e, em seguida, especificar outros atributos de Propriedade do `<fill>` subelemento, como **src** e **color2**.</span><span class="sxs-lookup"><span data-stu-id="35d27-174">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="35d27-175">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="35d27-175">**Examples:**</span></span>

<span data-ttu-id="35d27-176">Para criar uma forma que é preenchida com um arquivo de imagem, você pode especificar o atributo de propriedade **Type** como "frame" e, em seguida, apontar o atributo de propriedade **src** para o local do arquivo de imagem, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="35d27-176">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 bytes)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="35d27-178">Você pode criar facilmente uma forma que é preenchida com uma imagem diferente apontando o atributo de propriedade **src** para outro arquivo.</span><span class="sxs-lookup"><span data-stu-id="35d27-178">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="35d27-179">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span><span class="sxs-lookup"><span data-stu-id="35d27-179">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 