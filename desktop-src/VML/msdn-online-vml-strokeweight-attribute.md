---
title: Atributo StrokeWeight de VML
description: Atributo StrokeWeight de VML
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641292"
---
# <a name="vml-strokeweight-attribute"></a><span data-ttu-id="8114a-103">Atributo StrokeWeight de VML</span><span class="sxs-lookup"><span data-stu-id="8114a-103">VML StrokeWeight Attribute</span></span>

<span data-ttu-id="8114a-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8114a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8114a-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="8114a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8114a-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="8114a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8114a-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="8114a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8114a-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8114a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8114a-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8114a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8114a-110">Define a espessura do pincel que traça o caminho de uma forma.</span><span class="sxs-lookup"><span data-stu-id="8114a-110">Defines the brush thickness that strokes the path of a shape.</span></span> <span data-ttu-id="8114a-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8114a-111">Read/write.</span></span> <span data-ttu-id="8114a-112">**VGLength**.</span><span class="sxs-lookup"><span data-stu-id="8114a-112">**VGLength**.</span></span>

<span data-ttu-id="8114a-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="8114a-113">**Applies To**</span></span>

[<span data-ttu-id="8114a-114">Forma</span><span class="sxs-lookup"><span data-stu-id="8114a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="8114a-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="8114a-115">**Tag Syntax**</span></span>

<span data-ttu-id="8114a-116"><v: *Element* strokeweight = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="8114a-116"><v: *element* strokeweight=" *expression* "></span></span>

<span data-ttu-id="8114a-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="8114a-117">**Script Syntax**</span></span>

<span data-ttu-id="8114a-118">*Element* . strokeweight = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="8114a-118">*element* .strokeweight="*expression*"</span></span>

<span data-ttu-id="8114a-119">*expressão* = de *elemento*. strokeweight</span><span class="sxs-lookup"><span data-stu-id="8114a-119">*expression*=*element*.strokeweight</span></span>

<span data-ttu-id="8114a-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="8114a-120">**Remarks**</span></span>

<span data-ttu-id="8114a-121">O valor é duplicado do atributo **Weight** do elemento **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="8114a-121">The value is duplicated from the **Weight** attribute of the **Stroke** element.</span></span> <span data-ttu-id="8114a-122">Se um número for especificado, mas nenhuma das unidades for adicionada, a unidade de medida padrão será a emu.</span><span class="sxs-lookup"><span data-stu-id="8114a-122">If a number is specified, but no units are added, the default unit of measurement is the Emu.</span></span> <span data-ttu-id="8114a-123">Se nenhum valor for especificado, o padrão será 1 pixel (1px).</span><span class="sxs-lookup"><span data-stu-id="8114a-123">If no value is specified, the default is 1 pixel (1px).</span></span>

<span data-ttu-id="8114a-124">No entanto, para scripts, a unidade de medida padrão é em pontos.</span><span class="sxs-lookup"><span data-stu-id="8114a-124">For scripting, however, the default unit of measurement is in points.</span></span>

<span data-ttu-id="8114a-125">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="8114a-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="8114a-126">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="8114a-126">**See Also**</span></span>

<span data-ttu-id="8114a-127">[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [unidades](msdn-online-vml-units.md)</span><span class="sxs-lookup"><span data-stu-id="8114a-127">[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)</span></span>

<span data-ttu-id="8114a-128">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="8114a-128">**Example**</span></span>

<span data-ttu-id="8114a-129">O peso do traço da forma é 1 ponto.</span><span class="sxs-lookup"><span data-stu-id="8114a-129">The stroke weight of the shape is 1 point.</span></span>


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="8114a-130">[Exemplo do atributo StrokeWeight](/previous-versions/bb264095(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8114a-130">[StrokeWeight Attribute Example](/previous-versions/bb264095(v=vs.85)).</span></span> <span data-ttu-id="8114a-131">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="8114a-131">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 