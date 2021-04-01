---
title: Atributo WrapCoords de VML
description: Atributo WrapCoords de VML
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641265"
---
# <a name="vml-wrapcoords-attribute"></a><span data-ttu-id="ada2f-103">Atributo WrapCoords de VML</span><span class="sxs-lookup"><span data-stu-id="ada2f-103">VML WrapCoords Attribute</span></span>

<span data-ttu-id="ada2f-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ada2f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ada2f-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="ada2f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ada2f-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="ada2f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ada2f-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="ada2f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ada2f-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ada2f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ada2f-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ada2f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ada2f-110">Define o polígono delimitador que circunda uma forma.</span><span class="sxs-lookup"><span data-stu-id="ada2f-110">Defines the bounding polygon that surrounds a shape.</span></span> <span data-ttu-id="ada2f-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ada2f-111">Read/write.</span></span> <span data-ttu-id="ada2f-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="ada2f-112">**String**.</span></span>

<span data-ttu-id="ada2f-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="ada2f-113">**Applies To**</span></span>

[<span data-ttu-id="ada2f-114">Forma</span><span class="sxs-lookup"><span data-stu-id="ada2f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ada2f-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="ada2f-115">**Tag Syntax**</span></span>

<span data-ttu-id="ada2f-116"><v: *Element* o:wrapcoords = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="ada2f-116"><v: *element* o:wrapcoords=" *expression* "></span></span>

<span data-ttu-id="ada2f-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="ada2f-117">**Remarks**</span></span>

<span data-ttu-id="ada2f-118">Descreve uma lista delimitada por vírgulas de x e ycoordinates; ou seja, "x1, y1, X2, Y2, X3, Y3,..." Isso é usado quando o texto é rigidamente disposto em torno de uma forma.</span><span class="sxs-lookup"><span data-stu-id="ada2f-118">Describes a comma-delimited list of x and ycoordinates; that is, "x1,y1,x2,y2,x3,y3,..." This is used when text is tightly wrapped around a shape.</span></span> <span data-ttu-id="ada2f-119">O padrão é **NULL** (uma cadeia de caracteres vazia) até que o atributo **mso-Wrap-Mode** seja definido como **apertado** ou **até**.</span><span class="sxs-lookup"><span data-stu-id="ada2f-119">The default is **NULL** (an empty string) until the **MSO-Wrap-Mode** attribute is set to **tight** or **through**.</span></span>

<span data-ttu-id="ada2f-120">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="ada2f-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="ada2f-121">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="ada2f-121">**Example**</span></span>

<span data-ttu-id="ada2f-122">A forma tem uma caixa delimitadora de texto que é de 5 unidades maior do que o caminho.</span><span class="sxs-lookup"><span data-stu-id="ada2f-122">The shape has a text wrap bounding box that is 5 units larger than the path.</span></span>


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 