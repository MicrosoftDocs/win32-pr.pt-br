---
title: Atributo de faceta de VML
description: Atributo de faceta de VML
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d4fec254ff3e6af35d82cd45146c201701555b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084645"
---
# <a name="vml-facet-attribute"></a><span data-ttu-id="44587-103">Atributo de faceta de VML</span><span class="sxs-lookup"><span data-stu-id="44587-103">VML Facet Attribute</span></span>

<span data-ttu-id="44587-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="44587-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="44587-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="44587-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="44587-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="44587-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="44587-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="44587-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="44587-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="44587-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="44587-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="44587-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="44587-110">Define o número de facetas usadas para descrever superfícies curvas de uma extrusão.</span><span class="sxs-lookup"><span data-stu-id="44587-110">Defines the number of facets used to describe curved surfaces of an extrusion.</span></span> <span data-ttu-id="44587-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="44587-111">Read/write.</span></span> <span data-ttu-id="44587-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="44587-112">**VgNumber**.</span></span>

<span data-ttu-id="44587-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="44587-113">**Applies To**</span></span>

[<span data-ttu-id="44587-114">Extrusão</span><span class="sxs-lookup"><span data-stu-id="44587-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="44587-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="44587-115">**Tag Syntax**</span></span>

<span data-ttu-id="44587-116"><o: *elemento* Facet = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="44587-116"><o: *element* facet=" *expression* "></span></span>

<span data-ttu-id="44587-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="44587-117">**Script Syntax**</span></span>

<span data-ttu-id="44587-118">*Element* . faceta = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="44587-118">*element* .facet="*expression*"</span></span>

<span data-ttu-id="44587-119">*expressão* = de *elemento*. Facet</span><span class="sxs-lookup"><span data-stu-id="44587-119">*expression*=*element*.facet</span></span>

<span data-ttu-id="44587-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="44587-120">**Remarks**</span></span>

<span data-ttu-id="44587-121">Define a maneira como um mecanismo de renderização aproximará a extrusão.</span><span class="sxs-lookup"><span data-stu-id="44587-121">Defines the way that a rendering engine will approximate the extrusion.</span></span> <span data-ttu-id="44587-122">Um número mais baixo indicará uma tolerância de renderização inferior ao mecanismo de renderização e produzirá mais facetas.</span><span class="sxs-lookup"><span data-stu-id="44587-122">A lower number will indicate a lower rendering tolerance to the rendering engine and will yield more facets.</span></span> <span data-ttu-id="44587-123">Números mais altos farão com que a extrusão pareça mais facetada.</span><span class="sxs-lookup"><span data-stu-id="44587-123">Higher numbers will make the extrusion appear more faceted.</span></span> <span data-ttu-id="44587-124">O valor padrão é 30.000.</span><span class="sxs-lookup"><span data-stu-id="44587-124">The default value is 30,000.</span></span>

<span data-ttu-id="44587-125">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="44587-125">*Microsoft Office Extensions Attribute*</span></span>

 

 