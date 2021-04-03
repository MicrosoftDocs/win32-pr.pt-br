---
title: Atributo de posição (Fill) (VML)
description: Atributo de posição (Fill) (VML)
ms.assetid: 0d532d4c-0c96-4f41-b54f-55b6aade0c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01fff487f134d50b5a72623abf21c0b5710f9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084858"
---
# <a name="position-attribute-fillvml"></a><span data-ttu-id="f610b-103">Atributo de posição (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="f610b-103">Position Attribute (Fill)(VML)</span></span>

<span data-ttu-id="f610b-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f610b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f610b-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="f610b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f610b-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="f610b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f610b-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="f610b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f610b-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f610b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f610b-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f610b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f610b-110">Define a posição da imagem de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="f610b-110">Defines the position of fill image.</span></span> <span data-ttu-id="f610b-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f610b-111">Read/write.</span></span> <span data-ttu-id="f610b-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="f610b-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="f610b-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="f610b-113">**Applies To**</span></span>

[<span data-ttu-id="f610b-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="f610b-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="f610b-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="f610b-115">**Tag Syntax**</span></span>

<span data-ttu-id="f610b-116"><v: *elemento* position = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="f610b-116"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="f610b-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="f610b-117">**Script Syntax**</span></span>

<span data-ttu-id="f610b-118">*elemento* . Position = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="f610b-118">*element* .position="*expression*"</span></span>

<span data-ttu-id="f610b-119">*expressão* = de *elemento*. Position</span><span class="sxs-lookup"><span data-stu-id="f610b-119">*expression*=*element*.position</span></span>

<span data-ttu-id="f610b-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="f610b-120">**Remarks**</span></span>

<span data-ttu-id="f610b-121">Especifica um ponto na forma para posicionar a origem da imagem.</span><span class="sxs-lookup"><span data-stu-id="f610b-121">Specifies a point in the shape to position the origin of the image.</span></span> <span data-ttu-id="f610b-122">O padrão é o centro do retângulo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f610b-122">Default is the center of the container rectangle.</span></span> <span data-ttu-id="f610b-123">O vetor é uma fração da largura e da altura da imagem.</span><span class="sxs-lookup"><span data-stu-id="f610b-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="f610b-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="f610b-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="f610b-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="f610b-125">**Example**</span></span>

<span data-ttu-id="f610b-126">A imagem do preenchimento é deslocada para a direita para um ponto de 50% da largura da forma.</span><span class="sxs-lookup"><span data-stu-id="f610b-126">The image of the fill is shifted right to a point 50% of the width of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" position="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 