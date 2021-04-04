---
title: Atributo de pontos de VML
description: Atributo de pontos de VML
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007643"
---
# <a name="vml-points-attribute"></a><span data-ttu-id="3e7a9-103">Atributo de pontos de VML</span><span class="sxs-lookup"><span data-stu-id="3e7a9-103">VML Points Attribute</span></span>

<span data-ttu-id="3e7a9-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3e7a9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3e7a9-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="3e7a9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3e7a9-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="3e7a9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3e7a9-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="3e7a9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3e7a9-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3e7a9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3e7a9-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3e7a9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3e7a9-110">Define um conjunto de pontos que compõem uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="3e7a9-110">Defines a set of points that make up a polyline.</span></span> <span data-ttu-id="3e7a9-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3e7a9-111">Read/write.</span></span> <span data-ttu-id="3e7a9-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="3e7a9-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .</span></span>

<span data-ttu-id="3e7a9-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="3e7a9-113">**Applies To**</span></span>

[<span data-ttu-id="3e7a9-114">Múltipla</span><span class="sxs-lookup"><span data-stu-id="3e7a9-114">Polyline</span></span>](msdn-online-vml-polyline-element.md)

<span data-ttu-id="3e7a9-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="3e7a9-115">**Tag Syntax**</span></span>

<span data-ttu-id="3e7a9-116"><v: *Element* Points = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3e7a9-116"><v: *element* points=" *expression* "></span></span>

<span data-ttu-id="3e7a9-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="3e7a9-117">**Script Syntax**</span></span>

<span data-ttu-id="3e7a9-118">*Element* . Points = "*Expression \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="3e7a9-118">*element* .points="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="3e7a9-119">*expressão* = de *elemento*. Points</span><span class="sxs-lookup"><span data-stu-id="3e7a9-119">*expression*=*element*.points</span></span>

<span data-ttu-id="3e7a9-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="3e7a9-120">**Remarks**</span></span>

<span data-ttu-id="3e7a9-121">Define um conjunto de segmentos de linha reta que são compostos por uma série de pontos.</span><span class="sxs-lookup"><span data-stu-id="3e7a9-121">Defines a set of straight line segments that are composed of a series of points.</span></span> <span data-ttu-id="3e7a9-122">Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado).</span><span class="sxs-lookup"><span data-stu-id="3e7a9-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="3e7a9-123">O valor padrão é "0, 0 10, 10".</span><span class="sxs-lookup"><span data-stu-id="3e7a9-123">The default value is "0,0 10,10".</span></span> <span data-ttu-id="3e7a9-124">Observe que as vírgulas não são necessárias, mas elas tornam a legibilidade mais fácil.</span><span class="sxs-lookup"><span data-stu-id="3e7a9-124">Note that commas are not required, but they make for easier readability.</span></span>

<span data-ttu-id="3e7a9-125">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="3e7a9-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="3e7a9-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="3e7a9-126">**Example**</span></span>

<span data-ttu-id="3e7a9-127">A polilinha começa no ponto 10, 10 e termina em 100.100, com os valores de pontos.</span><span class="sxs-lookup"><span data-stu-id="3e7a9-127">The polyline starts at the point 10,10 and ends at 100,100, with the valuesin points.</span></span>


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 