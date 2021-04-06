---
title: Atributo VML Z-index
description: Atributo VML Z-index
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917369"
---
# <a name="vml-z-index-attribute"></a><span data-ttu-id="054a9-103">Atributo VML Z-index</span><span class="sxs-lookup"><span data-stu-id="054a9-103">VML Z-Index Attribute</span></span>

<span data-ttu-id="054a9-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="054a9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="054a9-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="054a9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="054a9-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="054a9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="054a9-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="054a9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="054a9-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="054a9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="054a9-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="054a9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="054a9-110">Determina a ordem de exibição de formas sobrepostas.</span><span class="sxs-lookup"><span data-stu-id="054a9-110">Determines the display order of overlapping shapes.</span></span> <span data-ttu-id="054a9-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="054a9-111">Read/write.</span></span> <span data-ttu-id="054a9-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="054a9-112">**String**.</span></span>

<span data-ttu-id="054a9-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="054a9-113">**Applies To**</span></span>

[<span data-ttu-id="054a9-114">Forma</span><span class="sxs-lookup"><span data-stu-id="054a9-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="054a9-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="054a9-115">**Tag Syntax**</span></span>

<span data-ttu-id="054a9-116"><v: *elemento* Style = "z-index: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="054a9-116"><v: *element* style="z-index: *expression* "></span></span>

<span data-ttu-id="054a9-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="054a9-117">**Script Syntax**</span></span>

<span data-ttu-id="054a9-118">*elemento* . Style. ZIndex = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="054a9-118">*element* .style.zindex="*expression*"</span></span>

<span data-ttu-id="054a9-119">*expressão* = de *elemento*. Style. ZIndex</span><span class="sxs-lookup"><span data-stu-id="054a9-119">*expression*=*element*.style.zindex</span></span>

<span data-ttu-id="054a9-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="054a9-120">**Remarks**</span></span>

<span data-ttu-id="054a9-121">O atributo **z-index** é semelhante ao atributo HTML **z-index** padrão para estilos.</span><span class="sxs-lookup"><span data-stu-id="054a9-121">The **Z-Index** attribute is similar to the standard HTML **Z-Index** attribute for styles.</span></span>

<span data-ttu-id="054a9-122">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="054a9-122">Values include:</span></span>



| <span data-ttu-id="054a9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="054a9-123">Value</span></span> | <span data-ttu-id="054a9-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="054a9-124">Description</span></span>                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="054a9-125">Automático</span><span class="sxs-lookup"><span data-stu-id="054a9-125">Auto</span></span>  | <span data-ttu-id="054a9-126">A ordem em que as formas aparecem na página HTML será usada, de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="054a9-126">The order that the shapes appear in the HTML page will be used, bottom to top.</span></span>                                                                                                                         |
| <span data-ttu-id="054a9-127">ordem</span><span class="sxs-lookup"><span data-stu-id="054a9-127">order</span></span> | <span data-ttu-id="054a9-128">Um número que representa a precedência de empilhamento.</span><span class="sxs-lookup"><span data-stu-id="054a9-128">A number that represents the stacking precedence.</span></span> <span data-ttu-id="054a9-129">Uma forma com um número mais alto será exibida como se wereoverlapping (em "frente" de) uma forma com um número mais baixo.</span><span class="sxs-lookup"><span data-stu-id="054a9-129">A shape with a a higher number will be displayed as if it wereoverlapping (in "front" of) a shape with a lower number.</span></span> <span data-ttu-id="054a9-130">Números negativos podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="054a9-130">Negative numbers can be used.</span></span> |



 

<span data-ttu-id="054a9-131">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="054a9-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="054a9-132">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="054a9-132">**Example**</span></span>

<span data-ttu-id="054a9-133">A forma vermelha será exibida em "frente" da forma azul, pois ela tem um índice z superior.</span><span class="sxs-lookup"><span data-stu-id="054a9-133">The red shape will be displayed in "front" of the blue shape, because it has a higher z-index.</span></span>


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



<span data-ttu-id="054a9-134">[Exemplo de atributo Z-index](/previous-versions/ms530275(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="054a9-134">[Z-Index Attribute Example](/previous-versions/ms530275(v=vs.85)).</span></span> <span data-ttu-id="054a9-135">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="054a9-135">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 