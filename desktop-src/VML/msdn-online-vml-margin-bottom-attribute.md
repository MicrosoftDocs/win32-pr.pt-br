---
title: Atributo Margin-Bottom de VML
description: Atributo Margin-Bottom de VML
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35712733179a3c03dc291c4d5efcf4fee68c2865
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641480"
---
# <a name="vml-margin-bottom-attribute"></a><span data-ttu-id="8fbb6-103">Atributo Margin-Bottom de VML</span><span class="sxs-lookup"><span data-stu-id="8fbb6-103">VML Margin-Bottom Attribute</span></span>

<span data-ttu-id="8fbb6-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8fbb6-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8fbb6-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8fbb6-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8fbb6-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8fbb6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8fbb6-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8fbb6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8fbb6-110">Especifica a borda inferior da forma que contém o retângulo em relação à âncora de forma.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-110">Specifies the bottom edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="8fbb6-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-111">Read/write.</span></span> <span data-ttu-id="8fbb6-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-112">**String**.</span></span>

<span data-ttu-id="8fbb6-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="8fbb6-113">**Applies To**</span></span>

[<span data-ttu-id="8fbb6-114">Forma</span><span class="sxs-lookup"><span data-stu-id="8fbb6-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="8fbb6-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="8fbb6-115">**Tag Syntax**</span></span>

<span data-ttu-id="8fbb6-116"><v: *elemento* Margin-Bottom = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="8fbb6-116"><v: *element* margin-bottom=" *expression* "></span></span>

<span data-ttu-id="8fbb6-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="8fbb6-117">**Script Syntax**</span></span>

<span data-ttu-id="8fbb6-118">*Element* . MarginBottom = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="8fbb6-118">*element* .marginbottom="*expression*"</span></span>

<span data-ttu-id="8fbb6-119">*expressão* = de *elemento*. MarginBottom</span><span class="sxs-lookup"><span data-stu-id="8fbb6-119">*expression*=*element*.marginbottom</span></span>

<span data-ttu-id="8fbb6-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="8fbb6-120">**Remarks**</span></span>

<span data-ttu-id="8fbb6-121">O atributo **Margin-Bottom** é semelhante ao atributo padrão **de margem HTML-inferior** usado com folhas de estilo.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-121">The **Margin-Bottom** attribute is similar to the standard HTML **Margin-Bottom** attribute used with style sheets.</span></span>

<span data-ttu-id="8fbb6-122">Observe que **MarginBottom** é usado em vez de **Margin-Bottom** para scripts.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-122">Note that **marginbottom** is used instead of **margin-bottom** for scripting.</span></span> <span data-ttu-id="8fbb6-123">Observe também que, se a **posição** for **absoluta**, a margem não parecerá ser alterada.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="8fbb6-124">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="8fbb6-124">Values include:</span></span>



| <span data-ttu-id="8fbb6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8fbb6-125">Value</span></span>      | <span data-ttu-id="8fbb6-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="8fbb6-126">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbb6-127">Automático</span><span class="sxs-lookup"><span data-stu-id="8fbb6-127">Auto</span></span>       | <span data-ttu-id="8fbb6-128">Posição padrão de um elemento no fluxo da página.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-128">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="8fbb6-129">units</span><span class="sxs-lookup"><span data-stu-id="8fbb6-129">units</span></span>      | <span data-ttu-id="8fbb6-130">Padrão.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-130">Default.</span></span> <span data-ttu-id="8fbb6-131">Um número com um designador de unidades absolutas (cm, mm, em, pt, PC ou px) ou um designador de unidades relativas (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="8fbb6-131">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="8fbb6-132">Se nenhuma unidade for fornecida, serão assumidos pixels (px).</span><span class="sxs-lookup"><span data-stu-id="8fbb6-132">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="8fbb6-133">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-133">The default value is 0.</span></span> |
| <span data-ttu-id="8fbb6-134">percentage</span><span class="sxs-lookup"><span data-stu-id="8fbb6-134">percentage</span></span> | <span data-ttu-id="8fbb6-135">Valor expresso como uma porcentagem da altura do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-135">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="8fbb6-136">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="8fbb6-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="8fbb6-137">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="8fbb6-137">**See Also**</span></span>

[<span data-ttu-id="8fbb6-138">Unidades</span><span class="sxs-lookup"><span data-stu-id="8fbb6-138">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="8fbb6-139">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="8fbb6-139">**Example**</span></span>

<span data-ttu-id="8fbb6-140">A margem inferior é definida como 25 pixels.</span><span class="sxs-lookup"><span data-stu-id="8fbb6-140">The bottom margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



<span data-ttu-id="8fbb6-141">[Exemplo de atributo Margin-Bottom](/previous-versions/bb229675(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8fbb6-141">[Margin-Bottom Attribute Example](/previous-versions/bb229675(v=vs.85)).</span></span> <span data-ttu-id="8fbb6-142">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="8fbb6-142">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 