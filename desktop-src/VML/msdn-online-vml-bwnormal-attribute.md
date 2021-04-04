---
title: Atributo BWNormal de VML
description: Atributo BWNormal de VML
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2fd14a50fc28c47154611b9a996fe0ef035f70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007756"
---
# <a name="vml-bwnormal-attribute"></a><span data-ttu-id="c15ba-103">Atributo BWNormal de VML</span><span class="sxs-lookup"><span data-stu-id="c15ba-103">VML BWNormal Attribute</span></span>

<span data-ttu-id="c15ba-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c15ba-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c15ba-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="c15ba-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c15ba-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="c15ba-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c15ba-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="c15ba-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c15ba-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c15ba-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c15ba-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c15ba-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c15ba-110">Define o modo preto e branco para dispositivos normais de saída em preto e branco.</span><span class="sxs-lookup"><span data-stu-id="c15ba-110">Defines the black-and-white mode for normal black-and-white output devices.</span></span> <span data-ttu-id="c15ba-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c15ba-111">Read/write.</span></span> <span data-ttu-id="c15ba-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="c15ba-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="c15ba-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="c15ba-113">**Applies To**</span></span>

[<span data-ttu-id="c15ba-114">Forma</span><span class="sxs-lookup"><span data-stu-id="c15ba-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c15ba-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="c15ba-115">**Tag Syntax**</span></span>

<span data-ttu-id="c15ba-116"><v: *Element* o:bwnormal = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="c15ba-116"><v: *element* o:bwnormal=" *expression* "></span></span>

<span data-ttu-id="c15ba-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="c15ba-117">**Remarks**</span></span>

<span data-ttu-id="c15ba-118">Quando [BWMode](msdn-online-vml-bwmode-attribute.md) é definido como **auto**, esse atributo é usado para determinar como renderizar a forma em preto e branco normal.</span><span class="sxs-lookup"><span data-stu-id="c15ba-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in normal black and white.</span></span>

<span data-ttu-id="c15ba-119">Para obter mais informações sobre os valores desse atributo, consulte o tópico [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="c15ba-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="c15ba-120">O valor padrão é **auto**.</span><span class="sxs-lookup"><span data-stu-id="c15ba-120">The default value is **auto**.</span></span>

<span data-ttu-id="c15ba-121">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="c15ba-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="c15ba-122">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="c15ba-122">**Example**</span></span>

<span data-ttu-id="c15ba-123">A forma é processada como uma imagem em escala de cinza para saída normal de preto e branco.</span><span class="sxs-lookup"><span data-stu-id="c15ba-123">The shape is processed as a grayscale image for normal black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 