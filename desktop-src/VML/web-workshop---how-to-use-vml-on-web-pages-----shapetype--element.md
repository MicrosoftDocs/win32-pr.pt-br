---
title: Usando o elemento ShapeType
description: Usando o elemento ShapeType
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Web Workshop, elemento ShapeType
- Criando páginas da Web, elemento ShapeType
- Linguagem VML (VML), elemento ShapeType
- VML (linguagem VML), elemento ShapeType
- gráficos vetoriais, elemento ShapeType
- elemento ShapeType
- Elementos de VML, formatype
- Formas de VML, elemento ShapeType
- Linguagem VML (VML), definindo formas usadas com frequência
- VML (linguagem VML), definindo formas usadas com frequência
- gráficos vetoriais, definição de formas usadas com frequência
- definindo formas usadas com frequência
- Formas de VML, definindo frequentemente usadas
- Linguagem VML (VML), instanciando cópias de formas
- VML (linguagem VML), instanciando cópias de formas
- gráficos vetoriais, instanciando cópias de formas
- Criando uma instância de cópias de formas
- Formas de VML, instanciando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa7ec47dde492231e8bcd54f68e4637454613b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454289"
---
# <a name="using-the-shapetype-element"></a><span data-ttu-id="ac16c-121">Usando o elemento ShapeType</span><span class="sxs-lookup"><span data-stu-id="ac16c-121">Using the Shapetype Element</span></span>

<span data-ttu-id="ac16c-122">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ac16c-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ac16c-123">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="ac16c-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ac16c-124">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="ac16c-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ac16c-125">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="ac16c-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ac16c-126">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ac16c-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ac16c-127">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ac16c-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ac16c-128">Neste tópico, Ilustraremos como usar o `<shapetype>` elemento para definir suas próprias formas usadas com frequência e, em seguida, instanciar ou criar formas a partir de ShapeType.</span><span class="sxs-lookup"><span data-stu-id="ac16c-128">In this topic, we will illustrate how to use the `<shapetype>` element to define your own frequently-used shapes and then instantiate, or create, shapes from the shapetype.</span></span>

<span data-ttu-id="ac16c-129">Se você quisesse desenhar muitas formas que tenham Propriedades iguais ou semelhantes, seria entediante se você tivesse que digitar repetidamente os mesmos atributos de propriedade para cada forma.</span><span class="sxs-lookup"><span data-stu-id="ac16c-129">If you wanted to draw many shapes that have the same or similar properties, it would be tedious if you had to repeatedly type the same property attributes for each shape.</span></span> <span data-ttu-id="ac16c-130">A VML fornece o `<shapetype>` elemento para que você possa definir um protótipo de uma forma.</span><span class="sxs-lookup"><span data-stu-id="ac16c-130">VML provides the `<shapetype>` element so that you can define a prototype of a shape.</span></span> <span data-ttu-id="ac16c-131">Em seguida, você pode usar o `<shape>` elemento para instanciar muitas cópias de formas do mesmo ShapeType.</span><span class="sxs-lookup"><span data-stu-id="ac16c-131">You can then use the `<shape>` element to instantiate many copies of shapes from the same shapetype.</span></span>

<span data-ttu-id="ac16c-132">Você pode seguir as três etapas para definir um ShapeType e, em seguida, instanciar uma forma a partir de ShapeType:</span><span class="sxs-lookup"><span data-stu-id="ac16c-132">You can follow the three steps to define a shapetype, and then instantiate a shape from the shapetype:</span></span>

1.  <span data-ttu-id="ac16c-133">Digite um `<shapetype>` elemento e dê a ele um nome especificando o atributo de ID.</span><span class="sxs-lookup"><span data-stu-id="ac16c-133">Type a `<shapetype>` element and give it a name by specifying the id attribute.</span></span>
2.  <span data-ttu-id="ac16c-134">Descreva o tipo de forma usando seus atributos de propriedade ou subelementos.</span><span class="sxs-lookup"><span data-stu-id="ac16c-134">Describe the shapetype by using its property attributes or sub-elements.</span></span>
3.  <span data-ttu-id="ac16c-135">Crie uma instância de uma forma digitando um `<shape>` elemento e consulte o atributo Type da forma para o atributo ID de ShapeType.</span><span class="sxs-lookup"><span data-stu-id="ac16c-135">Instantiate a shape by typing a `<shape>` element, and refer the type attribute of the shape to the id attribute of the shapetype.</span></span>

<span data-ttu-id="ac16c-136">Por exemplo, você digita as linhas a seguir para criar um tipo de forma chamado "myShape":</span><span class="sxs-lookup"><span data-stu-id="ac16c-136">For example, you type the following lines to create a shapetype called "MyShape":</span></span>


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



<span data-ttu-id="ac16c-137">Em seguida, você altera o tipo de forma definindo alguns atributos de propriedade, como `fillcolor="red" strokecolor="blue"` .</span><span class="sxs-lookup"><span data-stu-id="ac16c-137">Then, you alter the shapetype by setting some property attributes, such as `fillcolor="red" strokecolor="blue"`.</span></span> <span data-ttu-id="ac16c-138">Ou, você pode usar subelementos dentro de ShapeType, como `<path>` , `<fill>` (Falaremos `<stroke>` sobre esses subelementos nos tópicos posteriores).</span><span class="sxs-lookup"><span data-stu-id="ac16c-138">Or, you can use sub-elements inside the shapetype, such as `<path>`, `<fill>`, `<stroke>` (we will talk about those sub-elements in later topics).</span></span>


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



