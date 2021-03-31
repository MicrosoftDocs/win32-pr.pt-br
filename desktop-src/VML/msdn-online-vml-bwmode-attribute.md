---
title: Atributo BWMode de VML
description: Atributo BWMode de VML
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641348"
---
# <a name="vml-bwmode-attribute"></a><span data-ttu-id="02bcd-103">Atributo BWMode de VML</span><span class="sxs-lookup"><span data-stu-id="02bcd-103">VML BWMode Attribute</span></span>

<span data-ttu-id="02bcd-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="02bcd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="02bcd-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="02bcd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="02bcd-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="02bcd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="02bcd-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="02bcd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="02bcd-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="02bcd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="02bcd-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="02bcd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="02bcd-110">Determina como uma forma será renderizada para dispositivos de saída em preto e branco.</span><span class="sxs-lookup"><span data-stu-id="02bcd-110">Determines how a shape will render for black-and-white output devices.</span></span> <span data-ttu-id="02bcd-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="02bcd-111">Read/write.</span></span> <span data-ttu-id="02bcd-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="02bcd-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="02bcd-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="02bcd-113">**Applies To**</span></span>

[<span data-ttu-id="02bcd-114">Forma</span><span class="sxs-lookup"><span data-stu-id="02bcd-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="02bcd-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="02bcd-115">**Tag Syntax**</span></span>

<span data-ttu-id="02bcd-116"><v: *Element* o:bwmode = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="02bcd-116"><v: *element* o:bwmode=" *expression* "></span></span>

<span data-ttu-id="02bcd-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="02bcd-117">**Remarks**</span></span>

<span data-ttu-id="02bcd-118">Quando uma forma é impressa em uma impressora preto e branco ou exibida em uma exibição em preto e branco em um aplicativo, várias opções são possíveis.</span><span class="sxs-lookup"><span data-stu-id="02bcd-118">When a shape is printed on a black-and-white printer or displayed in a black-and-white view in an application, several options are possible.</span></span> <span data-ttu-id="02bcd-119">Para obter mais informações sobre os valores desse atributo, consulte o tópico [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="02bcd-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="02bcd-120">O valor padrão é **auto**.</span><span class="sxs-lookup"><span data-stu-id="02bcd-120">The default value is **auto**.</span></span>

<span data-ttu-id="02bcd-121">Se **auto** for especificado, [BWNormal](msdn-online-vml-bwnormal-attribute.md) será usado para determinar o comportamento para saída normal de preto e branco, e [BWPure](msdn-online-vml-bwpure-attribute.md) será usado para determinar o comportamento de saída puro de preto e branco.</span><span class="sxs-lookup"><span data-stu-id="02bcd-121">If **auto** is specified, [BWNormal](msdn-online-vml-bwnormal-attribute.md) is used to determine the behavior for normal black-and-white output, and [BWPure](msdn-online-vml-bwpure-attribute.md) is used to determine the behavior for pure black-and-white output.</span></span>

<span data-ttu-id="02bcd-122">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="02bcd-122">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="02bcd-123">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="02bcd-123">**Example**</span></span>

<span data-ttu-id="02bcd-124">O modo preto e branco da forma é **automático**.</span><span class="sxs-lookup"><span data-stu-id="02bcd-124">The black-and-white mode of the shape is **auto**.</span></span>


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 