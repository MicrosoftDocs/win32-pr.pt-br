---
title: Atributo Margin-Right de VML
description: Atributo Margin-Right de VML
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5529257a0e21c8a8f8c7a1a2f8381c10a6e3b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008340"
---
# <a name="vml-margin-right-attribute"></a><span data-ttu-id="a73d4-103">Atributo Margin-Right de VML</span><span class="sxs-lookup"><span data-stu-id="a73d4-103">VML Margin-Right Attribute</span></span>

<span data-ttu-id="a73d4-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a73d4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a73d4-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="a73d4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a73d4-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="a73d4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a73d4-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="a73d4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a73d4-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a73d4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a73d4-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a73d4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a73d4-110">Especifica a borda direita da forma que contém o retângulo em relação à âncora de forma.</span><span class="sxs-lookup"><span data-stu-id="a73d4-110">Specifies the right edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="a73d4-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a73d4-111">Read/write.</span></span> <span data-ttu-id="a73d4-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="a73d4-112">**String**.</span></span>

<span data-ttu-id="a73d4-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="a73d4-113">**Applies To**</span></span>

[<span data-ttu-id="a73d4-114">Forma</span><span class="sxs-lookup"><span data-stu-id="a73d4-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a73d4-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="a73d4-115">**Tag Syntax**</span></span>

<span data-ttu-id="a73d4-116"><v: *Element* Style = "margin-right: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a73d4-116"><v: *element* style="margin-right: *expression* "></span></span>

<span data-ttu-id="a73d4-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="a73d4-117">**Script Syntax**</span></span>

<span data-ttu-id="a73d4-118">*elemento* . Style. marginright = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="a73d4-118">*element* .style.marginright="*expression*"</span></span>

<span data-ttu-id="a73d4-119">*expressão* = de *elemento*. Style. marginright</span><span class="sxs-lookup"><span data-stu-id="a73d4-119">*expression*=*element*.style.marginright</span></span>

<span data-ttu-id="a73d4-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="a73d4-120">**Remarks**</span></span>

<span data-ttu-id="a73d4-121">O atributo **margin-right** é semelhante ao atributo de margem HTML padrão **-direito** usado com folhas de estilo.</span><span class="sxs-lookup"><span data-stu-id="a73d4-121">The **Margin-Right** attribute is similar to the standard HTML **Margin-Right** attribute used with style sheets.</span></span>

<span data-ttu-id="a73d4-122">Observe que **marginright** é usado em vez de **margin-right** para scripts.</span><span class="sxs-lookup"><span data-stu-id="a73d4-122">Note that **marginright** is used instead of **margin-right** for scripting.</span></span> <span data-ttu-id="a73d4-123">Observe também que, se a **posição** for **absoluta**, a margem não parecerá ser alterada.</span><span class="sxs-lookup"><span data-stu-id="a73d4-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="a73d4-124">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="a73d4-124">Values include:</span></span>



| <span data-ttu-id="a73d4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a73d4-125">Value</span></span>      | <span data-ttu-id="a73d4-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="a73d4-126">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a73d4-127">Automático</span><span class="sxs-lookup"><span data-stu-id="a73d4-127">Auto</span></span>       | <span data-ttu-id="a73d4-128">Posição padrão de um elemento no fluxo da página.</span><span class="sxs-lookup"><span data-stu-id="a73d4-128">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="a73d4-129">units</span><span class="sxs-lookup"><span data-stu-id="a73d4-129">units</span></span>      | <span data-ttu-id="a73d4-130">Padrão.</span><span class="sxs-lookup"><span data-stu-id="a73d4-130">Default.</span></span> <span data-ttu-id="a73d4-131">Um número com um designador de unidades absolutas (cm, mm, em, pt, PC ou px) ou um designador de unidades relativas (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="a73d4-131">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="a73d4-132">Se nenhuma unidade for fornecida, serão assumidos pixels (px).</span><span class="sxs-lookup"><span data-stu-id="a73d4-132">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="a73d4-133">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a73d4-133">The default value is 0.</span></span> |
| <span data-ttu-id="a73d4-134">percentage</span><span class="sxs-lookup"><span data-stu-id="a73d4-134">percentage</span></span> | <span data-ttu-id="a73d4-135">Valor expresso como uma porcentagem da altura do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="a73d4-135">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="a73d4-136">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="a73d4-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="a73d4-137">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="a73d4-137">**See Also**</span></span>

[<span data-ttu-id="a73d4-138">Unidades</span><span class="sxs-lookup"><span data-stu-id="a73d4-138">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="a73d4-139">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a73d4-139">**Example**</span></span>

<span data-ttu-id="a73d4-140">A margem direita é definida como 25 pixels.</span><span class="sxs-lookup"><span data-stu-id="a73d4-140">The right margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



<span data-ttu-id="a73d4-141">[Exemplo do atributo margin-right](/previous-versions/bb229677(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a73d4-141">[Margin-Right Attribute Example](/previous-versions/bb229677(v=vs.85)).</span></span> <span data-ttu-id="a73d4-142">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="a73d4-142">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 