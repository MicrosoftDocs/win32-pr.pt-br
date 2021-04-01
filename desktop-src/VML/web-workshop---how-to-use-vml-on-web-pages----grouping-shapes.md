---
title: Agrupando formas
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Web Workshop, agrupando formas
- Criando páginas da Web, agrupando formas
- Linguagem VML (VML), agrupamento de formas
- VML (linguagem VML), agrupamento de formas
- gráficos vetoriais, agrupamento de formas
- Formas de VML, agrupamento
- agrupando formas
- Linguagem VML (VML), elemento de grupo
- VML (linguagem VML), elemento de grupo
- gráficos vetoriais, elemento Group
- elemento de grupo
- Elementos de VML, grupo
- Linguagem VML (VML), espaço de coordenadas local
- VML (linguagem VML), espaço de coordenadas local
- gráficos vetoriais, espaço de coordenadas local
- espaço de coordenadas local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eed282094e2d24d2d27e338b93731eaaa1eec0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008066"
---
# <a name="grouping-shapes"></a><span data-ttu-id="32271-120">Agrupando formas</span><span class="sxs-lookup"><span data-stu-id="32271-120">Grouping Shapes</span></span>

<span data-ttu-id="32271-121">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="32271-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="32271-122">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="32271-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="32271-123">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="32271-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="32271-124">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="32271-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="32271-125">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="32271-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="32271-126">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="32271-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="32271-127">Como você aprendeu, você pode facilmente desenhar formas individuais usando VML.</span><span class="sxs-lookup"><span data-stu-id="32271-127">As you've learned, you can easily draw individual shapes by using VML.</span></span> <span data-ttu-id="32271-128">Nesta seção, explicaremos os benefícios do agrupamento de formas e como agrupar formas.</span><span class="sxs-lookup"><span data-stu-id="32271-128">In this section, we will explain the benefits of grouping shapes together, and how to group shapes.</span></span>

<span data-ttu-id="32271-129">Se você tivesse muitas formas que precisavam ser dimensionadas, movidas ou giradas juntas, você acharia entediante definir os atributos individualmente para cada forma.</span><span class="sxs-lookup"><span data-stu-id="32271-129">If you had many shapes that needed to be scaled, moved, or rotated together, you would find it tedious to set the attributes individually for each shape.</span></span> <span data-ttu-id="32271-130">Além disso, você aumentaria a margem de erros.</span><span class="sxs-lookup"><span data-stu-id="32271-130">Plus you would raise your margin for errors.</span></span> <span data-ttu-id="32271-131">Seria melhor se você pudesse agrupar as formas e, em seguida, definir os atributos de todo o grupo.</span><span class="sxs-lookup"><span data-stu-id="32271-131">It would be better if you could group the shapes, and then set the attributes for the entire group.</span></span>

<span data-ttu-id="32271-132">Na VML, você pode usar o `<group>` elemento para agrupar muitas formas para que elas possam ser transformadas como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="32271-132">In VML, you can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span> <span data-ttu-id="32271-133">Por exemplo, conforme mostrado na representação de VML a seguir, você pode facilmente agrupar duas formas.</span><span class="sxs-lookup"><span data-stu-id="32271-133">For example, as shown in the following VML representation, you can easily group two shapes together.</span></span>


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



<span data-ttu-id="32271-134">Quando as formas são agrupadas, elas usam o [espaço de coordenadas local](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) do grupo.</span><span class="sxs-lookup"><span data-stu-id="32271-134">When shapes are grouped, they use the [local coordinate space](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) of the group.</span></span> <span data-ttu-id="32271-135">Portanto, as formas dentro de um grupo podem ser dimensionadas e movidas juntas.</span><span class="sxs-lookup"><span data-stu-id="32271-135">Therefore, shapes within a group can be scaled and moved together.</span></span> <span data-ttu-id="32271-136">Você verá mais exemplos no tópico usar espaço de coordenadas local.</span><span class="sxs-lookup"><span data-stu-id="32271-136">You will see more examples in the Use Local Coordinate Space topic.</span></span>

<span data-ttu-id="32271-137">Dentro de um grupo, você pode ter quantas formas ou grupos desejar.</span><span class="sxs-lookup"><span data-stu-id="32271-137">Inside a group, you can have as many shapes or groups as you want.</span></span> <span data-ttu-id="32271-138">Quando um grupo está dentro de outro grupo, ele é chamado de "grupo aninhado".</span><span class="sxs-lookup"><span data-stu-id="32271-138">When a group is inside another group, it is called a "nested group".</span></span> <span data-ttu-id="32271-139">Não há nenhuma limitação nos níveis de aninhamento.</span><span class="sxs-lookup"><span data-stu-id="32271-139">There is no limitation on the levels of nesting.</span></span>

<span data-ttu-id="32271-140">Por exemplo, as linhas a seguir demonstram um grupo aninhado de 3 níveis.</span><span class="sxs-lookup"><span data-stu-id="32271-140">For example, the following lines demonstrate a 3-level nested group.</span></span> <span data-ttu-id="32271-141">Shape3 e Shape4 estão em GroupC.</span><span class="sxs-lookup"><span data-stu-id="32271-141">Shape3 and Shape4 are in GroupC.</span></span> <span data-ttu-id="32271-142">Shape2 e GroupC estão em GroupB.</span><span class="sxs-lookup"><span data-stu-id="32271-142">Shape2 and GroupC are in GroupB.</span></span> <span data-ttu-id="32271-143">Shape1 e GroupB estão no GroupA.</span><span class="sxs-lookup"><span data-stu-id="32271-143">Shape1 and GroupB are in GroupA.</span></span>


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



<span data-ttu-id="32271-144">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span><span class="sxs-lookup"><span data-stu-id="32271-144">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span></span>

<span data-ttu-id="32271-145">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="32271-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="32271-146">Resumo</span><span class="sxs-lookup"><span data-stu-id="32271-146">Summary</span></span>

<span data-ttu-id="32271-147">Você pode usar o `<group>` elemento para agrupar muitas formas para que elas possam ser transformadas como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="32271-147">You can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span>

 

 