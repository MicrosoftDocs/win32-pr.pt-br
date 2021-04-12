---
title: Usando o elemento Image
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Web Workshop, elemento Image
- Criando páginas da Web, elemento Image
- Linguagem VML (VML), elemento Image
- VML (linguagem VML), elemento Image
- gráficos vetoriais, elemento Image
- elemento de imagem
- Elementos de VML, imagem
- Formas de VML, elemento Image
- Linguagem VML (VML), atributos de propriedade de corte
- VML (linguagem VML), atributos de propriedade de corte
- gráficos vetoriais, atributos de propriedade de corte
- Formas de VML, atributos de propriedade de corte
- cortar atributos de propriedade
- Linguagem VML (VML), obter atributo de propriedade
- VML (linguagem VML), obter atributo de propriedade
- gráfico vetorial, obter atributo de propriedade
- Formas de VML, obter atributo de propriedade
- obter atributo de propriedade
- Linguagem VML (VML), contraste
- VML (linguagem VML), contraste
- gráficos vetoriais, contraste
- Formas de VML, contraste
- Linguagem VML (VML), atributo de propriedade blacklevel
- VML (linguagem VML), atributo de propriedade blacklevel
- gráficos vetoriais, atributo de propriedade blacklevel
- Formas de VML, atributo de propriedade blacklevel
- atributo de propriedade blacklevel
- Linguagem VML (VML), brilho
- VML (linguagem VML), brilho
- gráficos vetoriais, brilho
- Formas de VML, brilho
- Linguagem VML (VML), atributo de propriedade de escala de cinza
- VML (linguagem VML), atributo de propriedade de escala de cinza
- gráficos vetoriais, atributo de propriedade tons de cinza
- Formas de VML, atributo de propriedade de escala de cinza
- atributo de propriedade de escala de cinza
- Linguagem VML (VML), atributo de propriedade gama
- VML (linguagem VML), atributo de propriedade gama
- gráficos vetoriais, atributo de propriedade gama
- Formas de VML, atributo de propriedade gama
- atributo de propriedade gama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820039ff76f3685eeea7a65e2bbc01578abbe581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499131"
---
# <a name="using-the-image-element"></a><span data-ttu-id="74916-145">Usando o elemento Image</span><span class="sxs-lookup"><span data-stu-id="74916-145">Using the Image Element</span></span>

<span data-ttu-id="74916-146">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="74916-146">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="74916-147">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="74916-147">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="74916-148">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="74916-148">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="74916-149">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="74916-149">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="74916-150">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="74916-150">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="74916-151">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="74916-151">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="74916-152">Usando `<image>`</span><span class="sxs-lookup"><span data-stu-id="74916-152">Using `<image>`</span></span>

