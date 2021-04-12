---
title: Atributo de ângulo de fim da VML
description: Atributo de ângulo de fim da VML
ms.assetid: fc8276dc-8f61-42f4-b405-e92ca31e4637
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b22f157a1ccfc2337baa0bb5de747332bb78d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294468"
---
# <a name="vml-endangle-attribute"></a><span data-ttu-id="7b670-103">Atributo de ângulo de fim da VML</span><span class="sxs-lookup"><span data-stu-id="7b670-103">VML EndAngle Attribute</span></span>

<span data-ttu-id="7b670-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7b670-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7b670-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="7b670-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7b670-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="7b670-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7b670-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="7b670-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7b670-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7b670-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7b670-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7b670-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7b670-110">Define o ponto de extremidade do arco. Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7b670-110">Defines the endpoint of the arc. Read/write.</span></span> <span data-ttu-id="7b670-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="7b670-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="7b670-112">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="7b670-112">**Applies To**</span></span>

[<span data-ttu-id="7b670-113">Arc</span><span class="sxs-lookup"><span data-stu-id="7b670-113">Arc</span></span>](msdn-online-vml-arc-element.md)

<span data-ttu-id="7b670-114">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="7b670-114">**Tag Syntax**</span></span>

<span data-ttu-id="7b670-115"><v: *Element* arângulo = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7b670-115"><v: *element* endangle=" *expression* "></span></span>

<span data-ttu-id="7b670-116">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="7b670-116">**Script Syntax**</span></span>

<span data-ttu-id="7b670-117">*elemento* . endângulo = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="7b670-117">*element* .endAngle="*expression*"</span></span>

<span data-ttu-id="7b670-118">*expressão* = de ângulo de *elemento*.</span><span class="sxs-lookup"><span data-stu-id="7b670-118">*expression*=*element*.endAngle</span></span>

<span data-ttu-id="7b670-119">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="7b670-119">**Remarks**</span></span>

<span data-ttu-id="7b670-120">O arco é definido como um traço desenhado ao longo de uma oval limitada pelos atributos de **estilo** de uma forma.</span><span class="sxs-lookup"><span data-stu-id="7b670-120">The arc is defined as a stroke drawn along an oval bounded by the **Style** attributes of a shape.</span></span> <span data-ttu-id="7b670-121">O final do traço é definido por um ângulo medido de forma direta (12 horas) no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="7b670-121">The end of the stroke is defined by an angle measured from straight up (12 o'clock) clockwise.</span></span> <span data-ttu-id="7b670-122">O valor padrão é 90 graus.</span><span class="sxs-lookup"><span data-stu-id="7b670-122">The default value is 90 degrees.</span></span>

<span data-ttu-id="7b670-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="7b670-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="7b670-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="7b670-124">**Example**</span></span>

<span data-ttu-id="7b670-125">O arco é sorrindo.</span><span class="sxs-lookup"><span data-stu-id="7b670-125">The arc is smiling.</span></span> <span data-ttu-id="7b670-126">O ponto de partida está no ponto de 90 graus de uma elipse inscrita dentro da caixa delimitadora de forma.</span><span class="sxs-lookup"><span data-stu-id="7b670-126">The start point is at the 90-degree point of an oval inscribed inside the shape bounding box.</span></span> <span data-ttu-id="7b670-127">O ponto de extremidade está no ponto de 270 graus da elipse.</span><span class="sxs-lookup"><span data-stu-id="7b670-127">The end point is at the 270-degree point of the oval.</span></span>


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 