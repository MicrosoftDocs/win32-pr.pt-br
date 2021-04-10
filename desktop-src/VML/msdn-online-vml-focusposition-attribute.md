---
title: Atributo FocusPosition de VML
description: Atributo FocusPosition de VML
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084882"
---
# <a name="vml-focusposition-attribute"></a><span data-ttu-id="b82fd-103">Atributo FocusPosition de VML</span><span class="sxs-lookup"><span data-stu-id="b82fd-103">VML FocusPosition Attribute</span></span>

<span data-ttu-id="b82fd-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b82fd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b82fd-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="b82fd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b82fd-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="b82fd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b82fd-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="b82fd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b82fd-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b82fd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b82fd-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b82fd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b82fd-110">Define o centro de um gradiente radial.</span><span class="sxs-lookup"><span data-stu-id="b82fd-110">Defines the center of a radial gradient.</span></span> <span data-ttu-id="b82fd-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b82fd-111">Read/write.</span></span> <span data-ttu-id="b82fd-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="b82fd-112">**VgVector2D**.</span></span>

<span data-ttu-id="b82fd-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="b82fd-113">**Applies To**</span></span>

[<span data-ttu-id="b82fd-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="b82fd-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="b82fd-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="b82fd-115">**Tag Syntax**</span></span>

<span data-ttu-id="b82fd-116"><v: *Element* focusposition = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="b82fd-116"><v: *element* focusposition=" *expression* "></span></span>

<span data-ttu-id="b82fd-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="b82fd-117">**Script Syntax**</span></span>

<span data-ttu-id="b82fd-118">*Element* . focusposition = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="b82fd-118">*element* .focusposition="*expression*"</span></span>

<span data-ttu-id="b82fd-119">*expressão* = de *elemento*. focusposition</span><span class="sxs-lookup"><span data-stu-id="b82fd-119">*expression*=*element*.focusposition</span></span>

<span data-ttu-id="b82fd-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="b82fd-120">**Remarks**</span></span>

<span data-ttu-id="b82fd-121">Especifica os gradientes radiais do positionfor Center.</span><span class="sxs-lookup"><span data-stu-id="b82fd-121">Specifies the center positionfor radial gradients.</span></span> <span data-ttu-id="b82fd-122">O vetor é uma fração da largura e da altura da forma.</span><span class="sxs-lookup"><span data-stu-id="b82fd-122">The vector is a fraction of the width and height of the shape.</span></span> <span data-ttu-id="b82fd-123">A primeira é uma porcentagem do preenchimento para a borda esquerda; a segunda é uma porcentagem do preenchimento para a parte superior.</span><span class="sxs-lookup"><span data-stu-id="b82fd-123">The first is a percentage of the fill to the left edge; the second is a percentage of the fill to the top.</span></span> <span data-ttu-id="b82fd-124">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="b82fd-124">The default value is 0,0.</span></span> <span data-ttu-id="b82fd-125">Para posicionar um preenchimento radial no centro de uma forma, use o valor de 50%, 50%.</span><span class="sxs-lookup"><span data-stu-id="b82fd-125">To position a radial fill at the center of a shape, use the value of 50%,50%.</span></span>

<span data-ttu-id="b82fd-126">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="b82fd-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="b82fd-127">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="b82fd-127">**Example**</span></span>

<span data-ttu-id="b82fd-128">O preenchimento radial será centralizado para que o azul seja iniciado no centro e radiado para fora, mudando gradualmente para vermelho no momento em que atingir as bordas externas e os cantos.</span><span class="sxs-lookup"><span data-stu-id="b82fd-128">The radial fill will be centered so that blue will start in the center and radiate outward, gradually changing to red by the time it reaches the outside edges and corners.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 