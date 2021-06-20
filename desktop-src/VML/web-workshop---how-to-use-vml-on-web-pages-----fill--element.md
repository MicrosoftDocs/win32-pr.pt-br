---
title: Usar o elemento Fill
description: Este artigo descreve como usar o elemento Fill do VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
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
ms.openlocfilehash: ecb243e4896443fd36a1b22c2ac3a0ab0bedfb2b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407789"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="95a7a-126">Usar o elemento Fill</span><span class="sxs-lookup"><span data-stu-id="95a7a-126">Using the Fill Element</span></span>

<span data-ttu-id="95a7a-127">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="95a7a-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="95a7a-128">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="95a7a-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="95a7a-129">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="95a7a-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="95a7a-130">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="95a7a-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="95a7a-131">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="95a7a-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="95a7a-132">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="95a7a-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="95a7a-133">Como você aprendeu, você pode usar o atributo da propriedade **FillColor** de um elemento Shape predefinido, como,,,,, `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` , `<arc>` --para especificar a cor usada para preencher a forma.</span><span class="sxs-lookup"><span data-stu-id="95a7a-133">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="95a7a-134">Neste tópico, Ilustraremos como desenhar uma forma que é preenchida com efeitos mais avançados.</span><span class="sxs-lookup"><span data-stu-id="95a7a-134">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="95a7a-135">Você pode posicionar o `<fill>` subelemento dentro do `<shape>` , ou `<shapetype>` ou qualquer elemento Shape predefinido para descrever como preencher a forma.</span><span class="sxs-lookup"><span data-stu-id="95a7a-135">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="95a7a-136">Você pode usar os atributos de Propriedade do `<fill>` subelemento para personalizar o efeito de preenchimento, como preenchimento de [gradiente](#gradient-fill), [preenchimento de padrão](#pattern-fill), [preenchimento de imagem](#picture-fill).</span><span class="sxs-lookup"><span data-stu-id="95a7a-136">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="95a7a-137">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="95a7a-137">In this topic:</span></span>

-   [<span data-ttu-id="95a7a-138">Preenchimento gradual</span><span class="sxs-lookup"><span data-stu-id="95a7a-138">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="95a7a-139">Preenchimento de padrão</span><span class="sxs-lookup"><span data-stu-id="95a7a-139">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="95a7a-140">Preenchimento de imagem</span><span class="sxs-lookup"><span data-stu-id="95a7a-140">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="95a7a-141">Preenchimento gradual</span><span class="sxs-lookup"><span data-stu-id="95a7a-141">Gradient Fill</span></span>

<span data-ttu-id="95a7a-142">Para desenhar uma forma preenchida com gradiente, você pode definir o atributo de propriedade **Type** do `<fill>` subelemento como "gradation" ou "gradientRadial" e, em seguida, especificar outros atributos de Propriedade do `<fill>` subelemento, como **Method**, **color2**, **Focus** e **Angle**.</span><span class="sxs-lookup"><span data-stu-id="95a7a-142">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="95a7a-143">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="95a7a-143">**Examples:**</span></span>

<span data-ttu-id="95a7a-144">Para criar uma forma que seja preenchida com gradiente horizontalmente, você pode definir o atributo da propriedade **Type** como "gradation", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="95a7a-144">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 bytes)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="95a7a-146">Se você alterar o atributo da propriedade **FillColor** da forma, a forma será preenchida com gradiente com uma cor diferente.</span><span class="sxs-lookup"><span data-stu-id="95a7a-146">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="95a7a-147">Você pode adicionar uma segunda cor especificando o atributo de propriedade **color2** do `<fill>` subelemento.</span><span class="sxs-lookup"><span data-stu-id="95a7a-147">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="95a7a-148">Por exemplo, para criar uma forma que seja preenchida com gradiente em duas cores, você pode adicionar uma segunda cor especificando o atributo da propriedade **color2** do `<fill>` subelemento, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="95a7a-148">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 bytes)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="95a7a-150">Você pode definir o atributo de Propriedade do **método** como "linear" ou "Sigma" ou "any" ou "None".</span><span class="sxs-lookup"><span data-stu-id="95a7a-150">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="95a7a-151">O efeito do gradiente é ligeiramente diferente.</span><span class="sxs-lookup"><span data-stu-id="95a7a-151">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="95a7a-152">Além disso, você pode usar o atributo de propriedade **Angle**,**Focus**,**focussize** ou **focusposition** para alterar a forma como o gradiente é.</span><span class="sxs-lookup"><span data-stu-id="95a7a-152">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="95a7a-153">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="95a7a-153">**Examples:**</span></span>

 

