---
title: Atributo StrokeColor de VML
description: Atributo StrokeColor de VML
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007708"
---
# <a name="vml-strokecolor-attribute"></a><span data-ttu-id="80af1-103">Atributo StrokeColor de VML</span><span class="sxs-lookup"><span data-stu-id="80af1-103">VML StrokeColor Attribute</span></span>

<span data-ttu-id="80af1-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="80af1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="80af1-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="80af1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="80af1-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="80af1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="80af1-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="80af1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="80af1-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="80af1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="80af1-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="80af1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="80af1-110">Define a cor do pincel que traça o caminho de uma forma.</span><span class="sxs-lookup"><span data-stu-id="80af1-110">Defines the brush color that strokes the path of a shape.</span></span> <span data-ttu-id="80af1-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="80af1-111">Read/write.</span></span> <span data-ttu-id="80af1-112">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="80af1-112">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span>

<span data-ttu-id="80af1-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="80af1-113">**Applies To**</span></span>

[<span data-ttu-id="80af1-114">Forma</span><span class="sxs-lookup"><span data-stu-id="80af1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="80af1-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="80af1-115">**Tag Syntax**</span></span>

<span data-ttu-id="80af1-116"><v: *Element* strokecolor = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="80af1-116"><v: *element* strokecolor=" *expression* "></span></span>

<span data-ttu-id="80af1-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="80af1-117">**Script Syntax**</span></span>

<span data-ttu-id="80af1-118">*Element* . strokecolor = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="80af1-118">*element* .strokecolor="*expression*"</span></span>

<span data-ttu-id="80af1-119">*expressão* = de *elemento*. strokecolor</span><span class="sxs-lookup"><span data-stu-id="80af1-119">*expression*=*element*.strokecolor</span></span>

<span data-ttu-id="80af1-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="80af1-120">**Remarks**</span></span>

<span data-ttu-id="80af1-121">O valor é duplicado do atributo **Color** do elemento [Stroke](msdn-online-vml-stroke-element.md) .</span><span class="sxs-lookup"><span data-stu-id="80af1-121">The value is duplicated from the **Color** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="80af1-122">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="80af1-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="80af1-123">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="80af1-123">**Example**</span></span>

<span data-ttu-id="80af1-124">A cor do traço do retângulo é vermelha.</span><span class="sxs-lookup"><span data-stu-id="80af1-124">The color of the stroke of the rectangle is red.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="80af1-125">[Exemplo do atributo StrokeColor](/previous-versions/bb264093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80af1-125">[StrokeColor Attribute Example](/previous-versions/bb264093(v=vs.85)).</span></span> <span data-ttu-id="80af1-126">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="80af1-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 