<span data-ttu-id="ac16c-139">Em seguida, você cria uma instância de uma forma de forma "myforma" especificando `type="#MyShape"` , conforme mostrado na representação de VML a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac16c-139">Then, you instantiate a shape from the shapetype "MyShape" by specifying `type="#MyShape"`, as shown in the following VML representation.</span></span> <span data-ttu-id="ac16c-140">Essa forma herda todas as propriedades da forma "myFormat" e é exibida dentro de sua caixa de conteúdo em um tamanho de 100 por 80.</span><span class="sxs-lookup"><span data-stu-id="ac16c-140">This shape inherits all properties from the shapetype "MyShape", and is displayed within its containing box at a size of 100 by 80.</span></span>


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



<span data-ttu-id="ac16c-141">Você pode criar uma instância de outra forma com base no tipo de forma "myFormat" especificando `type="#MyShape"` e substitui algumas propriedades, como `fillcolor="maroon"` , conforme mostrado na representação de VML a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac16c-141">You can instantiate another shape from the shapetype "MyShape" by specifying `type="#MyShape"` and overwrite some properties, such as `fillcolor="maroon"`, as shown in the following VML representation.</span></span> <span data-ttu-id="ac16c-142">Essa forma herda todas as propriedades da forma "myShape", exceto da propriedade FillColor, e é exibida dentro de sua caixa que contém um tamanho de 70 por 90.</span><span class="sxs-lookup"><span data-stu-id="ac16c-142">This shape inherits all properties from the shapetype "MyShape" except the fillcolor property, and is displayed within its containing box at a size of 70 by 90.</span></span>


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



<span data-ttu-id="ac16c-143">Aqui está a representação de VML completa para o exemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="ac16c-143">Here is the complete VML representation for the preceding example:</span></span>

![\-1.gif type1 (477 bytes)](images/type1-1.gif)![\-2.gif type1 (471 bytes)](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





<span data-ttu-id="ac16c-146">Como você aprendeu, quando uma forma é instanciada de um ShapeType, ela herda todos os atributos de Propriedade do ShapeType.</span><span class="sxs-lookup"><span data-stu-id="ac16c-146">As you've learned, when a shape is instantiated from a shapetype, it inherits all of the property attributes from the shapetype.</span></span> <span data-ttu-id="ac16c-147">Você pode substituir alguns ou todos os atributos herdados redefinindo atributos dentro do `<shape>` elemento.</span><span class="sxs-lookup"><span data-stu-id="ac16c-147">You can overwrite some or all of the inherited attributes by redefining attributes inside the `<shape>` element.</span></span> <span data-ttu-id="ac16c-148">Lembre-se de que a herança é apenas um nível.</span><span class="sxs-lookup"><span data-stu-id="ac16c-148">Be aware that the inheritance is only one level.</span></span> <span data-ttu-id="ac16c-149">Isso ocorre porque apenas um `<shape>` elemento pode referenciar um `<shapetype>` elemento.</span><span class="sxs-lookup"><span data-stu-id="ac16c-149">This is because only a `<shape>` element can reference a `<shapetype>` element.</span></span> <span data-ttu-id="ac16c-150">Um `<shapetype>` elemento não pode fazer referência A outro `<shapetype>` elemento.</span><span class="sxs-lookup"><span data-stu-id="ac16c-150">A `<shapetype>` element cannot reference another `<shapetype>` element.</span></span>

<span data-ttu-id="ac16c-151">Além disso, um ShapeType não pertence a nenhum grupo.</span><span class="sxs-lookup"><span data-stu-id="ac16c-151">Also, a shapetype doesn't belong to any group.</span></span> <span data-ttu-id="ac16c-152">Portanto, o `<shapetype>` elemento pode aparecer sozinha ou dentro de um `<group>` elemento.</span><span class="sxs-lookup"><span data-stu-id="ac16c-152">Therefore, the `<shapetype>` element can appear by itself or inside a `<group>` element.</span></span> <span data-ttu-id="ac16c-153">Você pode ter muitas formas dentro de grupos diferentes que referenciam o mesmo ShapeType.</span><span class="sxs-lookup"><span data-stu-id="ac16c-153">You can have many shapes inside different groups that reference the same shapetype.</span></span> <span data-ttu-id="ac16c-154">Se um ShapeType aparecer dentro de um grupo, uma forma que mora em outro grupo ainda poderá fazer referência a esse ShapeType.</span><span class="sxs-lookup"><span data-stu-id="ac16c-154">If a shapetype appears inside a group, a shape living in another group can still reference this shapetype.</span></span>

<span data-ttu-id="ac16c-155">Por exemplo, na seguinte representação de VML, Rect1 e Rect2 estão em GroupA e Rect3 está em GroupB.</span><span class="sxs-lookup"><span data-stu-id="ac16c-155">For example, in the following VML representation, Rect1 and Rect2 are in GroupA, and Rect3 is in GroupB.</span></span> <span data-ttu-id="ac16c-156">Todos os três retângulos são instanciados a partir de ShapeType de myFormat.</span><span class="sxs-lookup"><span data-stu-id="ac16c-156">All three rectangles are instantiated from MyShape shapetype.</span></span>


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



<span data-ttu-id="ac16c-157">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span><span class="sxs-lookup"><span data-stu-id="ac16c-157">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span></span>

 

 