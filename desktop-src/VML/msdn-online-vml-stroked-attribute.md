---
title: Atributo de traço de VML
description: Atributo de traço de VML
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084860"
---
# <a name="vml-stroked-attribute"></a><span data-ttu-id="a9749-103">Atributo de traço de VML</span><span class="sxs-lookup"><span data-stu-id="a9749-103">VML Stroked Attribute</span></span>

<span data-ttu-id="a9749-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a9749-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a9749-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="a9749-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a9749-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="a9749-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a9749-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="a9749-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a9749-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a9749-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a9749-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a9749-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a9749-110">Define se o caminho será traçado.</span><span class="sxs-lookup"><span data-stu-id="a9749-110">Defines whether the path will be stroked.</span></span> <span data-ttu-id="a9749-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a9749-111">Read/write.</span></span> <span data-ttu-id="a9749-112">[VgTriState](msdn-online-vml-vgtristate.md) .</span><span class="sxs-lookup"><span data-stu-id="a9749-112">[VgTriState](msdn-online-vml-vgtristate.md) .</span></span>

<span data-ttu-id="a9749-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="a9749-113">**Applies To**</span></span>

[<span data-ttu-id="a9749-114">Forma</span><span class="sxs-lookup"><span data-stu-id="a9749-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a9749-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="a9749-115">**Tag Syntax**</span></span>

<span data-ttu-id="a9749-116"><v: *Element* strokeed = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a9749-116"><v: *element* stroked=" *expression* "></span></span>

<span data-ttu-id="a9749-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="a9749-117">**Script Syntax**</span></span>

<span data-ttu-id="a9749-118">*elemento* . stroked = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="a9749-118">*element* .stroked="*expression*"</span></span>

<span data-ttu-id="a9749-119">*expressão* = de *elemento*. strokeed</span><span class="sxs-lookup"><span data-stu-id="a9749-119">*expression*=*element*.stroked</span></span>

<span data-ttu-id="a9749-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="a9749-120">**Remarks**</span></span>

<span data-ttu-id="a9749-121">O valor é duplicado a partir do atributo **on** do elemento [Stroke](msdn-online-vml-stroke-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a9749-121">The value is duplicated from the **On** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="a9749-122">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="a9749-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="a9749-123">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a9749-123">**Example**</span></span>

<span data-ttu-id="a9749-124">O caminho da forma é traçado.</span><span class="sxs-lookup"><span data-stu-id="a9749-124">The shape path is stroked.</span></span>


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="a9749-125">[Exemplo de atributo strokeed](/previous-versions/bb264094(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9749-125">[Stroked Attribute Example](/previous-versions/bb264094(v=vs.85)).</span></span> <span data-ttu-id="a9749-126">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="a9749-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 