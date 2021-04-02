---
title: Atributo de flip da VML
description: Atributo de flip da VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641811"
---
# <a name="vml-flip-attribute"></a><span data-ttu-id="388fe-103">Atributo de flip da VML</span><span class="sxs-lookup"><span data-stu-id="388fe-103">VML Flip Attribute</span></span>

<span data-ttu-id="388fe-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="388fe-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="388fe-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="388fe-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="388fe-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="388fe-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="388fe-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="388fe-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="388fe-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="388fe-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="388fe-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="388fe-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="388fe-110">Alterna a orientação de uma forma.</span><span class="sxs-lookup"><span data-stu-id="388fe-110">Switches the orientation of a shape.</span></span> <span data-ttu-id="388fe-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="388fe-111">Read/write.</span></span> <span data-ttu-id="388fe-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="388fe-112">**String**.</span></span>

<span data-ttu-id="388fe-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="388fe-113">**Applies To**</span></span>

[<span data-ttu-id="388fe-114">Forma</span><span class="sxs-lookup"><span data-stu-id="388fe-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="388fe-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="388fe-115">**Tag Syntax**</span></span>

<span data-ttu-id="388fe-116"><v: *Element* estilo = "flip: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="388fe-116"><v: *element* style="flip: *expression* "></span></span>

<span data-ttu-id="388fe-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="388fe-117">**Script Syntax**</span></span>

<span data-ttu-id="388fe-118">*elemento* . Style. flip = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="388fe-118">*element* .style.flip="*expression*"</span></span>

<span data-ttu-id="388fe-119">*expressão* = de *elemento*. Style. flip</span><span class="sxs-lookup"><span data-stu-id="388fe-119">*expression*=*element*.style.flip</span></span>

<span data-ttu-id="388fe-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="388fe-120">**Remarks**</span></span>

<span data-ttu-id="388fe-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="388fe-121">Values include:</span></span>



| <span data-ttu-id="388fe-122">Valor</span><span class="sxs-lookup"><span data-stu-id="388fe-122">Value</span></span> | <span data-ttu-id="388fe-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="388fe-123">Description</span></span>                                           |
|-------|-------------------------------------------------------|
| <span data-ttu-id="388fe-124">x</span><span class="sxs-lookup"><span data-stu-id="388fe-124">x</span></span>     | <span data-ttu-id="388fe-125">Inverter ao longo do eixo y, revertendo as coordenadas *x*.</span><span class="sxs-lookup"><span data-stu-id="388fe-125">Flip along the y-axis, reversing the *x*-coordinates.</span></span> |
| <span data-ttu-id="388fe-126">a</span><span class="sxs-lookup"><span data-stu-id="388fe-126">y</span></span>     | <span data-ttu-id="388fe-127">Inverter ao longo do eixo *x*, revertendo as coordenadas y.</span><span class="sxs-lookup"><span data-stu-id="388fe-127">Flip along the *x*-axis, reversing the y-coordinates.</span></span> |
| <span data-ttu-id="388fe-128">xy</span><span class="sxs-lookup"><span data-stu-id="388fe-128">xy</span></span>    | <span data-ttu-id="388fe-129">Inverta o eixo y e *x*.</span><span class="sxs-lookup"><span data-stu-id="388fe-129">Flip along both the y- and *x*-axis.</span></span>                  |
| <span data-ttu-id="388fe-130">yx</span><span class="sxs-lookup"><span data-stu-id="388fe-130">yx</span></span>    | <span data-ttu-id="388fe-131">Inverta o eixo *x* e *y*.</span><span class="sxs-lookup"><span data-stu-id="388fe-131">Flip along both the *x*- and *y*-axis.</span></span>                |



 

<span data-ttu-id="388fe-132">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="388fe-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="388fe-133">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="388fe-133">**See Also**</span></span>

[<span data-ttu-id="388fe-134">VgFlipOrientation</span><span class="sxs-lookup"><span data-stu-id="388fe-134">VgFlipOrientation</span></span>](msdn-online-vector-markup-language-object-model-reference.md)

<span data-ttu-id="388fe-135">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="388fe-135">**Example**</span></span>

<span data-ttu-id="388fe-136">A forma é invertida ao longo do eixo *y* , revertendo as coordenadas *x* .</span><span class="sxs-lookup"><span data-stu-id="388fe-136">The shape is flipped along the *y* -axis by reversing the *x* -coordinates.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



<span data-ttu-id="388fe-137">[Exemplo de atributo flip](/previous-versions/bb229670(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="388fe-137">[Flip Attribute Example](/previous-versions/bb229670(v=vs.85)).</span></span> <span data-ttu-id="388fe-138">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="388fe-138">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 