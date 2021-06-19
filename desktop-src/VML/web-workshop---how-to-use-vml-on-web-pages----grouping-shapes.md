---
title: Agrupando formas
description: Este artigo descreve as formas de agrupamento no VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
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
ms.openlocfilehash: 61e0c3073f55d23c15734b5d5ddfa886e7291530
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407699"
---
# <a name="grouping-shapes"></a><span data-ttu-id="739bf-119">Agrupando formas</span><span class="sxs-lookup"><span data-stu-id="739bf-119">Grouping Shapes</span></span>

<span data-ttu-id="739bf-120">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="739bf-120">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="739bf-121">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="739bf-121">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="739bf-122">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="739bf-122">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="739bf-123">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="739bf-123">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="739bf-124">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="739bf-124">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="739bf-125">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="739bf-125">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="739bf-126">Como você aprendeu, você pode facilmente desenhar formas individuais usando VML.</span><span class="sxs-lookup"><span data-stu-id="739bf-126">As you've learned, you can easily draw individual shapes by using VML.</span></span> <span data-ttu-id="739bf-127">Nesta seção, explicaremos os benefícios do agrupamento de formas e como agrupar formas.</span><span class="sxs-lookup"><span data-stu-id="739bf-127">In this section, we will explain the benefits of grouping shapes together, and how to group shapes.</span></span>

<span data-ttu-id="739bf-128">Se você tivesse muitas formas que precisavam ser dimensionadas, movidas ou giradas juntas, você acharia entediante definir os atributos individualmente para cada forma.</span><span class="sxs-lookup"><span data-stu-id="739bf-128">If you had many shapes that needed to be scaled, moved, or rotated together, you would find it tedious to set the attributes individually for each shape.</span></span> <span data-ttu-id="739bf-129">Além disso, você aumentaria a margem de erros.</span><span class="sxs-lookup"><span data-stu-id="739bf-129">Plus you would raise your margin for errors.</span></span> <span data-ttu-id="739bf-130">Seria melhor se você pudesse agrupar as formas e, em seguida, definir os atributos de todo o grupo.</span><span class="sxs-lookup"><span data-stu-id="739bf-130">It would be better if you could group the shapes, and then set the attributes for the entire group.</span></span>

<span data-ttu-id="739bf-131">Na VML, você pode usar o `<group>` elemento para agrupar muitas formas para que elas possam ser transformadas como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="739bf-131">In VML, you can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span> <span data-ttu-id="739bf-132">Por exemplo, conforme mostrado na representação de VML a seguir, você pode facilmente agrupar duas formas.</span><span class="sxs-lookup"><span data-stu-id="739bf-132">For example, as shown in the following VML representation, you can easily group two shapes together.</span></span>


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



<span data-ttu-id="739bf-133">Quando as formas são agrupadas, elas usam o [espaço de coordenadas local](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) do grupo.</span><span class="sxs-lookup"><span data-stu-id="739bf-133">When shapes are grouped, they use the [local coordinate space](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) of the group.</span></span> <span data-ttu-id="739bf-134">Portanto, as formas dentro de um grupo podem ser dimensionadas e movidas juntas.</span><span class="sxs-lookup"><span data-stu-id="739bf-134">Therefore, shapes within a group can be scaled and moved together.</span></span> <span data-ttu-id="739bf-135">Você verá mais exemplos no tópico usar espaço de coordenadas local.</span><span class="sxs-lookup"><span data-stu-id="739bf-135">You will see more examples in the Use Local Coordinate Space topic.</span></span>

<span data-ttu-id="739bf-136">Dentro de um grupo, você pode ter quantas formas ou grupos desejar.</span><span class="sxs-lookup"><span data-stu-id="739bf-136">Inside a group, you can have as many shapes or groups as you want.</span></span> <span data-ttu-id="739bf-137">Quando um grupo está dentro de outro grupo, ele é chamado de "grupo aninhado".</span><span class="sxs-lookup"><span data-stu-id="739bf-137">When a group is inside another group, it is called a "nested group".</span></span> <span data-ttu-id="739bf-138">Não há nenhuma limitação nos níveis de aninhamento.</span><span class="sxs-lookup"><span data-stu-id="739bf-138">There is no limitation on the levels of nesting.</span></span>

<span data-ttu-id="739bf-139">Por exemplo, as linhas a seguir demonstram um grupo aninhado de 3 níveis.</span><span class="sxs-lookup"><span data-stu-id="739bf-139">For example, the following lines demonstrate a 3-level nested group.</span></span> <span data-ttu-id="739bf-140">Shape3 e Shape4 estão em GroupC.</span><span class="sxs-lookup"><span data-stu-id="739bf-140">Shape3 and Shape4 are in GroupC.</span></span> <span data-ttu-id="739bf-141">Shape2 e GroupC estão em GroupB.</span><span class="sxs-lookup"><span data-stu-id="739bf-141">Shape2 and GroupC are in GroupB.</span></span> <span data-ttu-id="739bf-142">Shape1 e GroupB estão no GroupA.</span><span class="sxs-lookup"><span data-stu-id="739bf-142">Shape1 and GroupB are in GroupA.</span></span>


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



<span data-ttu-id="739bf-143">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span><span class="sxs-lookup"><span data-stu-id="739bf-143">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span></span>

<span data-ttu-id="739bf-144">[![voltar ao início ](images/top.gif) para cima](#top)</span><span class="sxs-lookup"><span data-stu-id="739bf-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="739bf-145">Resumo</span><span class="sxs-lookup"><span data-stu-id="739bf-145">Summary</span></span>

<span data-ttu-id="739bf-146">Você pode usar o `<group>` elemento para agrupar muitas formas para que elas possam ser transformadas como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="739bf-146">You can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span>

 

 