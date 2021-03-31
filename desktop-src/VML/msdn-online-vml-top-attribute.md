---
title: Atributo superior da VML
description: Atributo superior da VML
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c76a39035bc3dd3f0ae348280561e614d7dab4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641335"
---
# <a name="vml-top-attribute"></a><span data-ttu-id="d5dc3-103">Atributo superior da VML</span><span class="sxs-lookup"><span data-stu-id="d5dc3-103">VML Top Attribute</span></span>

<span data-ttu-id="d5dc3-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d5dc3-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d5dc3-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d5dc3-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d5dc3-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d5dc3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d5dc3-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d5dc3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d5dc3-110">Define a posição da forma em relação ao elemento acima dele no fluxo da página.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-110">Defines the position of the shape relative to the element above it in the flow of the page.</span></span> <span data-ttu-id="d5dc3-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-111">Read/write.</span></span> <span data-ttu-id="d5dc3-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-112">**String**.</span></span>

<span data-ttu-id="d5dc3-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="d5dc3-113">**Applies To**</span></span>

[<span data-ttu-id="d5dc3-114">Forma</span><span class="sxs-lookup"><span data-stu-id="d5dc3-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d5dc3-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="d5dc3-115">**Tag Syntax**</span></span>

<span data-ttu-id="d5dc3-116"><v: *Element* Style = "Top: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d5dc3-116"><v: *element* style="top: *expression* "></span></span>

<span data-ttu-id="d5dc3-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="d5dc3-117">**Script Syntax**</span></span>

<span data-ttu-id="d5dc3-118">*Element* . Style.Top = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="d5dc3-118">*element* .style.top="*expression*"</span></span>

<span data-ttu-id="d5dc3-119">*expressão* = de *elemento*. Style.Top</span><span class="sxs-lookup"><span data-stu-id="d5dc3-119">*expression*=*element*.style.top</span></span>

<span data-ttu-id="d5dc3-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="d5dc3-120">**Remarks**</span></span>

<span data-ttu-id="d5dc3-121">O atributo **Top** é semelhante ao atributo HTML **Top** padrão para estilos.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-121">The **Top** attribute is similar to the standard HTML **Top** attribute for styles.</span></span>

<span data-ttu-id="d5dc3-122">As unidades podem ser mapeadas para o elemento pai ou podem estar em unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="d5dc3-123">Este atributo não pode ser gravado para formas ancoradas em linhas.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-123">This attribute may not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="d5dc3-124">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="d5dc3-124">Values include:</span></span>



| <span data-ttu-id="d5dc3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d5dc3-125">Value</span></span>      | <span data-ttu-id="d5dc3-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5dc3-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5dc3-127">Automático</span><span class="sxs-lookup"><span data-stu-id="d5dc3-127">Auto</span></span>       | <span data-ttu-id="d5dc3-128">Posição padrão de um elemento no fluxo da página.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="d5dc3-129">units</span><span class="sxs-lookup"><span data-stu-id="d5dc3-129">units</span></span>      | <span data-ttu-id="d5dc3-130">Um número com um designador de unidades absolutas (cm, mm, em, pt, PC ou px) ou um designador de unidades relativas (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="d5dc3-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="d5dc3-131">Se nenhuma unidade for fornecida, serão assumidos pixels (px).</span><span class="sxs-lookup"><span data-stu-id="d5dc3-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="d5dc3-132">percentage</span><span class="sxs-lookup"><span data-stu-id="d5dc3-132">percentage</span></span> | <span data-ttu-id="d5dc3-133">Valor expresso como uma porcentagem da altura do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-133">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="d5dc3-134">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="d5dc3-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="d5dc3-135">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="d5dc3-135">**See Also**</span></span>

[<span data-ttu-id="d5dc3-136">Unidades</span><span class="sxs-lookup"><span data-stu-id="d5dc3-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="d5dc3-137">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="d5dc3-137">**Example**</span></span>

<span data-ttu-id="d5dc3-138">A borda superior da forma é de 5 pixels abaixo do objeto que a precede no fluxo da página.</span><span class="sxs-lookup"><span data-stu-id="d5dc3-138">The top edge of the shape is 5 pixels below the object that precedes it in the flow of the page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="d5dc3-139">[Exemplo de atributo Top](/previous-versions/bb264098(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d5dc3-139">[Top Attribute Example](/previous-versions/bb264098(v=vs.85)).</span></span> <span data-ttu-id="d5dc3-140">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="d5dc3-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 