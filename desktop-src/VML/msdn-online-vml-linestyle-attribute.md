---
title: Atributo LineStyle da VML
description: Atributo LineStyle da VML
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e69371e61a3d81f97de0243af19381f36c0555
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641131"
---
# <a name="vml-linestyle-attribute"></a><span data-ttu-id="4ce52-103">Atributo LineStyle da VML</span><span class="sxs-lookup"><span data-stu-id="4ce52-103">VML LineStyle Attribute</span></span>

<span data-ttu-id="4ce52-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4ce52-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4ce52-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="4ce52-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4ce52-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="4ce52-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4ce52-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="4ce52-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4ce52-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4ce52-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4ce52-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4ce52-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4ce52-110">Define o estilo de linha do traço.</span><span class="sxs-lookup"><span data-stu-id="4ce52-110">Defines the line style of the stroke.</span></span> <span data-ttu-id="4ce52-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4ce52-111">Read/write.</span></span> <span data-ttu-id="4ce52-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-112">**String**.</span></span>

<span data-ttu-id="4ce52-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="4ce52-113">**Applies To**</span></span>

[<span data-ttu-id="4ce52-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="4ce52-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="4ce52-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="4ce52-115">**Tag Syntax**</span></span>

<span data-ttu-id="4ce52-116"><v: *elemento* LineStyle = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="4ce52-116"><v: *element* linestyle=" *expression* "></span></span>

<span data-ttu-id="4ce52-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="4ce52-117">**Script Syntax**</span></span>

<span data-ttu-id="4ce52-118">*elemento* . LineStyle = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="4ce52-118">*element* .linestyle="*expression*"</span></span>

<span data-ttu-id="4ce52-119">*expressão* = de *elemento*. LineStyle</span><span class="sxs-lookup"><span data-stu-id="4ce52-119">*expression*=*element*.linestyle</span></span>

<span data-ttu-id="4ce52-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="4ce52-120">**Remarks**</span></span>

<span data-ttu-id="4ce52-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="4ce52-121">Values include:</span></span>

-   <span data-ttu-id="4ce52-122">Único (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ce52-122">Single (default)</span></span>
-   <span data-ttu-id="4ce52-123">ThinThin</span><span class="sxs-lookup"><span data-stu-id="4ce52-123">ThinThin</span></span>
-   <span data-ttu-id="4ce52-124">ThinThick</span><span class="sxs-lookup"><span data-stu-id="4ce52-124">ThinThick</span></span>
-   <span data-ttu-id="4ce52-125">ThickThin</span><span class="sxs-lookup"><span data-stu-id="4ce52-125">ThickThin</span></span>
-   <span data-ttu-id="4ce52-126">ThickBetweenThin</span><span class="sxs-lookup"><span data-stu-id="4ce52-126">ThickBetweenThin</span></span>

<span data-ttu-id="4ce52-127">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="4ce52-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="4ce52-128">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="4ce52-128">**Example**</span></span>

<span data-ttu-id="4ce52-129">Uma linha dupla é desenhada com dois traços finos.</span><span class="sxs-lookup"><span data-stu-id="4ce52-129">A double line is drawn with two thin strokes.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 