---
title: Atributo ColorMode da VML
description: Atributo ColorMode da VML
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7126a3f5a95910eb85007fe9a80d500c5233e5e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366230"
---
# <a name="vml-colormode-attribute"></a><span data-ttu-id="56062-103">Atributo ColorMode da VML</span><span class="sxs-lookup"><span data-stu-id="56062-103">VML ColorMode Attribute</span></span>

<span data-ttu-id="56062-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="56062-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="56062-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="56062-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="56062-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="56062-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="56062-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="56062-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="56062-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="56062-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="56062-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="56062-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="56062-110">Determina o modo de cor da extrusão.</span><span class="sxs-lookup"><span data-stu-id="56062-110">Determines the mode of extrusion color.</span></span> <span data-ttu-id="56062-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="56062-111">Read/write.</span></span> <span data-ttu-id="56062-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="56062-112">**VgTriState**.</span></span>

<span data-ttu-id="56062-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="56062-113">**Applies To**</span></span>

[<span data-ttu-id="56062-114">Extrusão</span><span class="sxs-lookup"><span data-stu-id="56062-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="56062-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="56062-115">**Tag Syntax**</span></span>

<span data-ttu-id="56062-116"><o: *elemento* ColorMode = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="56062-116"><o: *element* colormode=" *expression* "></span></span>

<span data-ttu-id="56062-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="56062-117">**Script Syntax**</span></span>

<span data-ttu-id="56062-118">*elemento* . ColorMode = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="56062-118">*element* .colormode="*expression*"</span></span>

<span data-ttu-id="56062-119">*expressão* = de *elemento*. ColorMode</span><span class="sxs-lookup"><span data-stu-id="56062-119">*expression*=*element*.colormode</span></span>

<span data-ttu-id="56062-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="56062-120">**Remarks**</span></span>

<span data-ttu-id="56062-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="56062-121">Values include:</span></span>



| <span data-ttu-id="56062-122">Valor</span><span class="sxs-lookup"><span data-stu-id="56062-122">Value</span></span>  | <span data-ttu-id="56062-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="56062-123">Description</span></span>                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56062-124">auto</span><span class="sxs-lookup"><span data-stu-id="56062-124">auto</span></span>   | <span data-ttu-id="56062-125">Especifica que a cor da extrusão é igual à cor de preenchimento da forma.</span><span class="sxs-lookup"><span data-stu-id="56062-125">Specifies that the color of the extrusion is the same as the fill color of the shape.</span></span> <span data-ttu-id="56062-126">Padrão.</span><span class="sxs-lookup"><span data-stu-id="56062-126">Default.</span></span>                |
| <span data-ttu-id="56062-127">custom</span><span class="sxs-lookup"><span data-stu-id="56062-127">custom</span></span> | <span data-ttu-id="56062-128">Especifica que a extrusão será a cor do atributo [Color](color-attribute--extrusion--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="56062-128">Specifies that the extrusion will be the color of the [Color](color-attribute--extrusion--vml.md) attribute.</span></span> |



 

<span data-ttu-id="56062-129">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="56062-129">*Microsoft Office Extensions Attribute*</span></span>

 

 