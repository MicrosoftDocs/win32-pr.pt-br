---
title: Atributo de largura da VML
description: Atributo de largura da VML
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b3d4917d76b3c8820186b04b2e77537e6a6ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105770586"
---
# <a name="vml-width-attribute"></a><span data-ttu-id="c27da-103">Atributo de largura da VML</span><span class="sxs-lookup"><span data-stu-id="c27da-103">VML Width Attribute</span></span>

<span data-ttu-id="c27da-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c27da-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c27da-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="c27da-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c27da-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="c27da-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c27da-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="c27da-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c27da-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c27da-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c27da-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c27da-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c27da-110">Define a largura da forma.</span><span class="sxs-lookup"><span data-stu-id="c27da-110">Defines the width of the shape.</span></span> <span data-ttu-id="c27da-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c27da-111">Read/write.</span></span> <span data-ttu-id="c27da-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="c27da-112">**String**.</span></span>

<span data-ttu-id="c27da-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="c27da-113">**Applies To**</span></span>

[<span data-ttu-id="c27da-114">Forma</span><span class="sxs-lookup"><span data-stu-id="c27da-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c27da-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="c27da-115">**Tag Syntax**</span></span>

<span data-ttu-id="c27da-116"><v: *elemento* Style = "largura: *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="c27da-116"><v: *element* style="width: *expression* "></span></span>

<span data-ttu-id="c27da-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="c27da-117">**Script Syntax**</span></span>

<span data-ttu-id="c27da-118">*elemento* . Style. Width = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="c27da-118">*element* .style.width="*expression*"</span></span>

<span data-ttu-id="c27da-119">*expressão* = de *elemento*. Style. Width</span><span class="sxs-lookup"><span data-stu-id="c27da-119">*expression*=*element*.style.width</span></span>

<span data-ttu-id="c27da-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="c27da-120">**Remarks**</span></span>

<span data-ttu-id="c27da-121">O atributo de **largura** é semelhante ao atributo de **largura** HTML padrão para estilos.</span><span class="sxs-lookup"><span data-stu-id="c27da-121">The **Width** attribute is similar to the standard HTML **Width** attribute for styles.</span></span>

<span data-ttu-id="c27da-122">As unidades podem ser mapeadas para o elemento pai ou podem estar em unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="c27da-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="c27da-123">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="c27da-123">Values include:</span></span>



| <span data-ttu-id="c27da-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c27da-124">Value</span></span>      | <span data-ttu-id="c27da-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="c27da-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c27da-126">Automático</span><span class="sxs-lookup"><span data-stu-id="c27da-126">Auto</span></span>       | <span data-ttu-id="c27da-127">Posição padrão de um elemento no fluxo da página.</span><span class="sxs-lookup"><span data-stu-id="c27da-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="c27da-128">units</span><span class="sxs-lookup"><span data-stu-id="c27da-128">units</span></span>      | <span data-ttu-id="c27da-129">Um número com um designador de unidades absolutas (cm, mm, em, pt, PC ou px) ou um designador de unidades relativas (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="c27da-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="c27da-130">Se nenhuma unidade for fornecida, serão assumidos pixels (px).</span><span class="sxs-lookup"><span data-stu-id="c27da-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="c27da-131">percentage</span><span class="sxs-lookup"><span data-stu-id="c27da-131">percentage</span></span> | <span data-ttu-id="c27da-132">Valor expresso como uma porcentagem da largura do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="c27da-132">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="c27da-133">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="c27da-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="c27da-134">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="c27da-134">**See Also**</span></span>

[<span data-ttu-id="c27da-135">Unidades</span><span class="sxs-lookup"><span data-stu-id="c27da-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="c27da-136">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="c27da-136">**Example**</span></span>

<span data-ttu-id="c27da-137">A largura da forma é 25.</span><span class="sxs-lookup"><span data-stu-id="c27da-137">The width of the shape is 25.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



<span data-ttu-id="c27da-138">[Exemplo de atributo de largura](/previous-versions/bb264101(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c27da-138">[Width Attribute Example](/previous-versions/bb264101(v=vs.85)).</span></span> <span data-ttu-id="c27da-139">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="c27da-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 