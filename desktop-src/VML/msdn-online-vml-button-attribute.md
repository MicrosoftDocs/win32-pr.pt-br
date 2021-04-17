---
title: Atributo do botão VML
description: Atributo do botão VML
ms.assetid: 273024ac-683f-48d2-b6a0-574824f4c05d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2760fceaf52e3f9ee217d4c3d249fb670a845f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105782288"
---
# <a name="vml-button-attribute"></a><span data-ttu-id="417f5-103">Atributo do botão VML</span><span class="sxs-lookup"><span data-stu-id="417f5-103">VML Button Attribute</span></span>

<span data-ttu-id="417f5-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="417f5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="417f5-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="417f5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="417f5-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="417f5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="417f5-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="417f5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="417f5-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="417f5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="417f5-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="417f5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="417f5-110">Determina se uma forma será processada como um botão.</span><span class="sxs-lookup"><span data-stu-id="417f5-110">Determines whether a shape will be processed as a button.</span></span> <span data-ttu-id="417f5-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="417f5-111">Read/write.</span></span> <span data-ttu-id="417f5-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="417f5-112">**VgTriState**.</span></span>

<span data-ttu-id="417f5-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="417f5-113">**Applies To**</span></span>

[<span data-ttu-id="417f5-114">Forma</span><span class="sxs-lookup"><span data-stu-id="417f5-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="417f5-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="417f5-115">**Tag Syntax**</span></span>

<span data-ttu-id="417f5-116"><v: *Element* o:Button = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="417f5-116"><v: *element* o:button=" *expression* "></span></span>

<span data-ttu-id="417f5-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="417f5-117">**Remarks**</span></span>

<span data-ttu-id="417f5-118">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="417f5-118">The default is **False**.</span></span> <span data-ttu-id="417f5-119">Se **for true**, a forma será processada como um botão.</span><span class="sxs-lookup"><span data-stu-id="417f5-119">If **True**, the shape is processed as a button.</span></span>

<span data-ttu-id="417f5-120">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="417f5-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="417f5-121">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="417f5-121">**Example**</span></span>

<span data-ttu-id="417f5-122">A forma é um botão.</span><span class="sxs-lookup"><span data-stu-id="417f5-122">The shape is a button.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:button="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 