---
title: Usando o elemento TextPath
description: Usando o elemento TextPath
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Web Workshop, elemento TextPath
- Criando páginas da Web, elemento TextPath
- Linguagem VML (VML), elemento TextPath
- VML (linguagem VML), elemento TextPath
- gráficos vetoriais, elemento TextPath
- elemento TextPath
- Elementos de VML, TextPath
- Formas de VML, elemento TextPath
- Linguagem VML (VML), texto de desenho
- VML (linguagem VML), texto de desenho
- gráficos vetoriais, desenho de texto em VML
- desenhando texto
- Formas de VML, texto de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c032d14307dc07ec56911f4c5cc45a4c69664
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084855"
---
# <a name="using-the-textpath-element"></a><span data-ttu-id="781c4-116">Usando o elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="781c4-116">Using the Textpath Element</span></span>

<span data-ttu-id="781c4-117">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="781c4-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="781c4-118">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="781c4-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="781c4-119">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="781c4-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="781c4-120">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="781c4-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="781c4-121">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="781c4-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="781c4-122">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="781c4-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="781c4-123">Neste tópico, Ilustraremos como usar o `<textpath>` elemento para desenhar texto com vários estilos.</span><span class="sxs-lookup"><span data-stu-id="781c4-123">In this topic, we will illustrate how to use the `<textpath>` element to draw text with various styles.</span></span>

<span data-ttu-id="781c4-124">Você pode posicionar o `<textpath>` subelemento dentro `<shape>` ou `<shapetype>` para desenhar o texto.</span><span class="sxs-lookup"><span data-stu-id="781c4-124">You can place the `<textpath>` sub-element inside `<shape>` or `<shapetype>` to draw text.</span></span> <span data-ttu-id="781c4-125">Você pode usar os atributos de Propriedade do `<textpath>` subelemento para personalizar o texto.</span><span class="sxs-lookup"><span data-stu-id="781c4-125">You can then use the property attributes of the `<textpath>` sub-element to customize the text.</span></span> <span data-ttu-id="781c4-126">Você também pode usar o `<formulas>` subelemento para definir a estrutura de tópicos do texto.</span><span class="sxs-lookup"><span data-stu-id="781c4-126">You can also use the `<formulas>` sub-element to define the outline of the text.</span></span>

<span data-ttu-id="781c4-127">Por exemplo, para criar o texto mostrado na imagem a seguir, você pode digitar a representação de VML abaixo.</span><span class="sxs-lookup"><span data-stu-id="781c4-127">For example, to create the text shown in the following picture, you can type the VML representation below.</span></span> <span data-ttu-id="781c4-128">Observe que usamos o `<shapetype>` elemento para definir um protótipo para o contorno do texto.</span><span class="sxs-lookup"><span data-stu-id="781c4-128">Notice that we use the `<shapetype>` element to define a prototype for the outline of the text.</span></span> <span data-ttu-id="781c4-129">Em seguida, criamos uma instância de duas formas a partir do mesmo ShapeType.</span><span class="sxs-lookup"><span data-stu-id="781c4-129">We then instantiate two shapes from the same shapetype.</span></span> <span data-ttu-id="781c4-130">Você pode simplesmente alterar o atributo de propriedade da **cadeia de caracteres** para exibir texto diferente.</span><span class="sxs-lookup"><span data-stu-id="781c4-130">You can simply change the **string** property attribute to display different text.</span></span>

![\-1.gif Shape1 (4898 bytes)](images/shape1-1t.gif)

![\-2.gif Shape1 (2789 bytes)](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





<span data-ttu-id="781c4-133">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858398) .</span><span class="sxs-lookup"><span data-stu-id="781c4-133">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858398) .</span></span>

 

 