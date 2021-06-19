---
title: Usando o elemento Image
description: Este artigo descreve o uso do elemento Image no VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Workshop da Web, elemento image
- projetando páginas da Web, elemento image
- linguagem VML (VML), elemento image
- VML (linguagem VML), elemento image
- gráficos vetoriais, elemento image
- elemento de imagem
- Elementos VML, imagem
- Formas VML, elemento image
- linguagem VML (VML), atributos de propriedade de corte
- VML (linguagem VML), atributos de propriedade de corte
- gráficos vetoriais, atributos de propriedade de corte
- Formas VML, atributos de propriedade de corte
- atributos de propriedade crop
- linguagem VML (VML), obter atributo de propriedade
- VML (linguagem VML), atributo de propriedade gain
- gráficos vetoriais, atributo de propriedade gain
- Formas VML, atributo de propriedade gain
- atributo de propriedade gain
- linguagem VML (VML), contraste
- VML (linguagem VML),contraste
- gráficos vetoriais, contraste
- Formas VML, contraste
- linguagem VML (VML), atributo de propriedade blacklevel
- VML (linguagem VML), atributo de propriedade blacklevel
- gráficos vetoriais, atributo de propriedade blacklevel
- Formas VML, atributo de propriedade blacklevel
- Atributo de propriedade blacklevel
- linguagem VML (VML), brilho
- VML (linguagem VML), brilho
- gráficos vetoriais, brilho
- Formas VML, brilho
- linguagem VML (VML), atributo de propriedade grayscale
- VML (linguagem VML), atributo de propriedade grayscale
- gráficos vetoriais, atributo de propriedade grayscale
- Formas VML, atributo de propriedade de escala de cinza
- atributo de propriedade grayscale
- linguagem VML (VML), atributo de propriedade gama
- VML (linguagem VML), atributo de propriedade gama
- gráficos vetoriais, atributo de propriedade gama
- Formas VML, atributo de propriedade gama
- Atributo de propriedade gama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407799"
---
# <a name="using-the-image-element"></a><span data-ttu-id="8b180-144">Usando o elemento Image</span><span class="sxs-lookup"><span data-stu-id="8b180-144">Using the Image Element</span></span>

<span data-ttu-id="8b180-145">Este tópico descreve o VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8b180-145">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8b180-146">As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="8b180-146">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8b180-147">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="8b180-147">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8b180-148">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="8b180-148">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8b180-149">Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="8b180-149">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8b180-150">Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="8b180-150">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8b180-151">Usando `<image>`</span><span class="sxs-lookup"><span data-stu-id="8b180-151">Using `<image>`</span></span>

