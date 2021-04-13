---
title: Atributo de tipo (sombra) (VML)
description: Atributo de tipo (sombra) (VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366362"
---
# <a name="type-attribute-shadowvml"></a><span data-ttu-id="ac681-103">Atributo de tipo (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="ac681-103">Type Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="ac681-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ac681-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ac681-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="ac681-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ac681-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="ac681-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ac681-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="ac681-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ac681-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ac681-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ac681-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ac681-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ac681-110">Especifica o tipo de sombra.</span><span class="sxs-lookup"><span data-stu-id="ac681-110">Specifies the type of shadow.</span></span> <span data-ttu-id="ac681-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ac681-111">Read/write.</span></span> <span data-ttu-id="ac681-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="ac681-112">**String**.</span></span>

<span data-ttu-id="ac681-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="ac681-113">**Applies To**</span></span>

[<span data-ttu-id="ac681-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="ac681-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="ac681-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="ac681-115">**Tag Syntax**</span></span>

<span data-ttu-id="ac681-116"><v: tipo de *elemento* = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="ac681-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="ac681-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="ac681-117">**Script Syntax**</span></span>

<span data-ttu-id="ac681-118">*elemento* . Type = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="ac681-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="ac681-119">*expressão* = de *elemento*. Type</span><span class="sxs-lookup"><span data-stu-id="ac681-119">*expression*=*element*.type</span></span>

<span data-ttu-id="ac681-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="ac681-120">**Remarks**</span></span>

<span data-ttu-id="ac681-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="ac681-121">Values include:</span></span>



| <span data-ttu-id="ac681-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ac681-122">Value</span></span>           | <span data-ttu-id="ac681-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac681-123">Description</span></span>                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac681-124">único</span><span class="sxs-lookup"><span data-stu-id="ac681-124">single</span></span>          | <span data-ttu-id="ac681-125">Sombra única.</span><span class="sxs-lookup"><span data-stu-id="ac681-125">Single shadow.</span></span> <span data-ttu-id="ac681-126">Padrão.</span><span class="sxs-lookup"><span data-stu-id="ac681-126">Default.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="ac681-127">double</span><span class="sxs-lookup"><span data-stu-id="ac681-127">double</span></span>          | <span data-ttu-id="ac681-128">Uma sombra dupla.</span><span class="sxs-lookup"><span data-stu-id="ac681-128">A double shadow.</span></span> <span data-ttu-id="ac681-129">[Color2](color2-attribute--shadow--vml.md) é usado para a cor da segunda sombra e [Offset2](msdn-online-vml-offset2-attribute.md) é usado para o deslocamento da segunda sombra.</span><span class="sxs-lookup"><span data-stu-id="ac681-129">[Color2](color2-attribute--shadow--vml.md) is used for the color of the second shadow and [Offset2](msdn-online-vml-offset2-attribute.md) is used for the second shadow's offset.</span></span> |
| <span data-ttu-id="ac681-130">perspectiva</span><span class="sxs-lookup"><span data-stu-id="ac681-130">perspective</span></span>     | <span data-ttu-id="ac681-131">Uma sombra em perspectiva.</span><span class="sxs-lookup"><span data-stu-id="ac681-131">A perspective shadow.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="ac681-132">shapeRelative</span><span class="sxs-lookup"><span data-stu-id="ac681-132">shapeRelative</span></span>   | <span data-ttu-id="ac681-133">A sombra é criada em relação à forma.</span><span class="sxs-lookup"><span data-stu-id="ac681-133">The shadow is created relative to the shape.</span></span>                                                                                                                                                         |
| <span data-ttu-id="ac681-134">drawingRelative</span><span class="sxs-lookup"><span data-stu-id="ac681-134">drawingRelative</span></span> | <span data-ttu-id="ac681-135">A sombra é criada em relação ao desenho.</span><span class="sxs-lookup"><span data-stu-id="ac681-135">The shadow is created relative to the drawing.</span></span>                                                                                                                                                       |
| <span data-ttu-id="ac681-136">embaralha</span><span class="sxs-lookup"><span data-stu-id="ac681-136">emboss</span></span>          | <span data-ttu-id="ac681-137">A sombra tem uma aparência em relevo.</span><span class="sxs-lookup"><span data-stu-id="ac681-137">The shadow has an embossed look.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="ac681-138">**Atributo padrão da VML**</span><span class="sxs-lookup"><span data-stu-id="ac681-138">**VML Standard Attribute**</span></span>

<span data-ttu-id="ac681-139">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="ac681-139">**Example**</span></span>

<span data-ttu-id="ac681-140">Uma sombra dupla é criada com o segundo verde de sombra e deslocamento de 5 pontos para baixo e para a direita.</span><span class="sxs-lookup"><span data-stu-id="ac681-140">A double shadow is created with the second shadow green and offset 5 points down and to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 