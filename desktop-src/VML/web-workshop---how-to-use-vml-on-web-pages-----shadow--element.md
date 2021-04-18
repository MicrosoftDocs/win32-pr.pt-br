---
title: Usando o elemento Shadow
description: Usando o elemento Shadow
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Web Workshop, elemento Shadow
- Criando páginas da Web, elemento Shadow
- Linguagem VML (VML), elemento Shadow
- VML (linguagem VML), elemento Shadow
- gráficos vetoriais, elemento Shadow
- elemento Shadow
- Elementos de VML, sombra
- Formas de VML, elemento Shadow
- Linguagem VML (VML), desenho com efeitos de sombra
- VML (linguagem VML), desenho com efeitos de sombra
- gráficos vetoriais, desenho com efeitos de sombra
- Formas de VML, desenho com efeitos de sombra
- desenho com efeitos de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe32651fbeab6b84b49a40bae05a08ba3d9c33a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366615"
---
# <a name="using-the-shadow-element"></a><span data-ttu-id="75b68-116">Usando o elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="75b68-116">Using the Shadow Element</span></span>

<span data-ttu-id="75b68-117">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="75b68-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="75b68-118">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="75b68-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="75b68-119">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="75b68-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="75b68-120">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="75b68-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="75b68-121">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="75b68-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="75b68-122">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="75b68-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="75b68-123">Neste tópico, Ilustraremos como usar o `<shadow>` subelemento para desenhar uma forma que tenha vários efeitos de sombra.</span><span class="sxs-lookup"><span data-stu-id="75b68-123">In this topic, we will illustrate how to use the `<shadow>` sub-element to draw a shape that has various shadow effects.</span></span>

<span data-ttu-id="75b68-124">Você pode posicionar o `<shadow>` subelemento dentro do `<shape>` , `<shapetype>` ou qualquer elemento Shape predefinido para desenhar uma forma com uma sombra.</span><span class="sxs-lookup"><span data-stu-id="75b68-124">You can place the `<shadow>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to draw a shape with a shadow.</span></span> <span data-ttu-id="75b68-125">Você pode usar os atributos de Propriedade do `<shadow>` subelemento para personalizar a sombra.</span><span class="sxs-lookup"><span data-stu-id="75b68-125">You can then use the property attributes of the `<shadow>` sub-element to customize the shadow.</span></span>

<span data-ttu-id="75b68-126">Por exemplo, para criar uma forma com uma sombra, conforme mostrado na imagem a seguir, você pode digitar as seguintes linhas na `<BODY>` região da sua página da Web:</span><span class="sxs-lookup"><span data-stu-id="75b68-126">For example, to create a shape with a shadow, as shown in the following picture, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![shape1.gif (887 bytes)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   <span data-ttu-id="75b68-128">`on="t"` e `type="perspective"` indique ativar a sombra usando o tipo de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="75b68-128">`on="t"` and `type="perspective"` indicate to turn on the shadow using the perspective type.</span></span>
-   <span data-ttu-id="75b68-129">A **origem** e o **deslocamento** indicam onde desenhar a sombra.</span><span class="sxs-lookup"><span data-stu-id="75b68-129">The **origin** and **offset** indicate where to draw the shadow.</span></span>
-   <span data-ttu-id="75b68-130">`matrix="..."` Especifica a matriz de transformação de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="75b68-130">`matrix="..."` specifies the perspective transform matrix.</span></span>

<span data-ttu-id="75b68-131">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span><span class="sxs-lookup"><span data-stu-id="75b68-131">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span></span>

 

 