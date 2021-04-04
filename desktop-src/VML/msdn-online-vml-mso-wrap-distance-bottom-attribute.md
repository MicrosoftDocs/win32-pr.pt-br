---
title: Atributo VML MSO-Wrap-Distance-Bottom
description: Atributo VML MSO-Wrap-Distance-Bottom
ms.assetid: b096fc67-dd99-4833-bb82-73de7b06f43c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c3ec66ae23994184227d857e269318606d9ea4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917464"
---
# <a name="vml-mso-wrap-distance-bottom-attribute"></a><span data-ttu-id="c5187-103">Atributo VML MSO-Wrap-Distance-Bottom</span><span class="sxs-lookup"><span data-stu-id="c5187-103">VML MSO-Wrap-Distance-Bottom Attribute</span></span>

<span data-ttu-id="c5187-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c5187-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c5187-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="c5187-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c5187-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="c5187-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c5187-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="c5187-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c5187-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c5187-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c5187-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c5187-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c5187-110">Define a distância do lado inferior da forma com o texto que é quebrado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="c5187-110">Defines the distance from the bottom side of the shape to the text that wraps around it.</span></span> <span data-ttu-id="c5187-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c5187-111">Read/write.</span></span> <span data-ttu-id="c5187-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="c5187-112">**String**.</span></span>

<span data-ttu-id="c5187-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="c5187-113">**Applies To**</span></span>

[<span data-ttu-id="c5187-114">Forma</span><span class="sxs-lookup"><span data-stu-id="c5187-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c5187-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="c5187-115">**Tag Syntax**</span></span>

<span data-ttu-id="c5187-116"><v: *elemento* Style = "Die-Wrap-Distance-bottom: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c5187-116"><v: *element* style="mso-wrap-distance-bottom: *expression* "></span></span>

<span data-ttu-id="c5187-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="c5187-117">**Remarks**</span></span>

<span data-ttu-id="c5187-118">Observe que esse atributo é diferente do atributo de **margem** CSS.</span><span class="sxs-lookup"><span data-stu-id="c5187-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="c5187-119">**Margin** altera a origem da forma para incluir as áreas de margem, mas a distância de encapsulamento em Microsoft Office não altera a origem da forma.</span><span class="sxs-lookup"><span data-stu-id="c5187-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="c5187-120">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="c5187-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="c5187-121">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="c5187-121">**Example**</span></span>

<span data-ttu-id="c5187-122">A forma tem uma distância de quebra inferior de 10 pontos.</span><span class="sxs-lookup"><span data-stu-id="c5187-122">The shape has a bottom wrap distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-bottom:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 