---
title: Atributo BWPure de VML
description: Atributo BWPure de VML
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e39c658265a5ab8c617fc8856db362a80d1ea8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823843"
---
# <a name="vml-bwpure-attribute"></a><span data-ttu-id="184e9-103">Atributo BWPure de VML</span><span class="sxs-lookup"><span data-stu-id="184e9-103">VML BWPure Attribute</span></span>

<span data-ttu-id="184e9-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="184e9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="184e9-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="184e9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="184e9-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="184e9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="184e9-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="184e9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="184e9-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="184e9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="184e9-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="184e9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="184e9-110">Define o modo preto e branco para dispositivos de saída puros preto e branco.</span><span class="sxs-lookup"><span data-stu-id="184e9-110">Defines the black-and-white mode for pure black-and-white output devices.</span></span> <span data-ttu-id="184e9-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="184e9-111">Read/write.</span></span> <span data-ttu-id="184e9-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="184e9-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="184e9-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="184e9-113">**Applies To**</span></span>

[<span data-ttu-id="184e9-114">Forma</span><span class="sxs-lookup"><span data-stu-id="184e9-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="184e9-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="184e9-115">**Tag Syntax**</span></span>

<span data-ttu-id="184e9-116"><v: *Element* o:bwpure = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="184e9-116"><v: *element* o:bwpure=" *expression* "></span></span>

<span data-ttu-id="184e9-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="184e9-117">**Remarks**</span></span>

<span data-ttu-id="184e9-118">Quando [BWMode](msdn-online-vml-bwmode-attribute.md) é definido como **auto**, esse atributo é usado para determinar como renderizar a forma em preto e branco puro.</span><span class="sxs-lookup"><span data-stu-id="184e9-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in pure black and white.</span></span>

<span data-ttu-id="184e9-119">Para obter mais informações sobre os valores desse atributo, consulte o tópico [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="184e9-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="184e9-120">O padrão é **auto**.</span><span class="sxs-lookup"><span data-stu-id="184e9-120">The default is **auto**.</span></span>

<span data-ttu-id="184e9-121">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="184e9-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="184e9-122">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="184e9-122">**Example**</span></span>

<span data-ttu-id="184e9-123">A forma é processada como uma imagem de alto contraste para saída puro de preto e branco.</span><span class="sxs-lookup"><span data-stu-id="184e9-123">The shape is processed as a high contrast image for pure black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 