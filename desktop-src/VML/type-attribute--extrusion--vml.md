---
title: Atributo de tipo (extrusão) (VML)
description: Atributo de tipo (extrusão) (VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823872"
---
# <a name="type-attribute-extrusionvml"></a><span data-ttu-id="c4406-103">Atributo de tipo (extrusão) (VML)</span><span class="sxs-lookup"><span data-stu-id="c4406-103">Type Attribute (Extrusion)(VML)</span></span>

<span data-ttu-id="c4406-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c4406-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c4406-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="c4406-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c4406-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="c4406-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c4406-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="c4406-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c4406-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c4406-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c4406-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c4406-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c4406-110">Define a maneira como a forma é extrudada.</span><span class="sxs-lookup"><span data-stu-id="c4406-110">Defines the way that the shape is extruded.</span></span> <span data-ttu-id="c4406-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c4406-111">Read/write.</span></span> <span data-ttu-id="c4406-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="c4406-112">**String**.</span></span>

<span data-ttu-id="c4406-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="c4406-113">**Applies To**</span></span>

[<span data-ttu-id="c4406-114">Extrusão</span><span class="sxs-lookup"><span data-stu-id="c4406-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="c4406-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="c4406-115">**Tag Syntax**</span></span>

<span data-ttu-id="c4406-116"><o: tipo de *elemento* = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="c4406-116"><o: *element* type=" *expression* "></span></span>

<span data-ttu-id="c4406-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="c4406-117">**Script Syntax**</span></span>

<span data-ttu-id="c4406-118">*elemento* . Type = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="c4406-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="c4406-119">*expressão* = de *elemento*. Type</span><span class="sxs-lookup"><span data-stu-id="c4406-119">*expression*=*element*.type</span></span>

<span data-ttu-id="c4406-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="c4406-120">**Remarks**</span></span>

<span data-ttu-id="c4406-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="c4406-121">Values include:</span></span>



| <span data-ttu-id="c4406-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c4406-122">Value</span></span>       | <span data-ttu-id="c4406-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4406-123">Description</span></span>                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4406-124">parallel</span><span class="sxs-lookup"><span data-stu-id="c4406-124">parallel</span></span>    | <span data-ttu-id="c4406-125">A extrusão é renderizada para que o centro da projeção esteja infinitamente distante; ou seja, as linhas de extrusão não convergem (ao contrário das projeções de perspectiva).</span><span class="sxs-lookup"><span data-stu-id="c4406-125">Extrusion is rendered so that the center of projection is infinitely far away; that is, the extrusion lines do not converge (unlike perspective projections).</span></span> <span data-ttu-id="c4406-126">Padrão.</span><span class="sxs-lookup"><span data-stu-id="c4406-126">Default.</span></span> |
| <span data-ttu-id="c4406-127">perspectiva</span><span class="sxs-lookup"><span data-stu-id="c4406-127">perspective</span></span> | <span data-ttu-id="c4406-128">A extrusão é renderizada em um centro de projeção, que é o mesmo que o ponto de fuga para objetos não girados.</span><span class="sxs-lookup"><span data-stu-id="c4406-128">Extrusion is rendered to a center of projection, which is the same as the vanishing point for unrotated objects.</span></span>                                                       |



 

<span data-ttu-id="c4406-129">**Atributo de extensões de Microsoft Office**</span><span class="sxs-lookup"><span data-stu-id="c4406-129">**Microsoft Office Extensions Attribute**</span></span>

 

 