<span data-ttu-id="74916-153">Neste tópico, Ilustraremos como usar o `<image>` elemento para exibir imagens com vários efeitos especiais.</span><span class="sxs-lookup"><span data-stu-id="74916-153">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="74916-154">Se você quisesse exibir uma imagem que foi carregada a partir de uma fonte externa, normalmente usaria o `<img>` elemento fornecido em HTML e, em seguida, apontaria o atributo de propriedade **src** para o local do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="74916-154">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="74916-155">Como alternativa, você pode usar o `<image>` elemento fornecido em VML.</span><span class="sxs-lookup"><span data-stu-id="74916-155">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="74916-156">Ao usar o `<image>` elemento, você pode criar apenas um arquivo de imagem e, em seguida, exibir a imagem de maneira diferente alterando os atributos de Propriedade do `<image>` elemento.</span><span class="sxs-lookup"><span data-stu-id="74916-156">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="74916-157">Além disso, `<image>` o elemento fornece vários efeitos especiais que você não pode fazer simplesmente usando o `<img>` elemento de HTML, como [corte](#crop), [contraste](#contrast), [brilho](#brightness), [gama](#gamma)e [escala de cinza](#grayscale).</span><span class="sxs-lookup"><span data-stu-id="74916-157">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="74916-158">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="74916-158">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="74916-159">cortar</span><span class="sxs-lookup"><span data-stu-id="74916-159">crop</span></span>

<span data-ttu-id="74916-160">Você pode usar os atributos de propriedade **cropbottom**, **croptop**, **CropLeft** e **CropRight** do `<image>` elemento para exibir imagens diferentes que são cortadas do mesmo arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="74916-160">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="74916-161">O valor desses atributos de corte representa a porcentagem de recorte da borda da imagem.</span><span class="sxs-lookup"><span data-stu-id="74916-161">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="74916-162">O valor pode ser qualquer número entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="74916-162">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="74916-163">Por padrão, o valor é definido como 0, indicando que não há nenhum corte na borda.</span><span class="sxs-lookup"><span data-stu-id="74916-163">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="74916-164">O valor 0,1 indica um corte de 10 por cento da borda, o valor 0,15 indica um corte de 15 por cento a partir da borda e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="74916-164">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="74916-165">Por exemplo, para exibir cinco imagens que são todas cortadas do mesmo arquivo de imagem, você pode usar o `<image>` elemento e especificar valores de corte diferentes, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="74916-165">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image1 (1969 bytes)](images/image1-2.jpg)![\-3.jpg image1 (1148 bytes)](images/image1-3.jpg)![\-4.jpg image1 (1686 bytes)](images/image1-4.jpg)![\-5.jpg image1 (1364 bytes)](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





<span data-ttu-id="74916-171">A primeira imagem, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , não tem nenhum valor de corte.</span><span class="sxs-lookup"><span data-stu-id="74916-171">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="74916-172">Portanto, 100% da imagem original é exibido em um tamanho de 100 pontos por 80 pontos.</span><span class="sxs-lookup"><span data-stu-id="74916-172">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="74916-173">A segunda imagem, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , tem alguns valores de corte.</span><span class="sxs-lookup"><span data-stu-id="74916-173">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="74916-174">`cropbottom="0.2"` indica que 20 por cento da imagem serão cortados da parte inferior; `cropright="0.15"` indica que 15 por cento da imagem será cortado da borda direita.</span><span class="sxs-lookup"><span data-stu-id="74916-174">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="74916-175">A imagem restante é exibida em um tamanho de 85 pontos por 64 pontos.</span><span class="sxs-lookup"><span data-stu-id="74916-175">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="74916-176">Da mesma forma, a terceira, a quarta e a quinta imagens têm alguns valores de corte.</span><span class="sxs-lookup"><span data-stu-id="74916-176">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="74916-177">A imagem original é cortada de acordo com os valores de corte e, em seguida, é exibida de acordo com o valor de largura e altura.</span><span class="sxs-lookup"><span data-stu-id="74916-177">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="74916-178">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="74916-178">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="74916-179">contraste</span><span class="sxs-lookup"><span data-stu-id="74916-179">contrast</span></span>

<span data-ttu-id="74916-180">Você pode usar o atributo **obter** Propriedade do `<image>` elemento para exibir várias imagens que têm configurações de contraste diferentes.</span><span class="sxs-lookup"><span data-stu-id="74916-180">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="74916-181">O valor do atributo de propriedade de **obter** pode ser qualquer número.</span><span class="sxs-lookup"><span data-stu-id="74916-181">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="74916-182">Por padrão, o valor é 1, indicando o uso do mesmo contraste da imagem original.</span><span class="sxs-lookup"><span data-stu-id="74916-182">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="74916-183">O valor 0 indica sem contraste.</span><span class="sxs-lookup"><span data-stu-id="74916-183">The value 0 indicates no contrast.</span></span> <span data-ttu-id="74916-184">Quanto maior o número, maior o contraste.</span><span class="sxs-lookup"><span data-stu-id="74916-184">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="74916-185">Por exemplo, para exibir cinco imagens que têm configurações de contraste diferentes, você pode usar o `<image>` elemento e definir um valor diferente para o atributo de propriedade de **obter** , conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="74916-185">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image2 (270 bytes)](images/image2-2.jpg)![\-3.jpg image2 (1919 bytes)](images/image2-3.jpg)![\-4.jpg image2 (3143 bytes)](images/image2-4.jpg)![\-5.jpg image2 (1724 bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="74916-191">Quando o atributo de propriedade de **obter** é definido como 0, a imagem inteira torna-se cinza porque não há contraste.</span><span class="sxs-lookup"><span data-stu-id="74916-191">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="74916-192">O contraste é mais perceptível quando o atributo de propriedade de **obter** é definido como 3 do que quando é definido como 0,5.</span><span class="sxs-lookup"><span data-stu-id="74916-192">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="74916-193">O contraste é invertido quando o atributo de propriedade de **obter** é definido como um valor negativo como-0,4.</span><span class="sxs-lookup"><span data-stu-id="74916-193">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="74916-194">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="74916-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="74916-195">lo</span><span class="sxs-lookup"><span data-stu-id="74916-195">brightness</span></span>

<span data-ttu-id="74916-196">Você pode usar o atributo de propriedade **blacklevel** do `<image>` elemento para exibir várias imagens que têm configurações de brilho diferentes.</span><span class="sxs-lookup"><span data-stu-id="74916-196">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="74916-197">O valor do atributo da propriedade **blacklevel** pode ser qualquer valor entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="74916-197">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="74916-198">Por padrão, o valor é 0, indicando que o nível de brilho na imagem original é preservado.</span><span class="sxs-lookup"><span data-stu-id="74916-198">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="74916-199">O valor 1 indica o nível mais alto de brilho.</span><span class="sxs-lookup"><span data-stu-id="74916-199">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="74916-200">Por exemplo, para exibir cinco imagens que têm configurações de brilho diferentes, você pode usar o `<image>` elemento e definir um valor diferente para o atributo de propriedade **blacklevel** , conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="74916-200">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image3 (2579 bytes)](images/image3-2.jpg)![\-3.jpg image3 (2330 bytes)](images/image3-3.jpg)![\-4.jpg image3 (2727 bytes)](images/image3-4.jpg)![\-5.jpg image3 (2435 bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="74916-206">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="74916-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="74916-207">escala de cinza</span><span class="sxs-lookup"><span data-stu-id="74916-207">grayscale</span></span>

<span data-ttu-id="74916-208">Você pode usar o atributo de propriedade de **escala de cinza** do `<image>` elemento para exibir imagens com ou sem tons de cinza.</span><span class="sxs-lookup"><span data-stu-id="74916-208">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="74916-209">O valor do atributo da propriedade de **escala de cinza** pode ser true ou false.</span><span class="sxs-lookup"><span data-stu-id="74916-209">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="74916-210">Por padrão, o valor é definido como false para que a imagem seja exibida em cores.</span><span class="sxs-lookup"><span data-stu-id="74916-210">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="74916-211">Se o valor for definido como true, a imagem será exibida em escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="74916-211">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="74916-212">Por exemplo, conforme mostrado na imagem a seguir, a primeira imagem usa a configuração padrão (false) do atributo de escala de cinza ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span><span class="sxs-lookup"><span data-stu-id="74916-212">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="74916-213">Portanto, a imagem é exibida em cores.</span><span class="sxs-lookup"><span data-stu-id="74916-213">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="74916-214">A segunda imagem define o atributo de escala de cinza como true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span><span class="sxs-lookup"><span data-stu-id="74916-214">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="74916-215">Portanto, a imagem é exibida em escala de cinza, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="74916-215">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image4 (2138 bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="74916-218">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="74916-218">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="74916-219">gamma</span><span class="sxs-lookup"><span data-stu-id="74916-219">gamma</span></span>

<span data-ttu-id="74916-220">Você pode usar o atributo de propriedade **gama** do `<image>` elemento para exibir imagens que têm diferentes configurações de gama.</span><span class="sxs-lookup"><span data-stu-id="74916-220">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="74916-221">O valor do atributo de propriedade gama pode ser qualquer valor entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="74916-221">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="74916-222">Por padrão, o valor é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="74916-222">By default, the value is set to 1.</span></span>

<span data-ttu-id="74916-223">Por exemplo, para exibir três imagens que têm diferentes configurações de gama, você pode usar o `<image>` elemento e definir um valor diferente do atributo de propriedade **gama** , conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="74916-223">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![\-1.jpg image5 (2714 bytes)](images/image5-1.jpg)![\-2.jpg image5 (2729 bytes)](images/image5-2.jpg)![\-3.jpg image5 (2726 bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="74916-227">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span><span class="sxs-lookup"><span data-stu-id="74916-227">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 