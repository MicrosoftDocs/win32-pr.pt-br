---
title: Usando o elemento Handles
description: Usando o elemento Handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Web Workshop, elemento Handles
- Criando páginas da Web, elemento Handles
- Linguagem VML (VML), elemento Handles
- VML (linguagem VML), elemento Handles
- elementos gráficos vetoriais, elemento Handles
- elemento Handles
- Elementos de VML, identificadores
- Formas de VML, elemento Handles
- Linguagem VML (VML), anexando texto a formas
- VML (linguagem VML), anexando texto a formas
- gráficos vetoriais, anexando texto a formas
- Formas de VML, anexando texto
- anexando texto a formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54c721d50f51c46cd4bf08393e85ad83307fc1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007606"
---
# <a name="using-the-handles-element"></a><span data-ttu-id="d27c0-116">Usando o elemento Handles</span><span class="sxs-lookup"><span data-stu-id="d27c0-116">Using the Handles Element</span></span>

<span data-ttu-id="d27c0-117">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d27c0-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d27c0-118">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="d27c0-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d27c0-119">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="d27c0-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d27c0-120">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="d27c0-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d27c0-121">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d27c0-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d27c0-122">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d27c0-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d27c0-123">Neste tópico, Ilustraremos como usar o `<handles>` elemento para anexar texto a uma forma.</span><span class="sxs-lookup"><span data-stu-id="d27c0-123">In this topic, we will illustrate how to use the `<handles>` element to attach text to a shape.</span></span>

<span data-ttu-id="d27c0-124">Você pode posicionar o `<handles>` subelemento dentro `<shape>` ou `<shapetype>` para definir elementos de interface do usuário que podem variar os valores de **adj** na forma.</span><span class="sxs-lookup"><span data-stu-id="d27c0-124">You can place the `<handles>` sub-element inside `<shape>` or `<shapetype>` to define user interface elements that can vary the **adj** values on the shape.</span></span>

<span data-ttu-id="d27c0-125">Por exemplo, como mostra a representação de VML a seguir, você pode fornecer um identificador de ajuste (caixa amarela) que os usuários podem simplesmente arrastar para ajustar a forma.</span><span class="sxs-lookup"><span data-stu-id="d27c0-125">For example, as shown the following VML representation, you can provide an adjust handle (yellow box) that users can simply drag to adjust the shape.</span></span>

<span data-ttu-id="d27c0-126">Observação: as alças estão disponíveis quando essa forma VML é exibida em aplicativos Microsoft Office, em que a forma é destinada a ser manipulable.</span><span class="sxs-lookup"><span data-stu-id="d27c0-126">Note: the handles are available when this VML shape is viewed in Microsoft Office applications, where the shape is intended to be manipulable.</span></span>

![shape1.gif (564 bytes)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="d27c0-128">Observe que a única diferença entre a representação VML anterior e a seguinte é o valor de **adj** .</span><span class="sxs-lookup"><span data-stu-id="d27c0-128">Notice that the only difference between the preceding VML representation and the following one is the **adj** value.</span></span>

![shape2.gif (1361 bytes)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="d27c0-130">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span><span class="sxs-lookup"><span data-stu-id="d27c0-130">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span></span>

 

 