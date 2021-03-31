---
title: Usando o espaço de coordenadas local
description: Usando o espaço de coordenadas local
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Web Workshop, espaço de coordenadas local
- Criando páginas da Web, espaço de coordenadas local
- Linguagem VML (VML), espaço de coordenadas local
- VML (linguagem VML), espaço de coordenadas local
- gráficos vetoriais, espaço de coordenadas local
- espaço de coordenadas local
- Formas de VML, espaço de coordenadas local
- Linguagem VML (VML), agrupamento de formas
- VML (linguagem VML), agrupamento de formas
- gráficos vetoriais, agrupamento de formas
- Formas de VML, agrupamento
- agrupando formas
- Linguagem VML (VML), dimensionar formas
- VML (linguagem VML), dimensionar formas
- gráficos vetoriais, dimensionando formas
- Formas de VML, dimensionamento
- Dimensionando formas
- Linguagem VML (VML), dimensionando formas
- VML (linguagem VML), dimensionando formas
- gráficos vetoriais, dimensionando formas
- Formas de VML, dimensionamento
- Dimensionando formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641708"
---
# <a name="using-local-coordinate-space"></a><span data-ttu-id="08e63-125">Usando o espaço de coordenadas local</span><span class="sxs-lookup"><span data-stu-id="08e63-125">Using Local Coordinate Space</span></span>

<span data-ttu-id="08e63-126">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="08e63-126">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="08e63-127">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="08e63-127">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="08e63-128">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="08e63-128">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="08e63-129">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="08e63-129">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="08e63-130">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="08e63-130">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="08e63-131">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="08e63-131">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="08e63-132">Como você aprendeu, você pode especificar os atributos de estilo de **largura** e **altura** para definir o tamanho de uma caixa contendo dentro da qual o conteúdo de uma forma ou grupo será renderizado.</span><span class="sxs-lookup"><span data-stu-id="08e63-132">As you've learned, you can specify the **width** and **height** style attributes to define the size of a containing box within which the contents of a shape or group will be rendered.</span></span> <span data-ttu-id="08e63-133">Neste tópico, explicaremos o espaço de coordenadas local e como ele é usado em VML para dimensionar formas.</span><span class="sxs-lookup"><span data-stu-id="08e63-133">In this topic, we will explain what Local Coordinate Space is, and how it is used in VML to scale shapes.</span></span>

<span data-ttu-id="08e63-134">Se você foi solicitado a desenhar um retângulo de uma polegada por dois centímetros em um pedaço de papel de grade, a primeira coisa que você descobriria é onde começar (o ponto de origem).</span><span class="sxs-lookup"><span data-stu-id="08e63-134">If you were asked to draw a one-inch by two-inch rectangle on a piece of grid paper, the first thing you would figure out is where to start (the originating point).</span></span> <span data-ttu-id="08e63-135">Em seguida, você descobrirá como mapear uma polegada para as células do papel de grade (a coordenada).</span><span class="sxs-lookup"><span data-stu-id="08e63-135">Then, you would figure out how to map one inch to the cells of the grid paper (the coordinate).</span></span>

<span data-ttu-id="08e63-136">Da mesma forma, quando o conteúdo de uma forma ou grupo é renderizado dentro da caixa que o contém em uma página da Web, o ponto de origem e a coordenada devem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="08e63-136">Similarly, when the contents of a shape or group are rendered inside its containing box on a Web page, the originating point and the coordinate must be defined.</span></span> <span data-ttu-id="08e63-137">A VML fornece espaço de coordenadas local para permitir que cada forma ou grupo defina seu próprio ponto de origem e coordenada.</span><span class="sxs-lookup"><span data-stu-id="08e63-137">VML provides Local Coordinate Space to allow each shape or group to define its own originating point and coordinate.</span></span> <span data-ttu-id="08e63-138">Se você não especificar um espaço de coordenadas, o padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="08e63-138">If you don't specify a coordinate space, the default one will be used.</span></span> <span data-ttu-id="08e63-139">Por padrão, a origem começa no canto superior esquerdo da caixa que o contém.</span><span class="sxs-lookup"><span data-stu-id="08e63-139">By default, the origination starts at the top-left corner of the containing box.</span></span>

