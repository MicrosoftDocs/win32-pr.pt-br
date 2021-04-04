---
title: Atributo StartAngle de VML
description: Atributo StartAngle de VML
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e779d343061ef65decb1dd21f615e054d561da28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007793"
---
# <a name="vml-startangle-attribute"></a><span data-ttu-id="dad89-103">Atributo StartAngle de VML</span><span class="sxs-lookup"><span data-stu-id="dad89-103">VML StartAngle Attribute</span></span>

<span data-ttu-id="dad89-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="dad89-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dad89-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="dad89-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dad89-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="dad89-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dad89-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="dad89-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dad89-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="dad89-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dad89-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="dad89-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dad89-110">Define o ponto inicial do arco. Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="dad89-110">Defines the starting point of the arc. Read/write.</span></span> <span data-ttu-id="dad89-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="dad89-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="dad89-112">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="dad89-112">**Applies To**</span></span>

[<span data-ttu-id="dad89-113">Arc</span><span class="sxs-lookup"><span data-stu-id="dad89-113">Arc</span></span>](msdn-online-vml-arc-element.md)

<span data-ttu-id="dad89-114">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="dad89-114">**Tag Syntax**</span></span>

<span data-ttu-id="dad89-115"><v: *Element* arângulo = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="dad89-115"><v: *element* endangle=" *expression* "></span></span>

<span data-ttu-id="dad89-116">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="dad89-116">**Script Syntax**</span></span>

<span data-ttu-id="dad89-117">*elemento* . endângulo = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="dad89-117">*element* .endAngle="*expression*"</span></span>

<span data-ttu-id="dad89-118">*expressão* = de ângulo de *elemento*.</span><span class="sxs-lookup"><span data-stu-id="dad89-118">*expression*=*element*.endAngle</span></span>

<span data-ttu-id="dad89-119">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="dad89-119">**Remarks**</span></span>

<span data-ttu-id="dad89-120">O arco é definido como um traço desenhado ao longo de uma oval limitada pelos atributos de **estilo** de uma forma.</span><span class="sxs-lookup"><span data-stu-id="dad89-120">The arc is defined as a stroke drawn along an oval bounded by the **Style** attributes of a shape.</span></span> <span data-ttu-id="dad89-121">O início do traço é definido por um ângulo medido de forma direta (12 horas) no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="dad89-121">The start of the stroke is defined by an angle measured from straight up (12 o'clock) clockwise.</span></span> <span data-ttu-id="dad89-122">O valor padrão é 0 graus.</span><span class="sxs-lookup"><span data-stu-id="dad89-122">The default value is 0 degrees.</span></span>

<span data-ttu-id="dad89-123">Atributo padrão da VML</span><span class="sxs-lookup"><span data-stu-id="dad89-123">VML Standard Attribute</span></span>

<span data-ttu-id="dad89-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="dad89-124">**Example**</span></span>

<span data-ttu-id="dad89-125">O arco é sorrindo.</span><span class="sxs-lookup"><span data-stu-id="dad89-125">The arc is smiling.</span></span> <span data-ttu-id="dad89-126">O ponto de partida está no ponto de 90 graus de uma elipse inscrita dentro da caixa delimitadora de forma.</span><span class="sxs-lookup"><span data-stu-id="dad89-126">The start point is at the 90-degree point of an oval inscribed inside the shape bounding box.</span></span> <span data-ttu-id="dad89-127">O ponto de extremidade está no ponto de 270 graus da elipse.</span><span class="sxs-lookup"><span data-stu-id="dad89-127">The end point is at the 270-degree point of the oval.</span></span>


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 