---
title: Atributo ImageAspect de VML
description: Atributo ImageAspect de VML
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294220"
---
# <a name="vml-imageaspect-attribute"></a><span data-ttu-id="dc05a-103">Atributo ImageAspect de VML</span><span class="sxs-lookup"><span data-stu-id="dc05a-103">VML ImageAspect Attribute</span></span>

<span data-ttu-id="dc05a-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="dc05a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dc05a-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="dc05a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dc05a-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="dc05a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dc05a-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="dc05a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dc05a-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="dc05a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dc05a-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="dc05a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dc05a-110">Define como a taxa de proporção da imagem de traço será preservada.</span><span class="sxs-lookup"><span data-stu-id="dc05a-110">Defines how the stroke image aspect ratio will be preserved.</span></span> <span data-ttu-id="dc05a-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="dc05a-111">Read/write.</span></span> <span data-ttu-id="dc05a-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="dc05a-112">**String**.</span></span>

<span data-ttu-id="dc05a-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="dc05a-113">**Applies To**</span></span>

[<span data-ttu-id="dc05a-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="dc05a-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="dc05a-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="dc05a-115">**Tag Syntax**</span></span>

<span data-ttu-id="dc05a-116"><v:</span><span class="sxs-lookup"><span data-stu-id="dc05a-116"><v:</span></span>

<span data-ttu-id="dc05a-117">elemento *imageaspect = "* expression *" >*</span><span class="sxs-lookup"><span data-stu-id="dc05a-117">element *imageaspect="* expression *">*</span></span>

<span data-ttu-id="dc05a-118">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="dc05a-118">**Script Syntax**</span></span>

<span data-ttu-id="dc05a-119">element *. imageaspect = "* expressão *"*</span><span class="sxs-lookup"><span data-stu-id="dc05a-119">element *.imageaspect="* expression *"*</span></span>

<span data-ttu-id="dc05a-120">elemento de expressão *=* *. imageaspect*</span><span class="sxs-lookup"><span data-stu-id="dc05a-120">expression *=* element *.imageaspect*</span></span>

<span data-ttu-id="dc05a-121">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="dc05a-121">**Remarks**</span></span>

<span data-ttu-id="dc05a-122">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="dc05a-122">Values include:</span></span>



| <span data-ttu-id="dc05a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dc05a-123">Value</span></span>   | <span data-ttu-id="dc05a-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc05a-124">Description</span></span>                                |
|---------|--------------------------------------------|
| <span data-ttu-id="dc05a-125">Ignorar</span><span class="sxs-lookup"><span data-stu-id="dc05a-125">Ignore</span></span>  | <span data-ttu-id="dc05a-126">Ignorar problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="dc05a-126">Ignore aspect issues.</span></span>                      |
| <span data-ttu-id="dc05a-127">Mínimo</span><span class="sxs-lookup"><span data-stu-id="dc05a-127">AtLeast</span></span> | <span data-ttu-id="dc05a-128">A imagem é pelo menos tão grande quanto **ImageSize**.</span><span class="sxs-lookup"><span data-stu-id="dc05a-128">Image is at least as big as **ImageSize**.</span></span> |
| <span data-ttu-id="dc05a-129">AtMost</span><span class="sxs-lookup"><span data-stu-id="dc05a-129">AtMost</span></span>  | <span data-ttu-id="dc05a-130">A imagem não é maior que **ImageSize**.</span><span class="sxs-lookup"><span data-stu-id="dc05a-130">Image is no bigger than **ImageSize**.</span></span>     |



 

<span data-ttu-id="dc05a-131">Em cada caso, o atributo **ImageSize** será ajustado para preservar o aspecto da imagem.</span><span class="sxs-lookup"><span data-stu-id="dc05a-131">In each case, the **ImageSize** attribute will be adjusted to preserve the aspect of the image.</span></span>

<span data-ttu-id="dc05a-132">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="dc05a-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="dc05a-133">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="dc05a-133">**Example**</span></span>

<span data-ttu-id="dc05a-134">A imagem de traço será pelo menos tão grande quanto o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="dc05a-134">The stroke image will be at least as big as the image size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 