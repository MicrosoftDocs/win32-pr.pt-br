---
title: Atributo LockRotationCenter de VML
description: Atributo LockRotationCenter de VML
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105759170"
---
# <a name="vml-lockrotationcenter-attribute"></a><span data-ttu-id="e50f5-103">Atributo LockRotationCenter de VML</span><span class="sxs-lookup"><span data-stu-id="e50f5-103">VML LockRotationCenter Attribute</span></span>

<span data-ttu-id="e50f5-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e50f5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e50f5-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="e50f5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e50f5-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="e50f5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e50f5-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="e50f5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e50f5-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e50f5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e50f5-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e50f5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e50f5-110">Determina se a rotação do objeto extrudada é especificada pelo atributo [RotationAngle](msdn-online-vml-rotationangle-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e50f5-110">Determines whether the rotation of the extruded object is specified by the [RotationAngle](msdn-online-vml-rotationangle-attribute.md) attribute.</span></span> <span data-ttu-id="e50f5-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e50f5-111">Read/write.</span></span> <span data-ttu-id="e50f5-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="e50f5-112">**VgTriState**.</span></span>

<span data-ttu-id="e50f5-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="e50f5-113">**Applies To**</span></span>

[<span data-ttu-id="e50f5-114">Extrusão</span><span class="sxs-lookup"><span data-stu-id="e50f5-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="e50f5-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="e50f5-115">**Tag Syntax**</span></span>

<span data-ttu-id="e50f5-116"><o: *Element* lockrotationcenter = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="e50f5-116"><o: *element* lockrotationcenter=" *expression* "></span></span>

<span data-ttu-id="e50f5-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="e50f5-117">**Script Syntax**</span></span>

<span data-ttu-id="e50f5-118">*Element* . lockrotationcenter = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="e50f5-118">*element* .lockrotationcenter="*expression*"</span></span>

<span data-ttu-id="e50f5-119">*expressão* = de *elemento*. lockrotationcenter</span><span class="sxs-lookup"><span data-stu-id="e50f5-119">*expression*=*element*.lockrotationcenter</span></span>

<span data-ttu-id="e50f5-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="e50f5-120">**Remarks**</span></span>

<span data-ttu-id="e50f5-121">Se for **false**, a rotação será especificada pelo atributo [Orientation](msdn-online-vml-orientation-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e50f5-121">If **False**, the rotation is specified by the [Orientation](msdn-online-vml-orientation-attribute.md) attribute.</span></span> <span data-ttu-id="e50f5-122">O padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="e50f5-122">The default is **True**.</span></span>

<span data-ttu-id="e50f5-123">Observe que:</span><span class="sxs-lookup"><span data-stu-id="e50f5-123">Note that:</span></span>


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



<span data-ttu-id="e50f5-124">é igual a:</span><span class="sxs-lookup"><span data-stu-id="e50f5-124">is the same as:</span></span>


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



<span data-ttu-id="e50f5-125">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="e50f5-125">*Microsoft Office Extensions Attribute*</span></span>

 

 