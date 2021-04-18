---
title: Atributo FillColor da VML
description: Atributo FillColor da VML
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbacd688d25745222b5dcaf62691bff8546dad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105788854"
---
# <a name="vml-fillcolor-attribute"></a><span data-ttu-id="8dc93-103">Atributo FillColor da VML</span><span class="sxs-lookup"><span data-stu-id="8dc93-103">VML FillColor Attribute</span></span>

<span data-ttu-id="8dc93-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8dc93-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8dc93-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="8dc93-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8dc93-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="8dc93-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8dc93-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="8dc93-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8dc93-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8dc93-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8dc93-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8dc93-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8dc93-110">Define a cor do pincel que preenche o caminho fechado de uma forma.</span><span class="sxs-lookup"><span data-stu-id="8dc93-110">Defines the brush color that fills the closed path of a shape.</span></span> <span data-ttu-id="8dc93-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8dc93-111">Read/write.</span></span> <span data-ttu-id="8dc93-112">[IVgColor](msdn-online-vml-ivgcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="8dc93-112">[IVgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="8dc93-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="8dc93-113">**Applies To**</span></span>

[<span data-ttu-id="8dc93-114">Forma</span><span class="sxs-lookup"><span data-stu-id="8dc93-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="8dc93-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="8dc93-115">**Tag Syntax**</span></span>

<span data-ttu-id="8dc93-116"><v: *Element* FillColor = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="8dc93-116"><v: *element* fillcolor=" *expression* "></span></span>

<span data-ttu-id="8dc93-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="8dc93-117">**Script Syntax**</span></span>

<span data-ttu-id="8dc93-118">*Element* . FillColor = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="8dc93-118">*element* .fillcolor="*expression*"</span></span>

<span data-ttu-id="8dc93-119">*expressão* = de *Element*. FillColor</span><span class="sxs-lookup"><span data-stu-id="8dc93-119">*expression*=*element*.fillcolor</span></span>

<span data-ttu-id="8dc93-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="8dc93-120">**Remarks**</span></span>

<span data-ttu-id="8dc93-121">O valor **FillColor** é duplicado do atributo **Color** do elemento **Fill** .</span><span class="sxs-lookup"><span data-stu-id="8dc93-121">The **FillColor** value is duplicated from the **Color** attribute of the **Fill** element.</span></span>

<span data-ttu-id="8dc93-122">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="8dc93-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="8dc93-123">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="8dc93-123">**See Also**</span></span>

<span data-ttu-id="8dc93-124">[Forma](shape-element--vml.md), [preenchimento](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="8dc93-124">[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)</span></span>

<span data-ttu-id="8dc93-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="8dc93-125">**Example**</span></span>

<span data-ttu-id="8dc93-126">A cor de preenchimento do retângulo é vermelha.</span><span class="sxs-lookup"><span data-stu-id="8dc93-126">The fill color of the rectangle is red.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="8dc93-127">[Exemplo do atributo FillColor](/previous-versions/bb229668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8dc93-127">[FillColor Attribute Example](/previous-versions/bb229668(v=vs.85)).</span></span> <span data-ttu-id="8dc93-128">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="8dc93-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 