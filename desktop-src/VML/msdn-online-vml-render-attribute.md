---
title: Atributo de renderização de VML
description: Atributo de renderização de VML
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70872e823a2d43d6a605fbf07a817473b19a125a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105760800"
---
# <a name="vml-render-attribute"></a><span data-ttu-id="6507d-103">Atributo de renderização de VML</span><span class="sxs-lookup"><span data-stu-id="6507d-103">VML Render Attribute</span></span>

<span data-ttu-id="6507d-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6507d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6507d-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="6507d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6507d-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="6507d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6507d-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="6507d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6507d-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6507d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6507d-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6507d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6507d-110">Define o modo de renderização da extrusão.</span><span class="sxs-lookup"><span data-stu-id="6507d-110">Defines the rendering mode of the extrusion.</span></span> <span data-ttu-id="6507d-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6507d-111">Read/write.</span></span> <span data-ttu-id="6507d-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="6507d-112">**String**.</span></span>

<span data-ttu-id="6507d-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="6507d-113">**Applies To**</span></span>

[<span data-ttu-id="6507d-114">Extrusão</span><span class="sxs-lookup"><span data-stu-id="6507d-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="6507d-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="6507d-115">**Tag Syntax**</span></span>

<span data-ttu-id="6507d-116"><o: *elemento* render = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="6507d-116"><o: *element* render=" *expression* "></span></span>

<span data-ttu-id="6507d-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="6507d-117">**Script Syntax**</span></span>

<span data-ttu-id="6507d-118">*elemento* . render = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="6507d-118">*element* .render="*expression*"</span></span>

<span data-ttu-id="6507d-119">*expressão* = de *elemento*. render</span><span class="sxs-lookup"><span data-stu-id="6507d-119">*expression*=*element*.render</span></span>

<span data-ttu-id="6507d-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="6507d-120">**Remarks**</span></span>

<span data-ttu-id="6507d-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="6507d-121">Values include:</span></span>



| <span data-ttu-id="6507d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6507d-122">Value</span></span>        | <span data-ttu-id="6507d-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="6507d-123">Description</span></span>                                                   |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="6507d-124">consolidou</span><span class="sxs-lookup"><span data-stu-id="6507d-124">solid</span></span>        | <span data-ttu-id="6507d-125">A renderização exibe uma forma sólida.</span><span class="sxs-lookup"><span data-stu-id="6507d-125">Rendering displays a solid shape.</span></span> <span data-ttu-id="6507d-126">Padrão.</span><span class="sxs-lookup"><span data-stu-id="6507d-126">Default.</span></span>                    |
| <span data-ttu-id="6507d-127">wireframe</span><span class="sxs-lookup"><span data-stu-id="6507d-127">wireframe</span></span>    | <span data-ttu-id="6507d-128">A renderização exibe uma forma de wireframe.</span><span class="sxs-lookup"><span data-stu-id="6507d-128">Rendering displays a wireframe shape.</span></span>                         |
| <span data-ttu-id="6507d-129">boundingcube</span><span class="sxs-lookup"><span data-stu-id="6507d-129">boundingcube</span></span> | <span data-ttu-id="6507d-130">Renderização exibe o cubo delimitador que contém a forma.</span><span class="sxs-lookup"><span data-stu-id="6507d-130">Rendering displays the bounding cube that contains the shape.</span></span> |



 

<span data-ttu-id="6507d-131">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="6507d-131">*Microsoft Office Extensions Attribute*</span></span>

 

 