<span data-ttu-id="08e63-140">Por exemplo, a representação de VML para a cor vermelha mostrada abaixo não especifica os atributos de propriedade **coordsize** e **coordorigin** .</span><span class="sxs-lookup"><span data-stu-id="08e63-140">For example, the VML representation for the red oval shown below doesn't specify the **coordsize** and **coordorigin** property attributes.</span></span> <span data-ttu-id="08e63-141">Portanto, um espaço de coordenadas local padrão é usado.</span><span class="sxs-lookup"><span data-stu-id="08e63-141">Therefore, a default local coordinate space is used.</span></span> <span data-ttu-id="08e63-142">O tamanho da elipse é de 100 pontos (largura) por 75 pontos (altura).</span><span class="sxs-lookup"><span data-stu-id="08e63-142">The size of the oval is 100 points (width) by 75 points (height).</span></span> <span data-ttu-id="08e63-143">Você pode redimensionar a elipse especificando uma largura ou altura diferente, como você aprendeu no tópico [dimensionar formas](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) .</span><span class="sxs-lookup"><span data-stu-id="08e63-143">You can resize the oval by specifying a different width or height, as you've learned in the [Scale Shapes](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) topic.</span></span>

![oval1.gif (627 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





<span data-ttu-id="08e63-145">Quando a forma se torna mais complicada, ou quando você deseja agrupar várias formas e dimensioná-las juntas, você deve usar o recurso de espaço de coordenadas local fornecido em VML.</span><span class="sxs-lookup"><span data-stu-id="08e63-145">When the shape becomes more complicated, or when you would like to group several shapes and scale them together, you should use the Local Coordinate Space feature provided in VML.</span></span>

<span data-ttu-id="08e63-146">Para cada forma ou grupo, você pode usar os atributos de propriedade **coordsize** e **coordorigin** para definir o espaço de coordenadas local do grupo ou da forma.</span><span class="sxs-lookup"><span data-stu-id="08e63-146">For each shape or group, you can use the **coordsize** and **coordorigin** property attributes to define the shape's or group's local coordinate space.</span></span> <span data-ttu-id="08e63-147">O atributo **coordsize** especifica o número de unidades ao longo da largura e a altura da caixa que a contém.</span><span class="sxs-lookup"><span data-stu-id="08e63-147">The **coordsize** attribute specifies the number of units along the width and the height of the containing box.</span></span> <span data-ttu-id="08e63-148">O atributo **coordorigin** define a coordenada no canto superior esquerdo da caixa que o contém.</span><span class="sxs-lookup"><span data-stu-id="08e63-148">The **coordorigin** attribute defines the coordinate at the top left corner of the containing box.</span></span> <span data-ttu-id="08e63-149">Todas as informações relacionadas à posição (como largura, altura, esquerda, superior, caminho etc.) são expressas em termos da unidade no espaço de coordenadas local.</span><span class="sxs-lookup"><span data-stu-id="08e63-149">All position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span>

<span data-ttu-id="08e63-150">Por exemplo, como mostrado na representação VML a seguir, `width: 100pt; height: 100pt;` define o tamanho da caixa que contém para que a forma seja de 100 pontos por 100 pontos.</span><span class="sxs-lookup"><span data-stu-id="08e63-150">For example, as shown in the following VML representation, `width: 100pt; height: 100pt;` defines the size of the containing box for the shape to be 100 points by 100 points.</span></span>

![cord1.gif (836 bytes)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   <span data-ttu-id="08e63-152">`coordsize="21600,21600"` define o tamanho do espaço de coordenadas local para que a forma seja de 21600 unidades por 21600 unidades.</span><span class="sxs-lookup"><span data-stu-id="08e63-152">`coordsize="21600,21600"` defines the size of the Local Coordinate Space for the shape to be 21600 units by 21600 units.</span></span> <span data-ttu-id="08e63-153">Portanto, uma unidade no espaço de coordenadas local é equivalente a 1/216 pontos.</span><span class="sxs-lookup"><span data-stu-id="08e63-153">Therefore, one unit in the Local Coordinate Space is equivalent to 1/216 point.</span></span>
-   <span data-ttu-id="08e63-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` define o contorno da forma como uma forma de losango.</span><span class="sxs-lookup"><span data-stu-id="08e63-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` defines the outline of the shape as a diamond shape.</span></span> <span data-ttu-id="08e63-155">Como aprendemos, todas as informações relacionadas à posição (como largura, altura, esquerda, superior, caminho etc.) são expressas em termos da unidade no espaço de coordenadas local.</span><span class="sxs-lookup"><span data-stu-id="08e63-155">As we've learned, all position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span> <span data-ttu-id="08e63-156">Portanto, 10800 nos `<path>` significa 10800 unidades, que é equivalente a 50 pontos.</span><span class="sxs-lookup"><span data-stu-id="08e63-156">Therefore, 10800 in the `<path>` means 10800 units, which is equivalent to 50 points.</span></span>

<span data-ttu-id="08e63-157">Quando você quiser redimensionar essa forma de losango, basta especificar uma largura ou altura diferente, isto é, Você não precisa alterar nenhum valor no `<path>` .</span><span class="sxs-lookup"><span data-stu-id="08e63-157">When you want to resize this diamond shape, simply specify a different width or height -- that's it; you don't have to change any value in the `<path>`.</span></span> <span data-ttu-id="08e63-158">Para essa forma complicada, se você não usou o recurso de espaço de coordenadas local, precisaria alterar cada valor no `<path>` sempre que quisesse redimensioná-lo.</span><span class="sxs-lookup"><span data-stu-id="08e63-158">For this complicated shape, if you didn't use the Local Coordinate Space feature, you would have to change every value in the `<path>` whenever you wanted to resize it.</span></span>

<span data-ttu-id="08e63-159">Por exemplo, você pode dimensionar a forma de losango simplesmente especificando uma largura ou altura diferente, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="08e63-159">For example, you can scale the diamond shape by simply specifying a different width or height, as shown in the following VML representation:</span></span>

![cord2.gif (1692 bytes)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





<span data-ttu-id="08e63-161">Você também pode usar o espaço de coordenadas local no `<group>` elemento para que o conteúdo de todas as formas dentro do grupo seja dimensionado em conjunto de acordo com a mesma coordenada.</span><span class="sxs-lookup"><span data-stu-id="08e63-161">You can also use Local Coordinate Space in the `<group>` element so that the contents of all shapes within the group are scaled together according to the same coordinate.</span></span> <span data-ttu-id="08e63-162">Em seguida, sempre que desejar dimensionar ou mover um grupo de formas, basta alterar as configurações de largura e altura, ou **coordsize** e **coordorigin** , do grupo.</span><span class="sxs-lookup"><span data-stu-id="08e63-162">Then, whenever you want to scale or move a group of shapes, simply change the width and height, or **coordsize** and **coordorigin** settings, of the group.</span></span>

<span data-ttu-id="08e63-163">Por exemplo, na representação VML a seguir, `<v:group style='... width:200pt;height:200pt;'>` define o tamanho da caixa que contém para que o grupo seja de 200 pontos por 200 pontos.</span><span class="sxs-lookup"><span data-stu-id="08e63-163">For example, in the following VML representation, `<v:group style='... width:200pt;height:200pt;'>` defines the size of the containing box for the group to be 200 points by 200 points.</span></span>

![cord3.gif (645 bytes)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   <span data-ttu-id="08e63-165">`coordsize="1000,1000"` define o tamanho do espaço de coordenadas local para o grupo ser de 1000 unidades por 1000 unidades.</span><span class="sxs-lookup"><span data-stu-id="08e63-165">`coordsize="1000,1000"` defines the size of the Local Coordinate Space for the group to be 1000 units by 1000 units.</span></span> <span data-ttu-id="08e63-166">Portanto, uma unidade no espaço de coordenadas local é equivalente a 1/5 pontos.</span><span class="sxs-lookup"><span data-stu-id="08e63-166">Therefore, 1 unit in the Local Coordinate Space is equivalent to 1/5 point.</span></span>
-   <span data-ttu-id="08e63-167">`coordorigin="-500,-500"` define o canto superior esquerdo da caixa que o contém como "-500,-500".</span><span class="sxs-lookup"><span data-stu-id="08e63-167">`coordorigin="-500,-500"` defines the top left corner of the containing box to be "-500, -500".</span></span> <span data-ttu-id="08e63-168">Portanto, o sistema de coordenadas dentro da caixa recipiente varia de-500 a 500 ao longo do eixo x e-500 a 500 ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="08e63-168">Therefore, the coordinate system inside the containing box ranges from -500 to 500 along the x-axis, and -500 to 500 along the y-axis.</span></span> <span data-ttu-id="08e63-169">Em outras palavras, o centro da caixa que o contém é "0, 0".</span><span class="sxs-lookup"><span data-stu-id="08e63-169">In other words, the center of the containing box is "0, 0".</span></span>
-   <span data-ttu-id="08e63-170">`<v:oval style='... width:400;height:300;'>` define o tamanho da caixa que contém para que a oval vermelha seja de 400 unidades (largura) por 300 unidades (altura).</span><span class="sxs-lookup"><span data-stu-id="08e63-170">`<v:oval style='... width:400;height:300;'>` defines the size of the containing box for the red oval to be 400 units (width) by 300 units (height).</span></span> <span data-ttu-id="08e63-171">Como uma unidade no espaço de coordenadas local é equivalente ao ponto de 1/5, o tamanho da caixa de conteúdo da oval vermelha é de 80 pontos (largura) por 60 pontos (altura).</span><span class="sxs-lookup"><span data-stu-id="08e63-171">Because one unit in the Local Coordinate Space is equivalent to 1/5 point, the size of the containing box for the red oval is 80 points (width) by 60 points (height).</span></span>

<span data-ttu-id="08e63-172">Da mesma forma, o tamanho da caixa que a contém para o RoundRect verde é de 50 pontos (largura) por 40 pontos (altura).</span><span class="sxs-lookup"><span data-stu-id="08e63-172">Similarly, the size of the containing box for the green roundrect is 50 points (width) by 40 points (height).</span></span>

<span data-ttu-id="08e63-173">Quando você quiser redimensionar a elipse vermelha e a RoundRect verde, basta alterar `<v:group style='... width:200pt;height:200pt;'>` .</span><span class="sxs-lookup"><span data-stu-id="08e63-173">When you want to to resize both the red oval and the green roundrect, simply change `<v:group style='... width:200pt;height:200pt;'>`.</span></span> <span data-ttu-id="08e63-174">É isso – você não precisa alterar o tamanho das duas formas individualmente.</span><span class="sxs-lookup"><span data-stu-id="08e63-174">That's it -- you don't have to individually change the size of the two shapes.</span></span>

<span data-ttu-id="08e63-175">Por exemplo, se você alterar `<v:group style='... width:200pt;height:200pt;'>` para `<v:group style='... width:300pt;height:300pt;'>` , as formas se tornarão maiores, conforme mostrado na figura a seguir:</span><span class="sxs-lookup"><span data-stu-id="08e63-175">For example, if you change `<v:group style='... width:200pt;height:200pt;'>` to `<v:group style='... width:300pt;height:300pt;'>`, the shapes become larger, as shown in the following picture:</span></span>

![cord4.gif (943 bytes)](images/cord4.gif)



<span data-ttu-id="08e63-177">Você também observaria que as formas estão localizadas de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="08e63-177">You'd also notice that the shapes are located differently.</span></span> <span data-ttu-id="08e63-178">Isso ocorre porque as formas são desenhadas de "0, 0" que está localizado no centro da caixa que o contém.</span><span class="sxs-lookup"><span data-stu-id="08e63-178">This is because the shapes are drawn from "0, 0" which is located at the center of the containing box.</span></span> <span data-ttu-id="08e63-179">Como você torna a caixa de conteúdo maior, o centro da caixa que a contém também é movido.</span><span class="sxs-lookup"><span data-stu-id="08e63-179">Because you make the containing box bigger, the center of the containing box is also moved.</span></span>

<span data-ttu-id="08e63-180">Se você alterar `coordorigin="-500,-500"` para `coordorigin="0,0"` , conforme mostrado na imagem a seguir, observará que a elipse vermelha e as RoundRect verdes são deslocadas para o novo local.</span><span class="sxs-lookup"><span data-stu-id="08e63-180">If you change `coordorigin="-500,-500"` to `coordorigin="0,0"`, as shown in the following picture, you'll notice that the red oval and the green roundrect are both shifted up to the new location.</span></span> <span data-ttu-id="08e63-181">Isso ocorre porque "0, 0" Agora localiza no canto superior esquerdo da caixa que o contém.</span><span class="sxs-lookup"><span data-stu-id="08e63-181">This is because "0, 0" now locates at the top left corner of the containing box.</span></span>

![cord5.gif (648 bytes)](images/cord5.gif)



<span data-ttu-id="08e63-183">Também é importante observar que a caixa que o contém não estabelece uma região de recorte.</span><span class="sxs-lookup"><span data-stu-id="08e63-183">It is also important to note that the containing box does not establish a clipping region.</span></span> <span data-ttu-id="08e63-184">Os gráficos podem ser desenhados fora dos limites da caixa que o contém.</span><span class="sxs-lookup"><span data-stu-id="08e63-184">Graphics may be drawn outside the boundaries of the containing box.</span></span> <span data-ttu-id="08e63-185">A caixa que o contém simplesmente serve para mapear o espaço de coordenadas local para o espaço da página.</span><span class="sxs-lookup"><span data-stu-id="08e63-185">The containing box merely serves to map the local coordinate space to the page space.</span></span>

<span data-ttu-id="08e63-186">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span><span class="sxs-lookup"><span data-stu-id="08e63-186">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span></span>

 

 