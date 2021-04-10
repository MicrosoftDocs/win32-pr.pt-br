---
title: Atributo Margin-Top de VML
description: Atributo Margin-Top de VML
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14b6f4743f04740fe3fdbac4cc1d03f7bbe0282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294483"
---
# <a name="vml-margin-top-attribute"></a><span data-ttu-id="82850-103">Atributo Margin-Top de VML</span><span class="sxs-lookup"><span data-stu-id="82850-103">VML Margin-Top Attribute</span></span>

<span data-ttu-id="82850-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="82850-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="82850-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="82850-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="82850-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="82850-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="82850-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="82850-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="82850-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="82850-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="82850-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="82850-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="82850-110">Especifica a borda superior da forma que contém o retângulo em relação à âncora de forma.</span><span class="sxs-lookup"><span data-stu-id="82850-110">Specifies the top edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="82850-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="82850-111">Read/write.</span></span> <span data-ttu-id="82850-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="82850-112">**String**.</span></span>

<span data-ttu-id="82850-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="82850-113">**Applies To**</span></span>

[<span data-ttu-id="82850-114">Forma</span><span class="sxs-lookup"><span data-stu-id="82850-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="82850-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="82850-115">**Tag Syntax**</span></span>

<span data-ttu-id="82850-116"><v: *elemento* margin-top = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="82850-116"><v: *element* margin-top=" *expression* "></span></span>

<span data-ttu-id="82850-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="82850-117">**Script Syntax**</span></span>

<span data-ttu-id="82850-118">*elemento* . margin-top = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="82850-118">*element* .margin-top="*expression*"</span></span>

<span data-ttu-id="82850-119">*expressão* = de *elemento*. margin-top</span><span class="sxs-lookup"><span data-stu-id="82850-119">*expression*=*element*.margin-top</span></span>

<span data-ttu-id="82850-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="82850-120">**Remarks**</span></span>

<span data-ttu-id="82850-121">O atributo **margin-top** é semelhante ao atributo padrão **de margem HTML-superior** usado com folhas de estilo.</span><span class="sxs-lookup"><span data-stu-id="82850-121">The **Margin-Top** attribute is similar to the standard HTML **Margin-Top** attribute used with style sheets.</span></span>

<span data-ttu-id="82850-122">Observe que **MarginTop** é usado em vez de **margin-top** para scripts.</span><span class="sxs-lookup"><span data-stu-id="82850-122">Note that **margintop** is used instead of **margin-top** for scripting.</span></span> <span data-ttu-id="82850-123">Observe também que, se a **posição** for **absoluta**, a margem não parecerá ser alterada.</span><span class="sxs-lookup"><span data-stu-id="82850-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="82850-124">Essa propriedade é usada em vez de **Top** para formas no Microsoft Word e no Microsoft Excel que estão flutuantes em uma posição relativa a um ponto de ancoragem.</span><span class="sxs-lookup"><span data-stu-id="82850-124">This property is used instead of **Top** for shapes in Microsoft Word and Microsoft Excel that are floating in a position relative to an anchor point.</span></span>

<span data-ttu-id="82850-125">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="82850-125">Values include:</span></span>



| <span data-ttu-id="82850-126">Valor</span><span class="sxs-lookup"><span data-stu-id="82850-126">Value</span></span>      | <span data-ttu-id="82850-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="82850-127">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82850-128">Automático</span><span class="sxs-lookup"><span data-stu-id="82850-128">Auto</span></span>       | <span data-ttu-id="82850-129">Posição padrão de um elemento no fluxo da página.</span><span class="sxs-lookup"><span data-stu-id="82850-129">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="82850-130">units</span><span class="sxs-lookup"><span data-stu-id="82850-130">units</span></span>      | <span data-ttu-id="82850-131">Padrão.</span><span class="sxs-lookup"><span data-stu-id="82850-131">Default.</span></span> <span data-ttu-id="82850-132">Um número com um designador de unidades absolutas (cm, mm, em, pt, PC ou px) ou um designador de unidades relativas (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="82850-132">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="82850-133">Se nenhuma unidade for fornecida, serão assumidos pixels (px).</span><span class="sxs-lookup"><span data-stu-id="82850-133">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="82850-134">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="82850-134">The default value is 0.</span></span> |
| <span data-ttu-id="82850-135">percentage</span><span class="sxs-lookup"><span data-stu-id="82850-135">percentage</span></span> | <span data-ttu-id="82850-136">Valor expresso como uma porcentagem da altura do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="82850-136">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="82850-137">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="82850-137">*VML Standard Attribute*</span></span>

<span data-ttu-id="82850-138">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="82850-138">**See Also**</span></span>

[<span data-ttu-id="82850-139">Unidades</span><span class="sxs-lookup"><span data-stu-id="82850-139">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="82850-140">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="82850-140">**Example**</span></span>

<span data-ttu-id="82850-141">A margem superior é definida como 25 pixels.</span><span class="sxs-lookup"><span data-stu-id="82850-141">The top margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



<span data-ttu-id="82850-142">[Exemplo do atributo margin-top](/previous-versions/bb264087(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="82850-142">[Margin-Top Attribute Example](/previous-versions/bb264087(v=vs.85)).</span></span> <span data-ttu-id="82850-143">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="82850-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 