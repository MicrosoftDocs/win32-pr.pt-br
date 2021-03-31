---
title: Usando o elemento Path
description: Usando o elemento Path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Web Workshop, elemento Path
- Criando páginas da Web, elemento Path
- Linguagem VML (VML), elemento de caminho
- VML (linguagem VML), elemento Path
- gráficos vetoriais, elemento Path
- elemento Path
- Elementos de VML, caminho
- Formas de VML, elemento Path
- Linguagem VML (VML), personalizando contornos de forma
- VML (linguagem VML), personalizando contornos de forma
- gráficos vetoriais, personalizando contornos de forma
- Formas de VML, personalizando contornos
- Personalizando contornos de forma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641712"
---
# <a name="using-the-path-element"></a><span data-ttu-id="aa18e-116">Usando o elemento Path</span><span class="sxs-lookup"><span data-stu-id="aa18e-116">Using the Path Element</span></span>

<span data-ttu-id="aa18e-117">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="aa18e-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="aa18e-118">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="aa18e-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="aa18e-119">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="aa18e-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="aa18e-120">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="aa18e-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="aa18e-121">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="aa18e-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="aa18e-122">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="aa18e-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="aa18e-123">Você aprendeu que pode usar os elementos de forma predefinidos da VML, como `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` e `<arc>` --para desenhar uma forma.</span><span class="sxs-lookup"><span data-stu-id="aa18e-123">You've learned that you can use the VML predefined shape elements -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` -- to draw a shape.</span></span> <span data-ttu-id="aa18e-124">Neste tópico, Ilustraremos como usar o `<path>` subelemento para personalizar a estrutura de tópicos de uma forma.</span><span class="sxs-lookup"><span data-stu-id="aa18e-124">In this topic, we will illustrate how to use the `<path>` sub-element to customize the outline of a shape.</span></span>

<span data-ttu-id="aa18e-125">Você pode posicionar o `<path>` subelemento dentro do `<shape>` `<shapetype>` elemento ou.</span><span class="sxs-lookup"><span data-stu-id="aa18e-125">You can place the `<path>` sub-element inside the `<shape>` or `<shapetype>` element.</span></span> <span data-ttu-id="aa18e-126">Você pode usar os atributos de Propriedade do `<path>` subelemento para personalizar a estrutura de tópicos da forma.</span><span class="sxs-lookup"><span data-stu-id="aa18e-126">You can then use the property attributes of the `<path>` sub-element to customize the outline of the shape.</span></span>

<span data-ttu-id="aa18e-127">Por exemplo, para desenhar a forma personalizada ilustrada na imagem a seguir, você pode usar o `<path>` subelemento para definir o contorno da forma, conforme mostrado na seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="aa18e-127">For example, to draw the customized shape illustrated in the following picture, you can use the `<path>` sub-element to define the outline of the shape, as shown in the following VML representation:</span></span>

![shape1.gif (1301 bytes)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   <span data-ttu-id="aa18e-129">Os valores `m 8,65` indicam que o desenho começa no ponto (8, 65).</span><span class="sxs-lookup"><span data-stu-id="aa18e-129">The values `m 8,65` indicate that the drawing starts at the point (8,65).</span></span>
-   <span data-ttu-id="aa18e-130">Os valores `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indicam que uma linha reta começa no ponto atual (8, 65) e termina no ponto determinado (72, 65), que se torna o novo ponto atual.</span><span class="sxs-lookup"><span data-stu-id="aa18e-130">The values `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indicate that a straight line begins at the current point (8, 65) and ends at the given point (72, 65), which becomes the new current point.</span></span> <span data-ttu-id="aa18e-131">Uma nova linha começa no ponto atual (72, 65) e termina no ponto determinado, que se torna o novo ponto atual e assim por diante, até o ponto final (60, 100).</span><span class="sxs-lookup"><span data-stu-id="aa18e-131">A new line begins at the current point (72, 65) and ends at the given point, which becomes the new current point, and so on, to the final point (60, 100).</span></span>
-   <span data-ttu-id="aa18e-132">`x` indica que o caminho será fechado por uma linha reta que começa no ponto atual (60, 100) e termina no ponto original (8, 65).</span><span class="sxs-lookup"><span data-stu-id="aa18e-132">`x` indicates that the path will close by a straight line that starts at the current point (60, 100) and ends at the original point (8, 65).</span></span>
-   <span data-ttu-id="aa18e-133">`e` indica parar o desenho.</span><span class="sxs-lookup"><span data-stu-id="aa18e-133">`e` indicates stop drawing.</span></span>

<span data-ttu-id="aa18e-134">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span><span class="sxs-lookup"><span data-stu-id="aa18e-134">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span></span>

 

 