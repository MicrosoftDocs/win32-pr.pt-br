---
title: Atributo de arco de VML
description: Atributo de arco de VML
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a4027f079ffb284125032570dd2293b1ab69e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810630"
---
# <a name="vml-arcsize-attribute"></a><span data-ttu-id="c1ab0-103">Atributo de arco de VML</span><span class="sxs-lookup"><span data-stu-id="c1ab0-103">VML ArcSize Attribute</span></span>

<span data-ttu-id="c1ab0-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c1ab0-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c1ab0-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c1ab0-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c1ab0-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c1ab0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c1ab0-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c1ab0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c1ab0-110">Define a quantidade de arredondamento para um retângulo arredondado.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-110">Defines the amount of roundness for a rounded rectangle.</span></span> <span data-ttu-id="c1ab0-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-111">Read/write.</span></span> <span data-ttu-id="c1ab0-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="c1ab0-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="c1ab0-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="c1ab0-113">**Applies To**</span></span>

[<span data-ttu-id="c1ab0-114">RoundRect</span><span class="sxs-lookup"><span data-stu-id="c1ab0-114">RoundRect</span></span>](msdn-online-vml-roundrect-element.md)

<span data-ttu-id="c1ab0-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="c1ab0-115">**Tag Syntax**</span></span>

<span data-ttu-id="c1ab0-116"><v: *Element* = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c1ab0-116"><v: *element* arcsize=" *expression* "></span></span>

<span data-ttu-id="c1ab0-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="c1ab0-117">**Script Syntax**</span></span>

<span data-ttu-id="c1ab0-118">*Element* . anestable = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="c1ab0-118">*element* .arcSize="*expression*"</span></span>

<span data-ttu-id="c1ab0-119">*expressão* = de *elemento*. arcoize</span><span class="sxs-lookup"><span data-stu-id="c1ab0-119">*expression*=*element*.arcSize</span></span>

<span data-ttu-id="c1ab0-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="c1ab0-120">**Remarks**</span></span>

<span data-ttu-id="c1ab0-121">Define os cantos arredondados de um retângulo arredondado como uma porcentagem da metade da dimensão menor do comprimento e da largura de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-121">Defines the rounded corners of a rounded rectangle as a percentage of half the smaller dimension of the length and width of a rectangle.</span></span> <span data-ttu-id="c1ab0-122">0% teria cantos quadrados e 100% formaria cantos circulares.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-122">0% would have square corners, and 100% would form circular corners.</span></span> <span data-ttu-id="c1ab0-123">Um quadrado com um valor de **arcos** de 1,0 seria um círculo.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-123">A square with an **ArcSize** value of 1.0 would be a circle.</span></span> <span data-ttu-id="c1ab0-124">O valor padrão é 0,2 (20%).</span><span class="sxs-lookup"><span data-stu-id="c1ab0-124">The default value is 0.2 (20%).</span></span>

<span data-ttu-id="c1ab0-125">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="c1ab0-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="c1ab0-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="c1ab0-126">**Example**</span></span>

<span data-ttu-id="c1ab0-127">O retângulo arredondado é desenhado com cantos apertados e arredondados.</span><span class="sxs-lookup"><span data-stu-id="c1ab0-127">The rounded rectangle is drawn with tight-but-rounded corners.</span></span>


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 