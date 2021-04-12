---
title: Atributo ViewpointOrigin de VML
description: Atributo ViewpointOrigin de VML
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad256f0f5d38c6fbbfb5722e803985506efca217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454132"
---
# <a name="vml-viewpointorigin-attribute"></a><span data-ttu-id="7713d-103">Atributo ViewpointOrigin de VML</span><span class="sxs-lookup"><span data-stu-id="7713d-103">VML ViewpointOrigin Attribute</span></span>

<span data-ttu-id="7713d-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7713d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7713d-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="7713d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7713d-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="7713d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7713d-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="7713d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7713d-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7713d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7713d-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7713d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7713d-110">Define a origem do ponto de vista dentro da caixa delimitadora da forma.</span><span class="sxs-lookup"><span data-stu-id="7713d-110">Defines the origin of the viewpoint within the bounding box of the shape.</span></span> <span data-ttu-id="7713d-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7713d-111">Read/write.</span></span> <span data-ttu-id="7713d-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="7713d-112">**VgVector2D**.</span></span>

<span data-ttu-id="7713d-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="7713d-113">**Applies To**</span></span>

[<span data-ttu-id="7713d-114">Extrusão</span><span class="sxs-lookup"><span data-stu-id="7713d-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="7713d-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="7713d-115">**Tag Syntax**</span></span>

<span data-ttu-id="7713d-116"><o: *Element* viewpointorigin = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="7713d-116"><o: *element* viewpointorigin=" *expression* "></span></span>

<span data-ttu-id="7713d-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="7713d-117">**Script Syntax**</span></span>

<span data-ttu-id="7713d-118">*Element* . viewpointorigin = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="7713d-118">*element* .viewpointorigin="*expression*"</span></span>

<span data-ttu-id="7713d-119">*expressão* = de *elemento*. viewpointorigin</span><span class="sxs-lookup"><span data-stu-id="7713d-119">*expression*=*element*.viewpointorigin</span></span>

<span data-ttu-id="7713d-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="7713d-120">**Remarks**</span></span>

<span data-ttu-id="7713d-121">Define o ponto de vista em termos dos valores x e y da forma original.</span><span class="sxs-lookup"><span data-stu-id="7713d-121">Defines the viewpoint in terms of the x and y values of the original shape.</span></span> <span data-ttu-id="7713d-122">Os valores x e y variam de 0,5 a-0,5 (50% a-50% da origem da coordenada da forma).</span><span class="sxs-lookup"><span data-stu-id="7713d-122">The x and y values range from 0.5 to -0.5 (50% to -50% of the shape's coordinate origin).</span></span> <span data-ttu-id="7713d-123">O padrão é 0, 0.</span><span class="sxs-lookup"><span data-stu-id="7713d-123">The default is 0,0.</span></span>

<span data-ttu-id="7713d-124">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="7713d-124">*Microsoft Office Extensions Attribute*</span></span>

 

 