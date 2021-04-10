---
title: Atributo de altura da VML
description: Atributo de altura da VML
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41751e4863fdb128dbbedf2e3abf8e7f0a6736d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084643"
---
# <a name="vml-height-attribute"></a><span data-ttu-id="3ffad-103">Atributo de altura da VML</span><span class="sxs-lookup"><span data-stu-id="3ffad-103">VML Height Attribute</span></span>

<span data-ttu-id="3ffad-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3ffad-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3ffad-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="3ffad-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3ffad-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="3ffad-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3ffad-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="3ffad-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3ffad-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3ffad-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3ffad-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3ffad-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3ffad-110">Especifica a altura da forma.</span><span class="sxs-lookup"><span data-stu-id="3ffad-110">Specifies the height of the shape.</span></span> <span data-ttu-id="3ffad-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3ffad-111">Read/write.</span></span> <span data-ttu-id="3ffad-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="3ffad-112">**String**.</span></span>

<span data-ttu-id="3ffad-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="3ffad-113">**Applies To**</span></span>

[<span data-ttu-id="3ffad-114">Forma</span><span class="sxs-lookup"><span data-stu-id="3ffad-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3ffad-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="3ffad-115">**Tag Syntax**</span></span>

<span data-ttu-id="3ffad-116"><v: *elemento* Style = "altura: *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="3ffad-116"><v: *element* style="height: *expression* "></span></span>

<span data-ttu-id="3ffad-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="3ffad-117">**Script Syntax**</span></span>

<span data-ttu-id="3ffad-118">*elemento* . Style. Height = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="3ffad-118">*element* .style.height="*expression*"</span></span>

<span data-ttu-id="3ffad-119">*expressão* = de *elemento*. Style. Height</span><span class="sxs-lookup"><span data-stu-id="3ffad-119">*expression*=*element*.style.height</span></span>

<span data-ttu-id="3ffad-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="3ffad-120">**Remarks**</span></span>

<span data-ttu-id="3ffad-121">O atributo de **altura** é semelhante ao atributo de **altura** padrão de HTML para estilos.</span><span class="sxs-lookup"><span data-stu-id="3ffad-121">The **Height** attribute is similar to the standard HTML **Height** attribute for styles.</span></span>

<span data-ttu-id="3ffad-122">As unidades podem ser mapeadas para o elemento pai ou podem estar em unidades absolutas.</span><span class="sxs-lookup"><span data-stu-id="3ffad-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="3ffad-123">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="3ffad-123">Values include:</span></span>



| <span data-ttu-id="3ffad-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffad-124">Value</span></span>      | <span data-ttu-id="3ffad-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ffad-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ffad-126">Automático</span><span class="sxs-lookup"><span data-stu-id="3ffad-126">Auto</span></span>       | <span data-ttu-id="3ffad-127">Posição padrão de um elemento no fluxo da página.</span><span class="sxs-lookup"><span data-stu-id="3ffad-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="3ffad-128">units</span><span class="sxs-lookup"><span data-stu-id="3ffad-128">units</span></span>      | <span data-ttu-id="3ffad-129">Um número com um designador de unidades absolutas (cm, mm, em, pt, PC ou px) ou um designador de unidades relativas (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="3ffad-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="3ffad-130">Se nenhuma unidade for fornecida, serão assumidos pixels (px).</span><span class="sxs-lookup"><span data-stu-id="3ffad-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="3ffad-131">percentage</span><span class="sxs-lookup"><span data-stu-id="3ffad-131">percentage</span></span> | <span data-ttu-id="3ffad-132">Valor expresso como uma porcentagem da altura do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="3ffad-132">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="3ffad-133">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="3ffad-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="3ffad-134">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="3ffad-134">**See Also**</span></span>

[<span data-ttu-id="3ffad-135">Unidades</span><span class="sxs-lookup"><span data-stu-id="3ffad-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="3ffad-136">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="3ffad-136">**Example**</span></span>

<span data-ttu-id="3ffad-137">A altura da forma é definida como 30.</span><span class="sxs-lookup"><span data-stu-id="3ffad-137">The height of the shape is set to 30.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



<span data-ttu-id="3ffad-138">[Exemplo de atributo Height](/previous-versions/bb229671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ffad-138">[Height Attribute Example](/previous-versions/bb229671(v=vs.85)).</span></span> <span data-ttu-id="3ffad-139">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="3ffad-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 