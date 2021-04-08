---
title: Atributo FillType da VML
description: Atributo FillType da VML
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917655"
---
# <a name="vml-filltype-attribute"></a><span data-ttu-id="3dbd4-103">Atributo FillType da VML</span><span class="sxs-lookup"><span data-stu-id="3dbd4-103">VML FillType Attribute</span></span>

<span data-ttu-id="3dbd4-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3dbd4-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3dbd4-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3dbd4-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3dbd4-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3dbd4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3dbd4-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3dbd4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3dbd4-110">Define o tipo de preenchimento usado para o plano de fundo de um traço.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-110">Defines the type of fill used for the background of a stroke.</span></span> <span data-ttu-id="3dbd4-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-111">Read/write.</span></span> <span data-ttu-id="3dbd4-112">**VgFillType**.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-112">**VgFillType**.</span></span>

<span data-ttu-id="3dbd4-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="3dbd4-113">**Applies To**</span></span>

[<span data-ttu-id="3dbd4-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="3dbd4-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="3dbd4-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="3dbd4-115">**Tag Syntax**</span></span>

<span data-ttu-id="3dbd4-116"><v: *Element* FILLIN = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3dbd4-116"><v: *element* filltype=" *expression* "></span></span>

<span data-ttu-id="3dbd4-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="3dbd4-117">**Script Syntax**</span></span>

<span data-ttu-id="3dbd4-118">*elemento* . FillType = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="3dbd4-118">*element* .filltype="*expression*"</span></span>

<span data-ttu-id="3dbd4-119">*expressão* = de *elemento*. FillType</span><span class="sxs-lookup"><span data-stu-id="3dbd4-119">*expression*=*element*.filltype</span></span>

<span data-ttu-id="3dbd4-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="3dbd4-120">**Remarks**</span></span>

<span data-ttu-id="3dbd4-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="3dbd4-121">Values include:</span></span>



| <span data-ttu-id="3dbd4-122">DashStyle</span><span class="sxs-lookup"><span data-stu-id="3dbd4-122">DashStyle</span></span> | <span data-ttu-id="3dbd4-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="3dbd4-123">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="3dbd4-124">Sólido</span><span class="sxs-lookup"><span data-stu-id="3dbd4-124">Solid</span></span>     | <span data-ttu-id="3dbd4-125">O padrão de preenchimento é sólido.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-125">The fill pattern is solid.</span></span> <span data-ttu-id="3dbd4-126">Valor padrão.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-126">Default value.</span></span>      |
| <span data-ttu-id="3dbd4-127">Tile</span><span class="sxs-lookup"><span data-stu-id="3dbd4-127">Tile</span></span>      | <span data-ttu-id="3dbd4-128">A imagem de preenchimento é disposta lado a lado.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-128">The fill image is tiled.</span></span>                       |
| <span data-ttu-id="3dbd4-129">Padrão</span><span class="sxs-lookup"><span data-stu-id="3dbd4-129">Pattern</span></span>   | <span data-ttu-id="3dbd4-130">A imagem de preenchimento é ampliada para formar um padrão.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-130">The fill image is stretched to form a pattern.</span></span> |
| <span data-ttu-id="3dbd4-131">Quadro</span><span class="sxs-lookup"><span data-stu-id="3dbd4-131">Frame</span></span>     | <span data-ttu-id="3dbd4-132">A imagem de preenchimento torna-se uma borda para a forma.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-132">The fill image becomes a border for the shape.</span></span> |



 

<span data-ttu-id="3dbd4-133">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="3dbd4-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="3dbd4-134">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="3dbd4-134">**Example**</span></span>

<span data-ttu-id="3dbd4-135">O traço da forma tem uma textura do lado do ladrilho criado a partir da imagem de cylinder.gif.</span><span class="sxs-lookup"><span data-stu-id="3dbd4-135">The stroke of the shape has a tiled texture created from the cylinder.gif image.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 