---
title: Atributo de deslocamento (sombra) (VML)
description: Atributo de deslocamento (sombra) (VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917368"
---
# <a name="offset-attribute-shadowvml"></a><span data-ttu-id="b9909-103">Atributo de deslocamento (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="b9909-103">Offset Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="b9909-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b9909-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b9909-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="b9909-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b9909-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="b9909-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b9909-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="b9909-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b9909-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b9909-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b9909-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b9909-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b9909-110">Define até que distância a sombra ultrapassa a forma.</span><span class="sxs-lookup"><span data-stu-id="b9909-110">Defines how far the shadow extends past the shape.</span></span> <span data-ttu-id="b9909-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b9909-111">Read/write.</span></span> <span data-ttu-id="b9909-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="b9909-112">**VgVector2D**.</span></span>

<span data-ttu-id="b9909-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="b9909-113">**Applies To**</span></span>

[<span data-ttu-id="b9909-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="b9909-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="b9909-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="b9909-115">**Tag Syntax**</span></span>

<span data-ttu-id="b9909-116"><v: *elemento* offset = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="b9909-116"><v: *element* offset=" *expression* "></span></span>

<span data-ttu-id="b9909-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="b9909-117">**Script Syntax**</span></span>

<span data-ttu-id="b9909-118">*elemento* . Offset = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="b9909-118">*element* .offset="*expression*"</span></span>

<span data-ttu-id="b9909-119">*expressão* = de *elemento*. Offset</span><span class="sxs-lookup"><span data-stu-id="b9909-119">*expression*=*element*.offset</span></span>

<span data-ttu-id="b9909-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="b9909-120">**Remarks**</span></span>

<span data-ttu-id="b9909-121">O deslocamento padrão para o valor x é 2PT e o padrão para o valor y é 2PT.</span><span class="sxs-lookup"><span data-stu-id="b9909-121">The default offset for the x value is 2pt and the default for the y value is 2pt.</span></span> <span data-ttu-id="b9909-122">Os valores são uma medida absoluta ou um valor fracionário de Shape.</span><span class="sxs-lookup"><span data-stu-id="b9909-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="b9909-123">Se houver frações, elas vão de 50% a-50%.</span><span class="sxs-lookup"><span data-stu-id="b9909-123">If fractional, they range from 50% to -50%.</span></span>

<span data-ttu-id="b9909-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="b9909-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="b9909-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="b9909-125">**Example**</span></span>

<span data-ttu-id="b9909-126">A forma tem uma sombra com um deslocamento de 5 pontos para baixo e 10 pontos à direita.</span><span class="sxs-lookup"><span data-stu-id="b9909-126">The shape has a shadow with an offset of 5 points down and 10 points to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 