<span data-ttu-id="95a7a-154">Para criar uma forma que seja preenchida com gradiente verticalmente, você pode definir o atributo de Propriedade Angle como Angle = "-90", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="95a7a-154">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 bytes)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="95a7a-156">Para criar uma forma que seja preenchida com gradiente da diagonal se movendo para cima, você pode definir o atributo de propriedade **Angle** como Angle = "-135", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="95a7a-156">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 bytes)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="95a7a-158">Para criar uma forma que seja preenchida com gradiente de uma diagonal para baixo, você pode definir o atributo de propriedade **Angle** como Angle = "-45", conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="95a7a-158">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 bytes)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="95a7a-160">Para criar uma forma que seja preenchida com gradiente do centro, você pode especificar `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="95a7a-160">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 bytes)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="95a7a-162">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="95a7a-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="95a7a-163">Preenchimento de padrão</span><span class="sxs-lookup"><span data-stu-id="95a7a-163">Pattern Fill</span></span>

<span data-ttu-id="95a7a-164">Para desenhar uma forma preenchida por padrão, você pode definir o atributo de propriedade **Type** do `<fill>` subelemento como "Pattern" e, em seguida, especificar outros atributos de Propriedade do `<fill>` subelemento, como **src** e **color2**.</span><span class="sxs-lookup"><span data-stu-id="95a7a-164">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="95a7a-165">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="95a7a-165">**Examples:**</span></span>

<span data-ttu-id="95a7a-166">Para criar uma forma que é preenchida com uma imagem de padrão, você pode especificar o atributo de propriedade **Type** como "Pattern" e apontar o atributo de propriedade **src** para o local do arquivo de imagem de padrão, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="95a7a-166">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 bytes)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="95a7a-168">Se você apontar o atributo de propriedade **src** para um arquivo de padrão diferente, poderá criar uma forma que é preenchida com um padrão diferente.</span><span class="sxs-lookup"><span data-stu-id="95a7a-168">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="95a7a-169">Além disso, você pode alterar a cor especificando um valor diferente para o atributo de propriedade **FillColor** ou **color2** , conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="95a7a-169">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 bytes)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="95a7a-171">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="95a7a-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="95a7a-172">Preenchimento de imagem</span><span class="sxs-lookup"><span data-stu-id="95a7a-172">Picture Fill</span></span>

<span data-ttu-id="95a7a-173">Para desenhar uma forma preenchida por imagem, você pode definir o atributo de propriedade **Type** do `<fill>` subelemento como "frame" e, em seguida, especificar outros atributos de Propriedade do `<fill>` subelemento, como **src** e **color2**.</span><span class="sxs-lookup"><span data-stu-id="95a7a-173">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="95a7a-174">**Exemplos:**</span><span class="sxs-lookup"><span data-stu-id="95a7a-174">**Examples:**</span></span>

<span data-ttu-id="95a7a-175">Para criar uma forma que é preenchida com um arquivo de imagem, você pode especificar o atributo de propriedade **Type** como "frame" e, em seguida, apontar o atributo de propriedade **src** para o local do arquivo de imagem, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="95a7a-175">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 bytes)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="95a7a-177">Você pode criar facilmente uma forma que é preenchida com uma imagem diferente apontando o atributo de propriedade **src** para outro arquivo.</span><span class="sxs-lookup"><span data-stu-id="95a7a-177">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="95a7a-178">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span><span class="sxs-lookup"><span data-stu-id="95a7a-178">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 