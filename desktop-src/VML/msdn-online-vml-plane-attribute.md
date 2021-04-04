---
title: Atributo de plano VML
description: Atributo de plano VML
ms.assetid: e1de630b-8e25-4052-b316-251046f73e98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f279f008adf8f12f78d6edd790cc533678adc9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917404"
---
# <a name="vml-plane-attribute"></a><span data-ttu-id="5661a-103">Atributo de plano VML</span><span class="sxs-lookup"><span data-stu-id="5661a-103">VML Plane Attribute</span></span>

<span data-ttu-id="5661a-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5661a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5661a-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="5661a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5661a-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="5661a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5661a-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="5661a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5661a-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5661a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5661a-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5661a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5661a-110">Especifica o plano que está em ângulos retos para a extrusão.</span><span class="sxs-lookup"><span data-stu-id="5661a-110">Specifies the plane that is at right angles to the extrusion.</span></span> <span data-ttu-id="5661a-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5661a-111">Read/write.</span></span> <span data-ttu-id="5661a-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="5661a-112">**String**.</span></span>

<span data-ttu-id="5661a-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="5661a-113">**Applies To**</span></span>

[<span data-ttu-id="5661a-114">Extrusão</span><span class="sxs-lookup"><span data-stu-id="5661a-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="5661a-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="5661a-115">**Tag Syntax**</span></span>

<span data-ttu-id="5661a-116"><o: *Element* avião = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="5661a-116"><o: *element* plane=" *expression* "></span></span>

<span data-ttu-id="5661a-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="5661a-117">**Script Syntax**</span></span>

<span data-ttu-id="5661a-118">*Element* . avião = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="5661a-118">*element* .plane="*expression*"</span></span>

<span data-ttu-id="5661a-119">*expressão* = de *elemento*. avião</span><span class="sxs-lookup"><span data-stu-id="5661a-119">*expression*=*element*.plane</span></span>

<span data-ttu-id="5661a-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="5661a-120">**Remarks**</span></span>

<span data-ttu-id="5661a-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="5661a-121">Values include:</span></span>



| <span data-ttu-id="5661a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5661a-122">Value</span></span> | <span data-ttu-id="5661a-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="5661a-123">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="5661a-124">xy</span><span class="sxs-lookup"><span data-stu-id="5661a-124">xy</span></span>    | <span data-ttu-id="5661a-125">A extrusão está em ângulos retos para o plano XY.</span><span class="sxs-lookup"><span data-stu-id="5661a-125">Extrusion is at right angles to the xy -plane.</span></span> <span data-ttu-id="5661a-126">Padrão</span><span class="sxs-lookup"><span data-stu-id="5661a-126">Default</span></span> |
| <span data-ttu-id="5661a-127">ZX</span><span class="sxs-lookup"><span data-stu-id="5661a-127">zx</span></span>    | <span data-ttu-id="5661a-128">A extrusão está em ângulos retos para o plano ZX.</span><span class="sxs-lookup"><span data-stu-id="5661a-128">Extrusion is at right angles to the zx -plane.</span></span>         |
| <span data-ttu-id="5661a-129">yz</span><span class="sxs-lookup"><span data-stu-id="5661a-129">yz</span></span>    | <span data-ttu-id="5661a-130">A extrusão está em ângulos retos para o YZ.</span><span class="sxs-lookup"><span data-stu-id="5661a-130">Extrusion is at right angles to the yz -plane.</span></span>         |



 

<span data-ttu-id="5661a-131">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="5661a-131">*Microsoft Office Extensions Attribute*</span></span>

 

 