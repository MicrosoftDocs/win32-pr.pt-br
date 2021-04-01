---
title: Dimensionando formas
description: Dimensionando formas
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Web Workshop, dimensionando formas
- Criando páginas da Web, dimensionando formas
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
ms.openlocfilehash: e2e7c64fdc0eaa32df1f22b06734b366609ee319
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641259"
---
# <a name="scaling-shapes"></a><span data-ttu-id="4e210-115">Dimensionando formas</span><span class="sxs-lookup"><span data-stu-id="4e210-115">Scaling Shapes</span></span>

<span data-ttu-id="4e210-116">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4e210-116">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4e210-117">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="4e210-117">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4e210-118">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="4e210-118">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4e210-119">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="4e210-119">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4e210-120">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4e210-120">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4e210-121">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4e210-121">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4e210-122">Você aprendeu como desenhar e colorir formas em uma página da Web usando a VML.</span><span class="sxs-lookup"><span data-stu-id="4e210-122">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="4e210-123">Neste tópico, Ilustraremos como dimensionar formas para qualquer tamanho desejado.</span><span class="sxs-lookup"><span data-stu-id="4e210-123">In this topic, we will illustrate how to scale shapes to any size you want.</span></span>

<span data-ttu-id="4e210-124">A VML usa a mesma sintaxe definida na seção [detalhes do modelo de renderização visual](https://www.w3.org/TR/PR-CSS2/visudet.mdl) da [especificação CSS2](https://www.w3.org/TR/PR-CSS2/) para especificar o tamanho da caixa que o contém para que o conteúdo de uma forma seja renderizado (desenhado) dentro da caixa que o contém.</span><span class="sxs-lookup"><span data-stu-id="4e210-124">VML uses the same syntax defined in the [Visual Rendering Model Details](https://www.w3.org/TR/PR-CSS2/visudet.mdl) section of the [CSS2 specification](https://www.w3.org/TR/PR-CSS2/) to specify the size of the containing box so that the contents of a shape will be rendered (drawn) within the containing box.</span></span> <span data-ttu-id="4e210-125">Você pode usar os atributos de estilo **Width** e **Height** para definir o tamanho da caixa que o contém.</span><span class="sxs-lookup"><span data-stu-id="4e210-125">You can use the **width** and **height** style attributes to define the size of the containing box.</span></span>

<span data-ttu-id="4e210-126">Por exemplo, se você desenhar uma oval e especificar **Style**= ' largura: 75pt; altura: 100pt ', a elipse será desenhada dentro de uma caixa que contém um tamanho de 75 pontos (largura) por 100 pontos (altura), conforme mostrado na figura a seguir:</span><span class="sxs-lookup"><span data-stu-id="4e210-126">For example, if you draw an oval and specify **style**='width:75pt;height:100pt', the oval will be drawn within a containing box at a size of 75 points (width) by 100 points (height), as shown in the following picture:</span></span>

![oval1.gif (660 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





<span data-ttu-id="4e210-128">Se você alterar o tamanho para **Style**= ' largura: 120pt; altura: 140pt ', a elipse se tornará maior porque é dimensionada na nova caixa de conteúdo em um tamanho de 120 pontos (largura) por 140 pontos (altura), conforme mostrado na figura a seguir:</span><span class="sxs-lookup"><span data-stu-id="4e210-128">If you change the size to **style**='width:120pt;height:140pt', the oval becomes larger because it is scaled within the new containing box at a size of 120 points (width) by 140 points (height), as shown in the following picture:</span></span>

![oval2.gif (966 bytes)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





<span data-ttu-id="4e210-130">Se você alterar o tamanho para **Style**= ' largura: 60pt; altura: 40pt ', a elipse se tornará menor porque é dimensionada na nova caixa de conteúdo em um tamanho de 60 pontos (largura) por 40 pontos (altura), conforme mostrado na figura a seguir:</span><span class="sxs-lookup"><span data-stu-id="4e210-130">If you change the size to **style**='width:60pt;height:40pt', the oval becomes smaller because it is scaled within the new containing box at a size of 60 points (width) by 40 points (height), as shown in the following picture:</span></span>

![oval3.gif (394 bytes)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 