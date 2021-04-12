---
title: Atributo de metal de VML
description: Atributo de metal de VML
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366053"
---
# <a name="vml-metal-attribute"></a><span data-ttu-id="25b45-103">Atributo de metal de VML</span><span class="sxs-lookup"><span data-stu-id="25b45-103">VML Metal Attribute</span></span>

<span data-ttu-id="25b45-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="25b45-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="25b45-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="25b45-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="25b45-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="25b45-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="25b45-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="25b45-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="25b45-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="25b45-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="25b45-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="25b45-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="25b45-110">Determina se a superfície da forma extrudada será semelhante a um metal.</span><span class="sxs-lookup"><span data-stu-id="25b45-110">Determines whether the surface of the extruded shape will resemble metal.</span></span> <span data-ttu-id="25b45-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="25b45-111">Read/write.</span></span> <span data-ttu-id="25b45-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="25b45-112">**VgTriState**.</span></span>

<span data-ttu-id="25b45-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="25b45-113">**Applies To**</span></span>

[<span data-ttu-id="25b45-114">Extrusão</span><span class="sxs-lookup"><span data-stu-id="25b45-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="25b45-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="25b45-115">**Tag Syntax**</span></span>

<span data-ttu-id="25b45-116"><o: *elemento* metal = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="25b45-116"><o: *element* metal=" *expression* "></span></span>

<span data-ttu-id="25b45-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="25b45-117">**Script Syntax**</span></span>

<span data-ttu-id="25b45-118">*Element* . metal = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="25b45-118">*element* .metal="*expression*"</span></span>

<span data-ttu-id="25b45-119">*expressão* = de *elemento*. metal</span><span class="sxs-lookup"><span data-stu-id="25b45-119">*expression*=*element*.metal</span></span>

<span data-ttu-id="25b45-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="25b45-120">**Remarks**</span></span>

<span data-ttu-id="25b45-121">Se definido como **true**, esse atributo fará com que a luz refletida de forma especulada seja a cor do material em vez da cor da fonte de luz, tornando o objeto aparentemente mais metálico. Para aproximar ainda mais um material metálico, é necessário que a especulação seja relativamente alta (cerca de 1,2) e a didifusão seja relativamente baixa (cerca de 0,6).</span><span class="sxs-lookup"><span data-stu-id="25b45-121">If set to **True**, this attribute causes the specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.To further approximate a metallic material requires that specularity be relatively high (about 1.2) and diffusity be relatively low (about 0.6).</span></span> <span data-ttu-id="25b45-122">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="25b45-122">The default value is **False**.</span></span>

<span data-ttu-id="25b45-123">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="25b45-123">*Microsoft Office Extensions Attribute*</span></span>

 

 