---
title: Atributo DashStyle de VML
description: Atributo DashStyle de VML
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294120"
---
# <a name="vml-dashstyle-attribute"></a><span data-ttu-id="e99d2-103">Atributo DashStyle de VML</span><span class="sxs-lookup"><span data-stu-id="e99d2-103">VML DashStyle Attribute</span></span>

<span data-ttu-id="e99d2-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e99d2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e99d2-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="e99d2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e99d2-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="e99d2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e99d2-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="e99d2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e99d2-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e99d2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e99d2-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e99d2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e99d2-110">Especifica o padrão de ponto e tracejado para um traço.</span><span class="sxs-lookup"><span data-stu-id="e99d2-110">Specifies the dot and dash pattern for a stroke.</span></span> <span data-ttu-id="e99d2-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e99d2-111">Read/write.</span></span> <span data-ttu-id="e99d2-112">**VgLineDashStyle**.</span><span class="sxs-lookup"><span data-stu-id="e99d2-112">**VgLineDashStyle**.</span></span>

<span data-ttu-id="e99d2-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="e99d2-113">**Applies To**</span></span>

[<span data-ttu-id="e99d2-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="e99d2-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="e99d2-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="e99d2-115">**Tag Syntax**</span></span>

<span data-ttu-id="e99d2-116"><v: *Element* DashStyle = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="e99d2-116"><v: *element* dashstyle=" *expression* "></span></span>

<span data-ttu-id="e99d2-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="e99d2-117">**Script Syntax**</span></span>

<span data-ttu-id="e99d2-118">*Element* . DashStyle = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="e99d2-118">*element* .dashstyle="*expression*"</span></span>

<span data-ttu-id="e99d2-119">*expressão* = de *elemento*. DashStyle</span><span class="sxs-lookup"><span data-stu-id="e99d2-119">*expression*=*element*.dashstyle</span></span>

<span data-ttu-id="e99d2-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="e99d2-120">**Remarks**</span></span>

<span data-ttu-id="e99d2-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="e99d2-121">Values include:</span></span>

-   <span data-ttu-id="e99d2-122">Solid (padrão)</span><span class="sxs-lookup"><span data-stu-id="e99d2-122">Solid (default)</span></span>
-   <span data-ttu-id="e99d2-123">ShortDash</span><span class="sxs-lookup"><span data-stu-id="e99d2-123">ShortDash</span></span>
-   <span data-ttu-id="e99d2-124">ShortDot</span><span class="sxs-lookup"><span data-stu-id="e99d2-124">ShortDot</span></span>
-   <span data-ttu-id="e99d2-125">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="e99d2-125">ShortDashDot</span></span>
-   <span data-ttu-id="e99d2-126">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="e99d2-126">ShortDashDotDot</span></span>
-   <span data-ttu-id="e99d2-127">Ponto</span><span class="sxs-lookup"><span data-stu-id="e99d2-127">Dot</span></span>
-   <span data-ttu-id="e99d2-128">Traço</span><span class="sxs-lookup"><span data-stu-id="e99d2-128">Dash</span></span>
-   <span data-ttu-id="e99d2-129">LongDash</span><span class="sxs-lookup"><span data-stu-id="e99d2-129">LongDash</span></span>
-   <span data-ttu-id="e99d2-130">DashDot</span><span class="sxs-lookup"><span data-stu-id="e99d2-130">DashDot</span></span>
-   <span data-ttu-id="e99d2-131">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="e99d2-131">LongDashDot</span></span>
-   <span data-ttu-id="e99d2-132">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="e99d2-132">LongDashDotDot</span></span>

<span data-ttu-id="e99d2-133">O atributo **DashStyle** permite que o usuário especifique um padrão de traço definido por personalizado.</span><span class="sxs-lookup"><span data-stu-id="e99d2-133">The **DashStyle** attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="e99d2-134">Isso é feito usando uma série de números.</span><span class="sxs-lookup"><span data-stu-id="e99d2-134">This is done using a series of numbers.</span></span> <span data-ttu-id="e99d2-135">Os estilos de traço são definidos em termos do comprimento do traço (a parte desenhada do traço) e o comprimento do espaço entre os traços.</span><span class="sxs-lookup"><span data-stu-id="e99d2-135">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="e99d2-136">Os comprimentos são relativos à largura da linha: um comprimento de "1" é igual à largura da linha.</span><span class="sxs-lookup"><span data-stu-id="e99d2-136">The lengths are relative to the line width: a length of "1" is equal to the line width.</span></span> <span data-ttu-id="e99d2-137">O estilo **EndCap** é aplicado a cada Dash, o estilo de seta não é.</span><span class="sxs-lookup"><span data-stu-id="e99d2-137">The **EndCap** style is applied to each dash, the arrow style is not.</span></span> <span data-ttu-id="e99d2-138">A cadeia de caracteres define primeiro o comprimento do traço em seguida, o comprimento do espaço.</span><span class="sxs-lookup"><span data-stu-id="e99d2-138">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="e99d2-139">Isso pode ser repetido para formar estilos de traço complexos.</span><span class="sxs-lookup"><span data-stu-id="e99d2-139">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="e99d2-140">A cadeia de caracteres sempre deve conter um par de números; Se ele contiver um número ímpar de números, o último pode ser desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="e99d2-140">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span>

<span data-ttu-id="e99d2-141">A tabela a seguir lista alguns valores típicos e uma descrição do efeito pretendido.</span><span class="sxs-lookup"><span data-stu-id="e99d2-141">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="e99d2-142">"0" implica um ponto que deve ser consta simétrico (com Caps de extremidade arredondado deve ser um círculo).</span><span class="sxs-lookup"><span data-stu-id="e99d2-142">"0" implies a dot that should be fourfold symmetrical (with round end caps it should be a circle).</span></span> <span data-ttu-id="e99d2-143">Se a ponta de extremidade de linha for "simples", um visualizador deverá escolher um sistema operacional interno, onde for possível (em outras palavras.</span><span class="sxs-lookup"><span data-stu-id="e99d2-143">If the line end cap is "flat," a viewer should choose a built-in operating system dash where possible (in other words.</span></span> <span data-ttu-id="e99d2-144">algo que é rápido de desenhar.).</span><span class="sxs-lookup"><span data-stu-id="e99d2-144">something that is fast to draw.).</span></span> <span data-ttu-id="e99d2-145">A tabela a seguir mostra alguns exemplos.</span><span class="sxs-lookup"><span data-stu-id="e99d2-145">The following table shows some examples.</span></span>



| <span data-ttu-id="e99d2-146">DashStyle</span><span class="sxs-lookup"><span data-stu-id="e99d2-146">DashStyle</span></span>     | <span data-ttu-id="e99d2-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="e99d2-147">Description</span></span>                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e99d2-148">"2 2"</span><span class="sxs-lookup"><span data-stu-id="e99d2-148">"2 2"</span></span>         | <span data-ttu-id="e99d2-149">Traços curtos.</span><span class="sxs-lookup"><span data-stu-id="e99d2-149">Short-dashes.</span></span> <span data-ttu-id="e99d2-150">Cada traço e o espaço entre o é o dobro da largura da linha.</span><span class="sxs-lookup"><span data-stu-id="e99d2-150">Each dash and the space between is twice the width of the line.</span></span>                        |
| <span data-ttu-id="e99d2-151">"0 2"</span><span class="sxs-lookup"><span data-stu-id="e99d2-151">"0 2"</span></span>         | <span data-ttu-id="e99d2-152">Pontilha.</span><span class="sxs-lookup"><span data-stu-id="e99d2-152">Dots.</span></span> <span data-ttu-id="e99d2-153">O espaço entre é duas vezes a largura da linha.</span><span class="sxs-lookup"><span data-stu-id="e99d2-153">Space between is twice the width of the line.</span></span>                                                  |
| <span data-ttu-id="e99d2-154">"2 2 0 2"</span><span class="sxs-lookup"><span data-stu-id="e99d2-154">"2 2 0 2"</span></span>     | <span data-ttu-id="e99d2-155">Traço curto ponto.</span><span class="sxs-lookup"><span data-stu-id="e99d2-155">Short dash dot.</span></span>                                                                                      |
| <span data-ttu-id="e99d2-156">"2 2 0 2 0 2"</span><span class="sxs-lookup"><span data-stu-id="e99d2-156">"2 2 0 2 0 2"</span></span> | <span data-ttu-id="e99d2-157">Traço ponto curto ponto.</span><span class="sxs-lookup"><span data-stu-id="e99d2-157">Short dash dot dot.</span></span>                                                                                  |
| <span data-ttu-id="e99d2-158">"1 2"</span><span class="sxs-lookup"><span data-stu-id="e99d2-158">"1 2"</span></span>         | <span data-ttu-id="e99d2-159">Final.</span><span class="sxs-lookup"><span data-stu-id="e99d2-159">Dot.</span></span> <span data-ttu-id="e99d2-160">Cada traço é a largura da linha, enquanto cada espaço é o dobro da largura da linha.</span><span class="sxs-lookup"><span data-stu-id="e99d2-160">Each dash is the width of the line, while each space is twice the width of the line.</span></span>            |
| <span data-ttu-id="e99d2-161">"4 2"</span><span class="sxs-lookup"><span data-stu-id="e99d2-161">"4 2"</span></span>         | <span data-ttu-id="e99d2-162">Dash.</span><span class="sxs-lookup"><span data-stu-id="e99d2-162">Dash.</span></span> <span data-ttu-id="e99d2-163">Cada traço é quatro vezes a largura da linha, enquanto cada espaço é o dobro da largura da linha.</span><span class="sxs-lookup"><span data-stu-id="e99d2-163">Each dash is four times the width of the line while each space is twice the width of the line.</span></span> |
| <span data-ttu-id="e99d2-164">"8 2"</span><span class="sxs-lookup"><span data-stu-id="e99d2-164">"8 2"</span></span>         | <span data-ttu-id="e99d2-165">Tracejado longo.</span><span class="sxs-lookup"><span data-stu-id="e99d2-165">Long dash.</span></span>                                                                                           |
| <span data-ttu-id="e99d2-166">"4 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="e99d2-166">"4 2 1 2"</span></span>     | <span data-ttu-id="e99d2-167">Traço ponto.</span><span class="sxs-lookup"><span data-stu-id="e99d2-167">Dash dot.</span></span>                                                                                            |
| <span data-ttu-id="e99d2-168">"8 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="e99d2-168">"8 2 1 2"</span></span>     | <span data-ttu-id="e99d2-169">Ponto de tracejado longo.</span><span class="sxs-lookup"><span data-stu-id="e99d2-169">Long dash dot.</span></span>                                                                                       |
| <span data-ttu-id="e99d2-170">"8 2 1 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="e99d2-170">"8 2 1 2 1 2"</span></span> | <span data-ttu-id="e99d2-171">Ponto longo de ponto pontilhado.</span><span class="sxs-lookup"><span data-stu-id="e99d2-171">Long dash dot dot.</span></span>                                                                                   |



 

<span data-ttu-id="e99d2-172">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="e99d2-172">*VML Standard Attribute*</span></span>

<span data-ttu-id="e99d2-173">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="e99d2-173">**Example**</span></span>

<span data-ttu-id="e99d2-174">A forma tem um estilo tracejado de traços e pontilhados alternados.</span><span class="sxs-lookup"><span data-stu-id="e99d2-174">The shape has a dash style of alternating dashes and dots.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 