---
title: Atributo VML MSO-Wrap-urbano-Top
description: Atributo VML MSO-Wrap-urbano-Top
ms.assetid: 20444d16-fa84-4685-911c-288150c2674b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a16898733ead7bf3728d8f520888c8a05ef5fe6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105807165"
---
# <a name="vml-mso-wrap-distance-top-attribute"></a><span data-ttu-id="cf58f-103">Atributo VML MSO-Wrap-urbano-Top</span><span class="sxs-lookup"><span data-stu-id="cf58f-103">VML MSO-Wrap-Distance-Top Attribute</span></span>

<span data-ttu-id="cf58f-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cf58f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cf58f-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="cf58f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cf58f-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="cf58f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cf58f-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="cf58f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cf58f-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cf58f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cf58f-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cf58f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cf58f-110">Define a distância da forma superior ao texto que é quebrado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="cf58f-110">Defines the distance from the shape top to the text that wraps around it.</span></span> <span data-ttu-id="cf58f-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cf58f-111">Read/write.</span></span> <span data-ttu-id="cf58f-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="cf58f-112">**String**.</span></span>

<span data-ttu-id="cf58f-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="cf58f-113">**Applies To**</span></span>

[<span data-ttu-id="cf58f-114">Forma</span><span class="sxs-lookup"><span data-stu-id="cf58f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="cf58f-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="cf58f-115">**Tag Syntax**</span></span>

<span data-ttu-id="cf58f-116"><v: *Element* Style = "Die-Wrap-urbano-Top: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="cf58f-116"><v: *element* style="mso-wrap-distance-top: *expression* "></span></span>

<span data-ttu-id="cf58f-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="cf58f-117">**Remarks**</span></span>

<span data-ttu-id="cf58f-118">Observe que esse atributo é diferente do atributo de **margem** CSS.</span><span class="sxs-lookup"><span data-stu-id="cf58f-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="cf58f-119">**Margin** altera a origem da forma para incluir as áreas de margem, mas a distância de ajuste em Microsoft Office não altera a origem da forma.</span><span class="sxs-lookup"><span data-stu-id="cf58f-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap-distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="cf58f-120">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="cf58f-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="cf58f-121">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="cf58f-121">**Example**</span></span>

<span data-ttu-id="cf58f-122">A forma tem uma distância de ajuste superior de 10 pontos.</span><span class="sxs-lookup"><span data-stu-id="cf58f-122">The shape has a top wrap-distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 