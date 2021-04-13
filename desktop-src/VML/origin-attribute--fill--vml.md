---
title: Atributo de origem (preenchimento) (VML)
description: Atributo de origem (preenchimento) (VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366666"
---
# <a name="origin-attribute-fillvml"></a><span data-ttu-id="0b887-103">Atributo de origem (preenchimento) (VML)</span><span class="sxs-lookup"><span data-stu-id="0b887-103">Origin Attribute (Fill)(VML)</span></span>

<span data-ttu-id="0b887-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0b887-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0b887-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="0b887-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0b887-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="0b887-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0b887-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="0b887-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0b887-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0b887-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0b887-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0b887-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0b887-110">Define o centro de uma imagem de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="0b887-110">Defines the center of a fill image.</span></span> <span data-ttu-id="0b887-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0b887-111">Read/write.</span></span> <span data-ttu-id="0b887-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="0b887-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="0b887-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="0b887-113">**Applies To**</span></span>

[<span data-ttu-id="0b887-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="0b887-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="0b887-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="0b887-115">**Tag Syntax**</span></span>

<span data-ttu-id="0b887-116"><v: *elemento* Origin = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="0b887-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="0b887-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="0b887-117">**Script Syntax**</span></span>

<span data-ttu-id="0b887-118">*elemento* . Origin = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="0b887-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="0b887-119">*expressão* = de *elemento*. Origin</span><span class="sxs-lookup"><span data-stu-id="0b887-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="0b887-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="0b887-120">**Remarks**</span></span>

<span data-ttu-id="0b887-121">Especifica um ponto relativo ao canto superior esquerdo da imagem; esse ponto é tratado como a origem da imagem.</span><span class="sxs-lookup"><span data-stu-id="0b887-121">Specifies a point relative to the upper left corner of the image; this point is treated as the origin of the image.</span></span> <span data-ttu-id="0b887-122">O padrão é o centro da imagem.</span><span class="sxs-lookup"><span data-stu-id="0b887-122">Default is the center of the image.</span></span> <span data-ttu-id="0b887-123">O vetor é uma fração da largura e da altura da imagem.</span><span class="sxs-lookup"><span data-stu-id="0b887-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="0b887-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="0b887-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="0b887-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="0b887-125">**Example**</span></span>

<span data-ttu-id="0b887-126">A imagem do preenchimento é deslocada para a esquerda para um ponto de 50% da largura da forma.</span><span class="sxs-lookup"><span data-stu-id="0b887-126">The image of the fill is shifted left to a point 50% of the width of the shape .</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 