---
title: Atributo da esquerda da VML
description: Atributo da esquerda da VML
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454292"
---
# <a name="vml-left-attribute"></a><span data-ttu-id="243fb-103">Atributo da esquerda da VML</span><span class="sxs-lookup"><span data-stu-id="243fb-103">VML Left Attribute</span></span>

<span data-ttu-id="243fb-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="243fb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="243fb-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="243fb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="243fb-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="243fb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="243fb-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="243fb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="243fb-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="243fb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="243fb-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="243fb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="243fb-110">Determina a posição da forma em relação ao elemento à esquerda do fluxo de documentos.</span><span class="sxs-lookup"><span data-stu-id="243fb-110">Determines the position of the shape relative to the element left of it in the document flow.</span></span> <span data-ttu-id="243fb-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="243fb-111">Read/write.</span></span> <span data-ttu-id="243fb-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="243fb-112">**String**.</span></span>

<span data-ttu-id="243fb-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="243fb-113">**Applies To**</span></span>

[<span data-ttu-id="243fb-114">Forma</span><span class="sxs-lookup"><span data-stu-id="243fb-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="243fb-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="243fb-115">**Tag Syntax**</span></span>

<span data-ttu-id="243fb-116"><v: *Element* estilo = "left: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="243fb-116"><v: *element* style="left: *expression* "></span></span>

<span data-ttu-id="243fb-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="243fb-117">**Script Syntax**</span></span>

<span data-ttu-id="243fb-118">*elemento* . Style. Left = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="243fb-118">*element* .style.left="*expression*"</span></span>

<span data-ttu-id="243fb-119">*expressão* = de *elemento*. Style. Left</span><span class="sxs-lookup"><span data-stu-id="243fb-119">*expression*=*element*.style.left</span></span>

<span data-ttu-id="243fb-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="243fb-120">**Remarks**</span></span>

<span data-ttu-id="243fb-121">O atributo **Left** é semelhante ao atributo HTML **esquerdo** padrão para estilos.</span><span class="sxs-lookup"><span data-stu-id="243fb-121">The **Left** attribute is similar to the standard HTML **Left** attribute for styles.</span></span>

<span data-ttu-id="243fb-122">As unidades podem ser mapeadas para o elemento pai ou podem estar em unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="243fb-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="243fb-123">Este atributo não será gravado para formas ancoradas em linhas.</span><span class="sxs-lookup"><span data-stu-id="243fb-123">This attribute will not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="243fb-124">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="243fb-124">Values include:</span></span>



| <span data-ttu-id="243fb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="243fb-125">Value</span></span>      | <span data-ttu-id="243fb-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="243fb-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="243fb-127">Automático</span><span class="sxs-lookup"><span data-stu-id="243fb-127">Auto</span></span>       | <span data-ttu-id="243fb-128">Posição padrão de um elemento no fluxo da página.</span><span class="sxs-lookup"><span data-stu-id="243fb-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="243fb-129">units</span><span class="sxs-lookup"><span data-stu-id="243fb-129">units</span></span>      | <span data-ttu-id="243fb-130">Um número com um designador de unidades absolutas (cm, mm, em, pt, PC ou px) ou um designador de unidades relativas (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="243fb-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="243fb-131">Se nenhuma unidade for fornecida, serão assumidos pixels (px).</span><span class="sxs-lookup"><span data-stu-id="243fb-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="243fb-132">percentage</span><span class="sxs-lookup"><span data-stu-id="243fb-132">percentage</span></span> | <span data-ttu-id="243fb-133">Valor expresso como uma porcentagem da largura do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="243fb-133">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="243fb-134">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="243fb-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="243fb-135">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="243fb-135">**See Also**</span></span>

[<span data-ttu-id="243fb-136">Unidades</span><span class="sxs-lookup"><span data-stu-id="243fb-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="243fb-137">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="243fb-137">**Example**</span></span>

<span data-ttu-id="243fb-138">O valor esquerdo da forma é definido como 1 no exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="243fb-138">The left value of the shape is set to 1 in the example below.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="243fb-139">[Exemplo de atributo Left](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span><span class="sxs-lookup"><span data-stu-id="243fb-139">[Left Attribute Example](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span></span> <span data-ttu-id="243fb-140">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="243fb-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 