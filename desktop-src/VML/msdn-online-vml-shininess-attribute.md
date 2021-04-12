---
title: Atributo de luminosidade de VML
description: Atributo de luminosidade de VML
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a116adeb955c0f3449b374947a3f8121bd848e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294090"
---
# <a name="vml-shininess-attribute"></a><span data-ttu-id="09cba-103">Atributo de luminosidade de VML</span><span class="sxs-lookup"><span data-stu-id="09cba-103">VML Shininess Attribute</span></span>

<span data-ttu-id="09cba-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="09cba-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="09cba-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="09cba-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="09cba-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="09cba-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="09cba-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="09cba-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="09cba-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="09cba-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="09cba-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="09cba-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="09cba-110">Define a concentração da luz refletida em uma superfície de extrusão.</span><span class="sxs-lookup"><span data-stu-id="09cba-110">Defines the concentration of the reflected light on an extrusion surface.</span></span> <span data-ttu-id="09cba-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="09cba-111">Read/write.</span></span> <span data-ttu-id="09cba-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="09cba-112">**VgNumber**.</span></span>

<span data-ttu-id="09cba-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="09cba-113">**Applies To**</span></span>

[<span data-ttu-id="09cba-114">Extrusão</span><span class="sxs-lookup"><span data-stu-id="09cba-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="09cba-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="09cba-115">**Tag Syntax**</span></span>

<span data-ttu-id="09cba-116"><o: *elemento* luminosidade = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="09cba-116"><o: *element* shininess=" *expression* "></span></span>

<span data-ttu-id="09cba-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="09cba-117">**Script Syntax**</span></span>

<span data-ttu-id="09cba-118">*elemento* . luminosidade = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="09cba-118">*element* .shininess="*expression*"</span></span>

<span data-ttu-id="09cba-119">*expressão* = de *elemento*. luminosidade</span><span class="sxs-lookup"><span data-stu-id="09cba-119">*expression*=*element*.shininess</span></span>

<span data-ttu-id="09cba-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="09cba-120">**Remarks**</span></span>

<span data-ttu-id="09cba-121">Valores altos (8-10) aproximam a luminosidade de um espelho e valores baixos (2-3) aproximariam um efeito manchado.</span><span class="sxs-lookup"><span data-stu-id="09cba-121">High values (8-10) would approximate the shininess of a mirror and low values (2-3) would approximate a speckled effect.</span></span> <span data-ttu-id="09cba-122">Os valores de 4-7 são típicos.</span><span class="sxs-lookup"><span data-stu-id="09cba-122">Values of 4-7 are typical.</span></span> <span data-ttu-id="09cba-123">Os reflexos não espelham outros objetos; apenas as fontes de luz do Pinpoint são refletidas.</span><span class="sxs-lookup"><span data-stu-id="09cba-123">Reflections do not mirror other objects; only pinpoint light sources are reflected.</span></span> <span data-ttu-id="09cba-124">O valor padrão é 5.</span><span class="sxs-lookup"><span data-stu-id="09cba-124">Default value is 5.</span></span>

<span data-ttu-id="09cba-125">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="09cba-125">*Microsoft Office Extensions Attribute*</span></span>

 

 