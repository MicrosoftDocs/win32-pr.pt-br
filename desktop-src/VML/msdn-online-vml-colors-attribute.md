---
title: Atributo de cores da VML
description: Atributo de cores da VML
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499103"
---
# <a name="vml-colors-attribute"></a><span data-ttu-id="3a7e7-103">Atributo de cores da VML</span><span class="sxs-lookup"><span data-stu-id="3a7e7-103">VML Colors Attribute</span></span>

<span data-ttu-id="3a7e7-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3a7e7-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3a7e7-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3a7e7-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3a7e7-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3a7e7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3a7e7-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3a7e7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3a7e7-110">Define várias cores para um preenchimento gradual.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-110">Defines multiple colors for a gradient fill.</span></span> <span data-ttu-id="3a7e7-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-111">Read/write.</span></span> <span data-ttu-id="3a7e7-112">**IVgGradientColorArray**.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-112">**IVgGradientColorArray**.</span></span>

<span data-ttu-id="3a7e7-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="3a7e7-113">**Applies To**</span></span>

[<span data-ttu-id="3a7e7-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="3a7e7-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="3a7e7-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="3a7e7-115">**Tag Syntax**</span></span>

<span data-ttu-id="3a7e7-116"><v: *Element* Colors = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3a7e7-116"><v: *element* colors=" *expression* "></span></span>

<span data-ttu-id="3a7e7-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="3a7e7-117">**Script Syntax**</span></span>

<span data-ttu-id="3a7e7-118">*Element* . Colors = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="3a7e7-118">*element* .colors="*expression*"</span></span>

<span data-ttu-id="3a7e7-119">*expressão* = de *elemento*. Colors</span><span class="sxs-lookup"><span data-stu-id="3a7e7-119">*expression*=*element*.colors</span></span>

<span data-ttu-id="3a7e7-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="3a7e7-120">**Remarks**</span></span>

<span data-ttu-id="3a7e7-121">Usado para definir uma matriz que consiste em valores emparelhados de percentuais ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) e Color ([VgColor](msdn-online-vml-ivgcolor.md)).</span><span class="sxs-lookup"><span data-stu-id="3a7e7-121">Used to define an array consisting of paired values of percentages ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) and color ([VgColor](msdn-online-vml-ivgcolor.md)).</span></span> <span data-ttu-id="3a7e7-122">A matriz cria um preenchimento combinado usando cada ponto na matriz, começando em 0% (definido por **cor**) e terminando em 100% (definido por **Color2**).</span><span class="sxs-lookup"><span data-stu-id="3a7e7-122">The array creates a blended fill using each point in the array, starting at 0% (defined by **Color**) and ending at 100% (defined by **Color2**).</span></span> <span data-ttu-id="3a7e7-123">As cores intermediárias ao longo do caminho podem ser definidas atribuindo um valor de cor a uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-123">Intermediate colors along the way can be defined by assigning a color value to a percentage.</span></span> <span data-ttu-id="3a7e7-124">O par de porcentagem e de cores não é separado por uma vírgula, mas os pares são separados uns dos outros por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-124">The percent and color pair are not separated by a comma, but pairs are separated from each other by commas.</span></span>

<span data-ttu-id="3a7e7-125">Atributo padrão da VML</span><span class="sxs-lookup"><span data-stu-id="3a7e7-125">VML Standard Attribute</span></span>

<span data-ttu-id="3a7e7-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="3a7e7-126">**Example**</span></span>

<span data-ttu-id="3a7e7-127">A forma tem um preenchimento gradual que consiste em quatro cores, começando com vermelho, mesclando para amarelo, em seguida, verde e finallyblue.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-127">The shape has a gradient fill consisting of four colors, starting with red, blending to yellow, then green, and finallyblue.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 