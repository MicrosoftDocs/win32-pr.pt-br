---
title: Atributo AltHRef (Stroke) (VML)
description: Atributo AltHRef (Stroke) (VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021e89e87f70910561e55406e282920cdbed2963
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810654"
---
# <a name="althref-attribute-strokevml"></a><span data-ttu-id="785a5-103">Atributo AltHRef (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="785a5-103">AltHRef Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="785a5-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="785a5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="785a5-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="785a5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="785a5-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="785a5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="785a5-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="785a5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="785a5-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="785a5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="785a5-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="785a5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="785a5-110">Especifica uma referência alternativa para uma imagem.</span><span class="sxs-lookup"><span data-stu-id="785a5-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="785a5-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="785a5-111">Read/write.</span></span> <span data-ttu-id="785a5-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="785a5-112">**String**.</span></span>

<span data-ttu-id="785a5-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="785a5-113">**Applies To**</span></span>

[<span data-ttu-id="785a5-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="785a5-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="785a5-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="785a5-115">**Tag Syntax**</span></span>

<span data-ttu-id="785a5-116"><v: *Element* o:althref = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="785a5-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="785a5-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="785a5-117">**Script Syntax**</span></span>

<span data-ttu-id="785a5-118">*Element* . althref = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="785a5-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="785a5-119">*expressão* = de *elemento*. althref</span><span class="sxs-lookup"><span data-stu-id="785a5-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="785a5-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="785a5-120">**Remarks**</span></span>

<span data-ttu-id="785a5-121">Dá suporte à preservação de dados PICT por meio de roundtripping HTML.</span><span class="sxs-lookup"><span data-stu-id="785a5-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="785a5-122">Na gravação em HTML, a representação alternativa (ou seja, os dados originais do PICT, se o arquivo foi originado do Macintosh) é salvo.</span><span class="sxs-lookup"><span data-stu-id="785a5-122">On HTML write, the alternate representation (i.e., the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="785a5-123">Em HTML Read, **AltHRef** é favorecedo sobre **src**.</span><span class="sxs-lookup"><span data-stu-id="785a5-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="785a5-124">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="785a5-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="785a5-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="785a5-125">**Example**</span></span>

<span data-ttu-id="785a5-126">O traço da forma tem um **AltHRef** que aponta para um arquivo chamado myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="785a5-126">The stroke of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 