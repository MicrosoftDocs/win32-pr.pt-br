---
title: Atributo Font-Weight de VML
description: Atributo Font-Weight de VML
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e4de8a1bb4132c75d4520dcacc661fbbc97eef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366227"
---
# <a name="vml-font-weight-attribute"></a><span data-ttu-id="acf4a-103">Atributo Font-Weight de VML</span><span class="sxs-lookup"><span data-stu-id="acf4a-103">VML Font-Weight Attribute</span></span>

<span data-ttu-id="acf4a-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="acf4a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="acf4a-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="acf4a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="acf4a-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="acf4a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="acf4a-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="acf4a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="acf4a-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="acf4a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="acf4a-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="acf4a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="acf4a-110">Define a espessura das letras da fonte.</span><span class="sxs-lookup"><span data-stu-id="acf4a-110">Defines the thickness of the letters of the font.</span></span> <span data-ttu-id="acf4a-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="acf4a-111">Read/write.</span></span> <span data-ttu-id="acf4a-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="acf4a-112">**String**.</span></span>

<span data-ttu-id="acf4a-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="acf4a-113">**Applies To**</span></span>

[<span data-ttu-id="acf4a-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="acf4a-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="acf4a-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="acf4a-115">**Tag Syntax**</span></span>

<span data-ttu-id="acf4a-116"><v: *elemento* Style = "fonte-peso: *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="acf4a-116"><v: *element* style="font-weight: *expression* "></span></span>

<span data-ttu-id="acf4a-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="acf4a-117">**Script Syntax**</span></span>

<span data-ttu-id="acf4a-118">*elemento* . Style. EspessuraDaFonte = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="acf4a-118">*element* .style.fontweight="*expression*"</span></span>

<span data-ttu-id="acf4a-119">*expressão* = de *elemento*. Style. EspessuraDaFonte</span><span class="sxs-lookup"><span data-stu-id="acf4a-119">*expression*=*element*.style.fontweight</span></span>

<span data-ttu-id="acf4a-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="acf4a-120">**Remarks**</span></span>

<span data-ttu-id="acf4a-121">Os valores são os mesmos que os atributos de estilo HTML padrão.</span><span class="sxs-lookup"><span data-stu-id="acf4a-121">The values are the same as the standard HTML style attributes.</span></span> <span data-ttu-id="acf4a-122">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="acf4a-122">Values include:</span></span>



| <span data-ttu-id="acf4a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="acf4a-123">Value</span></span>   | <span data-ttu-id="acf4a-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="acf4a-124">Description</span></span>                                                                 |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="acf4a-125">normal</span><span class="sxs-lookup"><span data-stu-id="acf4a-125">normal</span></span>  | <span data-ttu-id="acf4a-126">Normal.</span><span class="sxs-lookup"><span data-stu-id="acf4a-126">Normal.</span></span> <span data-ttu-id="acf4a-127">Padrão.</span><span class="sxs-lookup"><span data-stu-id="acf4a-127">Default.</span></span>                                                            |
| <span data-ttu-id="acf4a-128">negrito</span><span class="sxs-lookup"><span data-stu-id="acf4a-128">bold</span></span>    | <span data-ttu-id="acf4a-129">Aplique.</span><span class="sxs-lookup"><span data-stu-id="acf4a-129">Bold.</span></span>                                                                       |
| <span data-ttu-id="acf4a-130">bolder</span><span class="sxs-lookup"><span data-stu-id="acf4a-130">bolder</span></span>  | <span data-ttu-id="acf4a-131">Mais pesado do que o normal.</span><span class="sxs-lookup"><span data-stu-id="acf4a-131">Heavier than normal.</span></span>                                                        |
| <span data-ttu-id="acf4a-132">lighter</span><span class="sxs-lookup"><span data-stu-id="acf4a-132">lighter</span></span> | <span data-ttu-id="acf4a-133">Mais claro do que o normal.</span><span class="sxs-lookup"><span data-stu-id="acf4a-133">Lighter than normal.</span></span>                                                        |
| <span data-ttu-id="acf4a-134">100</span><span class="sxs-lookup"><span data-stu-id="acf4a-134">100</span></span>     | <span data-ttu-id="acf4a-135">Pelo menos tão leve quanto o peso de 200.</span><span class="sxs-lookup"><span data-stu-id="acf4a-135">At least as light as the 200 weight.</span></span>                                        |
| <span data-ttu-id="acf4a-136">200</span><span class="sxs-lookup"><span data-stu-id="acf4a-136">200</span></span>     | <span data-ttu-id="acf4a-137">Pelo menos, em negrito, como o peso de 100 e pelo menos tão leve quanto o peso de 300.</span><span class="sxs-lookup"><span data-stu-id="acf4a-137">At least as bold as the 100 weight and at least as light as the 300 weight.</span></span> |
| <span data-ttu-id="acf4a-138">300</span><span class="sxs-lookup"><span data-stu-id="acf4a-138">300</span></span>     | <span data-ttu-id="acf4a-139">Pelo menos, em negrito, como o peso de 200 e pelo menos tão leve quanto o peso de 400.</span><span class="sxs-lookup"><span data-stu-id="acf4a-139">At least as bold as the 200 weight and at least as light as the 400 weight.</span></span> |
| <span data-ttu-id="acf4a-140">400</span><span class="sxs-lookup"><span data-stu-id="acf4a-140">400</span></span>     | <span data-ttu-id="acf4a-141">Normal.</span><span class="sxs-lookup"><span data-stu-id="acf4a-141">Normal.</span></span>                                                                     |
| <span data-ttu-id="acf4a-142">500</span><span class="sxs-lookup"><span data-stu-id="acf4a-142">500</span></span>     | <span data-ttu-id="acf4a-143">Pelo menos, em negrito, como o peso de 400 e pelo menos tão leve quanto o peso de 600.</span><span class="sxs-lookup"><span data-stu-id="acf4a-143">At least as bold as the 400 weight and at least as light as the 600 weight.</span></span> |
| <span data-ttu-id="acf4a-144">600</span><span class="sxs-lookup"><span data-stu-id="acf4a-144">600</span></span>     | <span data-ttu-id="acf4a-145">Pelo menos, em negrito, como o peso de 500 e pelo menos tão leve quanto o peso de 700.</span><span class="sxs-lookup"><span data-stu-id="acf4a-145">At least as bold as the 500 weight and at least as light as the 700 weight.</span></span> |
| <span data-ttu-id="acf4a-146">700</span><span class="sxs-lookup"><span data-stu-id="acf4a-146">700</span></span>     | <span data-ttu-id="acf4a-147">Aplique.</span><span class="sxs-lookup"><span data-stu-id="acf4a-147">Bold.</span></span>                                                                       |
| <span data-ttu-id="acf4a-148">800</span><span class="sxs-lookup"><span data-stu-id="acf4a-148">800</span></span>     | <span data-ttu-id="acf4a-149">Pelo menos, em negrito, como o peso de 700 e pelo menos tão leve quanto o peso de 900.</span><span class="sxs-lookup"><span data-stu-id="acf4a-149">At least as bold as the 700 weight and at least as light as the 900 weight.</span></span> |
| <span data-ttu-id="acf4a-150">900</span><span class="sxs-lookup"><span data-stu-id="acf4a-150">900</span></span>     | <span data-ttu-id="acf4a-151">Pelo menos em negrito como o peso de 800.</span><span class="sxs-lookup"><span data-stu-id="acf4a-151">At least as bold as the 800 weight.</span></span>                                         |



 

<span data-ttu-id="acf4a-152">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="acf4a-152">*VML Standard Attribute*</span></span>

<span data-ttu-id="acf4a-153">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="acf4a-153">**Example**</span></span>

<span data-ttu-id="acf4a-154">A espessura da fonte é negrito.</span><span class="sxs-lookup"><span data-stu-id="acf4a-154">The font weight is bold.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 