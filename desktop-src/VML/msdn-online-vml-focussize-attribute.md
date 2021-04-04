---
title: Atributo FocusSize de VML
description: Atributo FocusSize de VML
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008341"
---
# <a name="vml-focussize-attribute"></a><span data-ttu-id="d6c77-103">Atributo FocusSize de VML</span><span class="sxs-lookup"><span data-stu-id="d6c77-103">VML FocusSize Attribute</span></span>

<span data-ttu-id="d6c77-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d6c77-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d6c77-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="d6c77-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d6c77-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="d6c77-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d6c77-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="d6c77-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d6c77-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d6c77-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d6c77-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d6c77-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d6c77-110">Define o tamanho do foco para preenchimentos radiais.</span><span class="sxs-lookup"><span data-stu-id="d6c77-110">Defines the focus size for radial fills.</span></span> <span data-ttu-id="d6c77-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d6c77-111">Read/write.</span></span> <span data-ttu-id="d6c77-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="d6c77-112">**VgVector2D**.</span></span>

<span data-ttu-id="d6c77-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="d6c77-113">**Applies To**</span></span>

[<span data-ttu-id="d6c77-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="d6c77-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="d6c77-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="d6c77-115">**Tag Syntax**</span></span>

<span data-ttu-id="d6c77-116"><v: *Element* focussize = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="d6c77-116"><v: *element* focussize=" *expression* "></span></span>

<span data-ttu-id="d6c77-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="d6c77-117">**Script Syntax**</span></span>

<span data-ttu-id="d6c77-118">*Element* . focussize = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="d6c77-118">*element* .focussize="*expression*"</span></span>

<span data-ttu-id="d6c77-119">*expressão* = de *elemento*. focussize</span><span class="sxs-lookup"><span data-stu-id="d6c77-119">*expression*=*element*.focussize</span></span>

<span data-ttu-id="d6c77-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="d6c77-120">**Remarks**</span></span>

<span data-ttu-id="d6c77-121">Os valores são frações de largura e altura da forma.</span><span class="sxs-lookup"><span data-stu-id="d6c77-121">The values are fractions of the width and height of the shape.</span></span> <span data-ttu-id="d6c77-122">A primeira é uma porcentagem do preenchimento para a borda direita da forma e a segunda é uma porcentagem do preenchimento até a parte inferior da forma.</span><span class="sxs-lookup"><span data-stu-id="d6c77-122">The first is a percentage of the fill to the right edge of the shape and the second is a percentage of the fill to the bottom of the shape.</span></span> <span data-ttu-id="d6c77-123">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="d6c77-123">The default value is 0,0.</span></span> <span data-ttu-id="d6c77-124">Um valor de **FocusSize** de 100%, 100% e um **FocusPosition** de 0, 0 faria com que Color2 dominasse completamente o Blend.</span><span class="sxs-lookup"><span data-stu-id="d6c77-124">A **FocusSize** value of 100%,100% and a **FocusPosition** of 0,0 would make Color2 dominate the blend completely.</span></span> <span data-ttu-id="d6c77-125">Valores pequenos de cerca de 10%, 10% são recomendados para mesclagens balanceadas.</span><span class="sxs-lookup"><span data-stu-id="d6c77-125">Small values of around 10%,10% are recommended for balanced blends.</span></span>

<span data-ttu-id="d6c77-126">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="d6c77-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="d6c77-127">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="d6c77-127">**Example**</span></span>

<span data-ttu-id="d6c77-128">O preenchimento radial criará uma mistura começando no centro como azul e ficando vermelha em todas as quatro bordas.</span><span class="sxs-lookup"><span data-stu-id="d6c77-128">The radial fill will create a blend starting in the center as blue and becoming red on all four edges.</span></span> <span data-ttu-id="d6c77-129">O centro do Blend é definido por **FocusPosition** e o tamanho da cor de início interna é determinado por **FocusSize**.</span><span class="sxs-lookup"><span data-stu-id="d6c77-129">The center of the blend is defined by **FocusPosition** and the size of the inner starting color is determined by **FocusSize**.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 