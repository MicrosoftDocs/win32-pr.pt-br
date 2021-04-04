---
title: Usando o elemento fórmulas
description: Usando o elemento fórmulas
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Web Workshop, elemento formulas
- Criando páginas da Web, elemento formulas
- Linguagem VML (VML), elemento formulas
- VML (linguagem VML), elemento formulas
- elementos gráficos vetoriais, elemento fórmulas
- elemento formulas
- Elementos de VML, fórmulas
- Formas de VML, elemento formulas
- Linguagem VML (VML), definindo caminhos para formas
- VML (linguagem VML), definindo caminhos para formas
- gráficos vetoriais, definição de caminhos para formas
- Formas de VML, definindo caminhos
- definindo caminhos para formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85ce4ebb6eea05895edf974e3ca86b1fa2ad923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007607"
---
# <a name="using-the-formulas-element"></a><span data-ttu-id="6e80d-116">Usando o elemento fórmulas</span><span class="sxs-lookup"><span data-stu-id="6e80d-116">Using the Formulas Element</span></span>

<span data-ttu-id="6e80d-117">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6e80d-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6e80d-118">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="6e80d-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6e80d-119">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="6e80d-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6e80d-120">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="6e80d-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6e80d-121">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6e80d-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6e80d-122">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6e80d-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6e80d-123">Neste tópico, Ilustraremos como usar o `<formulas>` subelemento para definir um caminho ajustável para uma forma.</span><span class="sxs-lookup"><span data-stu-id="6e80d-123">In this topic, we will illustrate how to use the `<formulas>` sub-element to define an adjustable path for a shape.</span></span>

<span data-ttu-id="6e80d-124">Você pode posicionar o <formulas> subelemento dentro `<shape>` ou `<shapetype>` para definir fórmulas que podem variar o caminho de uma forma.</span><span class="sxs-lookup"><span data-stu-id="6e80d-124">You can place the <formulas> sub-element inside `<shape>` or `<shapetype>` to define formulas that can vary the path of a shape.</span></span> <span data-ttu-id="6e80d-125">Dentro do `<formulas>` subelemento, um subelemento **f** define uma fórmula para que um valor seja avaliado com base na fórmula.</span><span class="sxs-lookup"><span data-stu-id="6e80d-125">Inside the `<formulas>` sub-element, one **f** sub-element defines one formula so that one value is evaluated based upon that formula.</span></span> <span data-ttu-id="6e80d-126">Por exemplo, a fórmula `<v:f eqn="prod 10 4 5"/>` define um valor equivalente a "10 x 4/5".</span><span class="sxs-lookup"><span data-stu-id="6e80d-126">For example, the formula, `<v:f eqn="prod 10 4 5"/>` defines a value that is equivalent to "10 x 4 / 5".</span></span>

<span data-ttu-id="6e80d-127">Você pode inserir muitos elementos **f** dentro de um `<formulas>` subelemento.</span><span class="sxs-lookup"><span data-stu-id="6e80d-127">You can place many **f** sub-elements inside one`<formulas>` sub-element.</span></span> <span data-ttu-id="6e80d-128">As fórmulas podem referenciar os valores que são definidos anteriormente em outras fórmulas dentro do mesmo `<formulas>` subelemento.</span><span class="sxs-lookup"><span data-stu-id="6e80d-128">Formulas can reference the values that are defined earlier in other formulas within the same `<formulas>` sub-element.</span></span> <span data-ttu-id="6e80d-129">O valor definido na primeira fórmula pode ser referido como @0 , o valor definido na segunda fórmula pode ser referido como @1 , e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6e80d-129">The value that is defined in the first formula can be referred to as @0, the value that is defined in the second formula can be referred to as @1, and so on.</span></span>

<span data-ttu-id="6e80d-130">Além disso, você pode especificar o atributo de propriedade **adj** do `<shape>` elemento, como adj = "100, 200, 150".</span><span class="sxs-lookup"><span data-stu-id="6e80d-130">In addition, you can specify the **adj** property attribute of the `<shape>` element, such as adj="100, 200, 150".</span></span> <span data-ttu-id="6e80d-131">Dentro do `<formulas>` elemento, você pode fazer referência a esses valores na lista de **adj** .</span><span class="sxs-lookup"><span data-stu-id="6e80d-131">Inside the `<formulas>` element, you can then reference those values in the **adj** list.</span></span> <span data-ttu-id="6e80d-132">O primeiro valor (100) na lista de **adj** pode ser referido como \# 0, o segundo valor (200) pode ser referido como \# 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6e80d-132">The first value (100) in the **adj** list can be referred to as \#0, the second value (200) can be referred to as \#1, and so on.</span></span>

