---
title: Formas de cores
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Web Workshop, formas de cores
- Criando páginas da Web, formas de cores
- Linguagem VML (VML), formas de cores
- VML (linguagem VML), formas de cor
- gráficos vetoriais, formas de cores
- Formas de VML, coloração
- formas de cores
- Linguagem VML (VML), nomes de cor de palavra-chave
- VML (linguagem VML), nomes de cor de palavra-chave
- gráficos vetoriais, nomes de cor de palavra-chave
- nomes de cor de palavra-chave
- Linguagem VML (VML), RGB tercetos
- VML (linguagem VML), RGB tercetos
- gráficos vetoriais, tercetos RGB
- Tercetos RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1257c5f5b0cf8021658820f09de6e87099f0a52b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007851"
---
# <a name="coloring-shapes"></a><span data-ttu-id="8b8a7-119">Formas de cores</span><span class="sxs-lookup"><span data-stu-id="8b8a7-119">Coloring Shapes</span></span>

<span data-ttu-id="8b8a7-120">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-120">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8b8a7-121">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-121">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8b8a7-122">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-122">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8b8a7-123">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-123">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8b8a7-124">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8b8a7-124">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8b8a7-125">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8b8a7-125">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8b8a7-126">Como mencionamos nas seções anteriores, você pode usar "vermelho" para representar uma cor em vermelho, "azul" para representar uma cor em azul e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-126">As we mentioned in earlier sections, you can use "red" to represent a color in red, "blue" to represent a color in blue, and so on.</span></span> <span data-ttu-id="8b8a7-127">Neste tópico, Ilustraremos como desenhar formas de qualquer cor desejada.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-127">In this topic, we will illustrate how to draw shapes in any color you want.</span></span>

<span data-ttu-id="8b8a7-128">A VML estende a sintaxe de cor HTML e CSS.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-128">VML extends HTML and CSS color syntax.</span></span> <span data-ttu-id="8b8a7-129">Quando o tipo de atributo de um elemento VML é Color--como **FillColor** e **strokecolor** , você pode expressar a cor usando um [nome de cor de palavra-chave](#keyword-color-name) ou um [terceto RGB](#rgb-triplet).</span><span class="sxs-lookup"><span data-stu-id="8b8a7-129">When the attribute type of a VML element is color -- such as **fillcolor** and **strokecolor** -- you can express the color by using either a [keyword color name](#keyword-color-name) or an [RGB triplet](#rgb-triplet).</span></span>

<span data-ttu-id="8b8a7-130">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="8b8a7-130">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="keyword-color-name"></a><span data-ttu-id="8b8a7-131">Nome da cor da palavra-chave</span><span class="sxs-lookup"><span data-stu-id="8b8a7-131">Keyword Color Name</span></span>

<span data-ttu-id="8b8a7-132">O HTML 4,0 define uma lista de nomes de cor de palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-132">HTML 4.0 defines a list of keyword color names.</span></span> <span data-ttu-id="8b8a7-133">Eles são azul-piscina, preto, azul, Fuchsia, cinza, verde, limão, bordô, marrom, verde-oliva, roxo, vermelho, prata, azul-petróleo, branco e amarelo.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-133">They are aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, and yellow.</span></span> <span data-ttu-id="8b8a7-134">O valor RGB para essas 16 cores é definido na [especificação de HTML 4,0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span><span class="sxs-lookup"><span data-stu-id="8b8a7-134">The RGB value for these 16 colors are defined in [HTML 4.0 specification](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span></span>

<span data-ttu-id="8b8a7-135">Por exemplo, você pode desenhar um retângulo preenchido com amarelo especificando e `fillcolor="yellow"` dar a ele um contorno azul especificando `strokecolor="blue"` , conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="8b8a7-135">For example, you can draw a rectangle filled with yellow by specifying `fillcolor="yellow"`, and give it a blue outline by specifying `strokecolor="blue"`, as shown in the following VML representation:</span></span>

![color1.gif (305 bytes)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





<span data-ttu-id="8b8a7-137">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="8b8a7-137">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rgb-triplet"></a><span data-ttu-id="8b8a7-138">Terceto RGB</span><span class="sxs-lookup"><span data-stu-id="8b8a7-138">RGB Triplet</span></span>

<span data-ttu-id="8b8a7-139">Se a cor não for um [nome de cor de palavra-chave](#keyword-color-name), você poderá expressar a cor como uma TERCETO decimal RGB ou um TERCETO hexadecimal RGB.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-139">If the color is not a [keyword color name](#keyword-color-name), you can express the color as either an RGB decimal triplet or an RGB hexadecimal triplet.</span></span> <span data-ttu-id="8b8a7-140">Com o tercetos RGB, você pode especificar valores para os componentes vermelho, verde e azul da cor, definindo cada componente com um valor que varia de 0 a 255 em decimal, ou 00 a FF em hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-140">With RGB triplets, you can specify values for the red, green, and blue components of the color, setting each component to a value ranging from 0 through 255 in decimal, or 00 through FF in hexadecimal.</span></span>

<span data-ttu-id="8b8a7-141">Por exemplo, você pode criar um retângulo que é preenchido com uma cor personalizada com um valor RGB de 253, 249, 186 em decimal especificando `fillcolor="rgb(253,249, 186)"` ou `fillcolor="#FDF9BA"` , conforme mostrado na representação de VML a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-141">For example, you can create a rectangle that is filled with a customized color with an RGB value of 253, 249, 186 in decimal by specifying either `fillcolor="rgb(253,249, 186)"` or `fillcolor="#FDF9BA"`, as shown in the following VML representation.</span></span> <span data-ttu-id="8b8a7-142">Em hexadecimal, o valor 253 torna-se FD, 249 torna-se F9 e 186 se torna BA.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-142">In hexadecimal, the value 253 becomes FD, 249 becomes F9, and 186 becomes BA.</span></span>

![color2.gif (305 bytes)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





<span data-ttu-id="8b8a7-144">Se o RGB em hexadecimal tiver um padrão como XXYYZZ, você poderá abreviar isso como XYZ.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-144">If the RGB in hexadecimal has a pattern such as XXYYZZ, you can abbreviate it to XYZ.</span></span> <span data-ttu-id="8b8a7-145">Por exemplo, " \# 66FF99" pode ser escrito como " \# 6F9".</span><span class="sxs-lookup"><span data-stu-id="8b8a7-145">For example, "\#66FF99" can be written out as "\#6F9".</span></span>

<span data-ttu-id="8b8a7-146">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="8b8a7-146">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="8b8a7-147">Resumo</span><span class="sxs-lookup"><span data-stu-id="8b8a7-147">Summary</span></span>

<span data-ttu-id="8b8a7-148">Na VML, você pode representar uma cor em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="8b8a7-148">In VML, you can represent a color in one of the following formats:</span></span>

1.  <span data-ttu-id="8b8a7-149">FillColor = "Blue"</span><span class="sxs-lookup"><span data-stu-id="8b8a7-149">fillcolor="blue"</span></span>
2.  <span data-ttu-id="8b8a7-150">FillColor = "RGB (0, 0255)"</span><span class="sxs-lookup"><span data-stu-id="8b8a7-150">fillcolor="rgb(0,0,255)"</span></span>
3.  <span data-ttu-id="8b8a7-151">FillColor = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="8b8a7-151">fillcolor="\#0000ff"</span></span>

 

 