<span data-ttu-id="8b180-152">Neste tópico, ilustramos como usar o elemento `<image>` para exibir imagens com vários efeitos especiais.</span><span class="sxs-lookup"><span data-stu-id="8b180-152">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="8b180-153">Se você quisesse exibir uma imagem carregada de uma fonte externa, normalmente usaria o elemento fornecido em HTML e, em seguida, apontaria o atributo de propriedade src para o local do arquivo `<img>` de imagem. </span><span class="sxs-lookup"><span data-stu-id="8b180-153">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="8b180-154">Como alternativa, você pode usar o `<image>` elemento fornecido no VML.</span><span class="sxs-lookup"><span data-stu-id="8b180-154">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="8b180-155">Ao usar o elemento , você pode criar apenas um arquivo de imagem e, em seguida, exibir a imagem de forma diferente alterando os atributos de `<image>` propriedade do `<image>` elemento.</span><span class="sxs-lookup"><span data-stu-id="8b180-155">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="8b180-156">Além disso, o elemento fornece vários efeitos especiais que você não pode fazer simplesmente usando o elemento de HTML, como corte `<image>` `<img>` , contraste, brilho, [gama](#gamma) [](#crop) [](#contrast) [](#brightness)e escala de [cinza.](#grayscale)</span><span class="sxs-lookup"><span data-stu-id="8b180-156">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="8b180-157">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="8b180-157">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="8b180-158">cortar</span><span class="sxs-lookup"><span data-stu-id="8b180-158">crop</span></span>

<span data-ttu-id="8b180-159">Você pode usar os atributos de propriedade **cropbottom**, **croptop**, **cropleft** e **cropright** do elemento para exibir imagens diferentes que são cortadas do mesmo arquivo `<image>` de imagem.</span><span class="sxs-lookup"><span data-stu-id="8b180-159">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="8b180-160">O valor desses atributos de corte representa o corte percentual da borda da imagem.</span><span class="sxs-lookup"><span data-stu-id="8b180-160">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="8b180-161">O valor pode ser qualquer número entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="8b180-161">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="8b180-162">Por padrão, o valor é definido como 0, indicando nenhuma recortação da borda.</span><span class="sxs-lookup"><span data-stu-id="8b180-162">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="8b180-163">O valor 0,1 indica um corte de 10% da borda, o valor 0,15 indica um corte de 15% da borda e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8b180-163">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="8b180-164">Por exemplo, para exibir cinco imagens que são todas cortadas do mesmo arquivo de imagem, você pode usar o elemento e especificar valores de corte diferentes, conforme mostrado na seguinte representação `<image>` de VML:</span><span class="sxs-lookup"><span data-stu-id="8b180-164">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![image1 \-2.jpg (1969 bytes)](images/image1-2.jpg)![image1 \-3.jpg (1148 bytes)](images/image1-3.jpg)![image1 \-4.jpg (1686 bytes)](images/image1-4.jpg)![image1 \-5.jpg (1364 bytes)](images/image1-5.jpg)


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





<span data-ttu-id="8b180-170">A primeira imagem, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , não tem nenhum valor de corte.</span><span class="sxs-lookup"><span data-stu-id="8b180-170">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="8b180-171">Portanto, 100% da imagem original é exibida em um tamanho de 100 pontos por 80 pontos.</span><span class="sxs-lookup"><span data-stu-id="8b180-171">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="8b180-172">A segunda imagem, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , tem alguns valores de corte.</span><span class="sxs-lookup"><span data-stu-id="8b180-172">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="8b180-173">`cropbottom="0.2"` indica que 20% da imagem será cortada da parte inferior; `cropright="0.15"` indica que 15% da imagem será cortada da borda direita.</span><span class="sxs-lookup"><span data-stu-id="8b180-173">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="8b180-174">A imagem restante é exibida em um tamanho de 85 pontos por 64 pontos.</span><span class="sxs-lookup"><span data-stu-id="8b180-174">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="8b180-175">Da mesma forma, a terceira, a quarta e a quinta imagens têm alguns valores de corte.</span><span class="sxs-lookup"><span data-stu-id="8b180-175">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="8b180-176">A imagem original é cortada de acordo com os valores de corte e, em seguida, é exibida de acordo com o valor de largura e altura.</span><span class="sxs-lookup"><span data-stu-id="8b180-176">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="8b180-177">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="8b180-177">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="8b180-178">contraste</span><span class="sxs-lookup"><span data-stu-id="8b180-178">contrast</span></span>

<span data-ttu-id="8b180-179">Você pode usar o **atributo de** propriedade gain do elemento para exibir várias imagens que `<image>` têm configurações de contraste diferentes.</span><span class="sxs-lookup"><span data-stu-id="8b180-179">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="8b180-180">O valor do **atributo de** propriedade gain pode ser qualquer número.</span><span class="sxs-lookup"><span data-stu-id="8b180-180">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="8b180-181">Por padrão, o valor é 1, indicando o uso do mesmo contraste que a imagem original.</span><span class="sxs-lookup"><span data-stu-id="8b180-181">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="8b180-182">O valor 0 não indica nenhum contraste.</span><span class="sxs-lookup"><span data-stu-id="8b180-182">The value 0 indicates no contrast.</span></span> <span data-ttu-id="8b180-183">Quanto maior o número, maior o contraste.</span><span class="sxs-lookup"><span data-stu-id="8b180-183">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="8b180-184">Por exemplo, para exibir cinco imagens que têm configurações de contraste diferentes, você pode usar o elemento e definir um valor diferente para o atributo de propriedade gain, conforme mostrado na seguinte representação `<image>` de VML: </span><span class="sxs-lookup"><span data-stu-id="8b180-184">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![image2 \-2.jpg (270 bytes)](images/image2-2.jpg)![image2 \-3.jpg (1919 bytes)](images/image2-3.jpg)![image2 \-4.jpg (3143 bytes)](images/image2-4.jpg)![image2 \-5.jpg (1724 bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="8b180-190">Quando o **atributo de** propriedade gain é definido como 0, a imagem inteira fica cinza porque não há contraste.</span><span class="sxs-lookup"><span data-stu-id="8b180-190">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="8b180-191">O contraste é mais perceptível quando o **atributo de** propriedade gain é definido como 3 do que quando ele é definido como 0,5.</span><span class="sxs-lookup"><span data-stu-id="8b180-191">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="8b180-192">O contraste é invertido quando o **atributo de** propriedade gain é definido como um valor negativo, como -0,4.</span><span class="sxs-lookup"><span data-stu-id="8b180-192">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="8b180-193">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="8b180-193">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="8b180-194">Brilho</span><span class="sxs-lookup"><span data-stu-id="8b180-194">brightness</span></span>

<span data-ttu-id="8b180-195">Você pode usar o **atributo de propriedade de nível** preto do elemento para exibir várias imagens que têm `<image>` configurações de brilho diferentes.</span><span class="sxs-lookup"><span data-stu-id="8b180-195">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="8b180-196">O valor do atributo **de propriedade blacklevel** pode ser qualquer valor entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="8b180-196">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="8b180-197">Por padrão, o valor é 0, indicando que o nível de brilho na imagem original é preservado.</span><span class="sxs-lookup"><span data-stu-id="8b180-197">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="8b180-198">O valor 1 indica o nível mais alto de brilho.</span><span class="sxs-lookup"><span data-stu-id="8b180-198">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="8b180-199">Por exemplo, para exibir cinco imagens que têm configurações de brilho diferentes, você pode usar o elemento e definir um valor diferente para o atributo de propriedade de nível preto, conforme mostrado na seguinte representação `<image>` de VML: </span><span class="sxs-lookup"><span data-stu-id="8b180-199">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![image3 \-2.jpg (2579 bytes)](images/image3-2.jpg)![image3 \-3.jpg (2330 bytes)](images/image3-3.jpg)![image3 \-4.jpg (2727 bytes)](images/image3-4.jpg)![image3 \-5.jpg (2435 bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="8b180-205">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="8b180-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="8b180-206">escala de cinza</span><span class="sxs-lookup"><span data-stu-id="8b180-206">grayscale</span></span>

<span data-ttu-id="8b180-207">Você pode usar o **atributo de propriedade grayscale** do `<image>` elemento para exibir imagens com ou sem escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="8b180-207">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="8b180-208">O valor do atributo **de propriedade de escala** de cinza pode ser true ou false.</span><span class="sxs-lookup"><span data-stu-id="8b180-208">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="8b180-209">Por padrão, o valor é definido como false para que a imagem seja exibida em cores.</span><span class="sxs-lookup"><span data-stu-id="8b180-209">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="8b180-210">Se o valor for definido como true, a imagem será exibida em escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="8b180-210">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="8b180-211">Por exemplo, conforme mostrado na imagem a seguir, a primeira imagem usa a configuração padrão (false)do atributo de escala de cinza ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span><span class="sxs-lookup"><span data-stu-id="8b180-211">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="8b180-212">Portanto, a imagem é exibida em cores.</span><span class="sxs-lookup"><span data-stu-id="8b180-212">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="8b180-213">A segunda imagem define o atributo de escala de cinza como true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span><span class="sxs-lookup"><span data-stu-id="8b180-213">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="8b180-214">Portanto, a imagem é exibida em escala de cinza, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="8b180-214">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 bytes)](images/image1.jpg)![image4 \-2.jpg (2138 bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="8b180-217">[![voltar ao início ](images/top.gif) Voltar ao início](#top)</span><span class="sxs-lookup"><span data-stu-id="8b180-217">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="8b180-218">gamma</span><span class="sxs-lookup"><span data-stu-id="8b180-218">gamma</span></span>

<span data-ttu-id="8b180-219">Você pode usar o atributo de propriedade **gama** do elemento `<image>` para exibir imagens que têm configurações gama diferentes.</span><span class="sxs-lookup"><span data-stu-id="8b180-219">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="8b180-220">O valor do atributo de propriedade gama pode ser qualquer valor entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="8b180-220">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="8b180-221">Por padrão, o valor é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="8b180-221">By default, the value is set to 1.</span></span>

<span data-ttu-id="8b180-222">Por exemplo, para exibir três imagens que têm configurações gama diferentes, você pode usar o elemento e definir um valor diferente do atributo de propriedade gama, conforme mostrado na seguinte representação `<image>` de VML: </span><span class="sxs-lookup"><span data-stu-id="8b180-222">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![image5 \-1.jpg (2714 bytes)](images/image5-1.jpg)![image5 \-2.jpg (2729 bytes)](images/image5-2.jpg)![image5 \-3.jpg (2726 bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="8b180-226">Para obter mais informações sobre esse elemento, consulte a [especificação de VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span><span class="sxs-lookup"><span data-stu-id="8b180-226">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 