<span data-ttu-id="6e80d-133">Por exemplo, para desenhar um sorriso, você pode digitar a seguinte representação de VML:</span><span class="sxs-lookup"><span data-stu-id="6e80d-133">For example, to draw a smiling face, you can type the following VML representation:</span></span>

![shape1.gif (735 bytes)](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   <span data-ttu-id="6e80d-135">`adj="17520"` define um valor (= 17520).</span><span class="sxs-lookup"><span data-stu-id="6e80d-135">`adj="17520"` defines a value (= 17520).</span></span> <span data-ttu-id="6e80d-136">Esse valor pode ser referenciado como \# 0.</span><span class="sxs-lookup"><span data-stu-id="6e80d-136">This value can be referenced as \#0.</span></span>
-   <span data-ttu-id="6e80d-137">A primeira fórmula, `<v:f eqn="sum 33030 0 #0"/>` , define o valor (= 33030 + 0- \# 0).</span><span class="sxs-lookup"><span data-stu-id="6e80d-137">The first formula, `<v:f eqn="sum 33030 0 #0"/>`, defines the value (= 33030 + 0 - \#0).</span></span> <span data-ttu-id="6e80d-138">Esse valor pode ser referenciado como @0 .</span><span class="sxs-lookup"><span data-stu-id="6e80d-138">This value can be referenced as @0.</span></span>
-   <span data-ttu-id="6e80d-139">A segunda fórmula, `<v:f eqn="prod #0 4 3"/>` , define o valor (= \# 0 \* 4/3).</span><span class="sxs-lookup"><span data-stu-id="6e80d-139">The second formula, `<v:f eqn="prod #0 4 3"/>`, defines the value (= \#0 \* 4 / 3).</span></span> <span data-ttu-id="6e80d-140">Esse valor pode ser referenciado como @1 .</span><span class="sxs-lookup"><span data-stu-id="6e80d-140">This value can be referenced as @1.</span></span>
-   <span data-ttu-id="6e80d-141">A terceira fórmula, `<v:f eqn="prod @0 1 3"/>` , define o valor (= @0 \* 1/3).</span><span class="sxs-lookup"><span data-stu-id="6e80d-141">The third formula, `<v:f eqn="prod @0 1 3"/>`, defines the value (= @0 \* 1 / 3).</span></span> <span data-ttu-id="6e80d-142">Esse valor pode ser referenciado como @2 .</span><span class="sxs-lookup"><span data-stu-id="6e80d-142">This value can be referenced as @2.</span></span>
-   <span data-ttu-id="6e80d-143">A quarta fórmula, `<v:f eqn="sum @1 0 @2"/>` , define o valor (= @1 + 0 -@2 ).</span><span class="sxs-lookup"><span data-stu-id="6e80d-143">The fourth formula, `<v:f eqn="sum @1 0 @2"/>`, defines the value (=@1 + 0 -@2).</span></span> <span data-ttu-id="6e80d-144">Esse valor pode ser referenciado como @3 .</span><span class="sxs-lookup"><span data-stu-id="6e80d-144">This value can be referenced as @3.</span></span>
-   <span data-ttu-id="6e80d-145">Dentro do `<path>` elemento, os valores definidos nas @0 fórmulas First () e quarta ( @3 ) são usados para determinar o contorno da forma.</span><span class="sxs-lookup"><span data-stu-id="6e80d-145">Inside the `<path>` element, the values defined in the first (@0) and the fourth (@3) formulas are used to determine the outline of the shape.</span></span>

<span data-ttu-id="6e80d-146">Se você alterar a lista de **adj** , como `adj="20000"` , os valores das fórmulas que fazem referência à lista de **adj** também serão alterados, afetando o sorriso da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6e80d-146">If you change the **adj** list, such as `adj="20000"`, the values of the formulas that reference the **adj** list will be changed as well, affecting the smiling face as follows:</span></span>

![shape2.gif (765 bytes)](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





<span data-ttu-id="6e80d-148">Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858392) .</span><span class="sxs-lookup"><span data-stu-id="6e80d-148">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858392) .</span></span>

 

 