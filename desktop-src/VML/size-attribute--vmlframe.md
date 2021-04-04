---
title: Atributo size (VMLFrame)
description: Atributo size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007612"
---
# <a name="size-attribute-vmlframe"></a><span data-ttu-id="cdb16-103">Atributo size (VMLFrame)</span><span class="sxs-lookup"><span data-stu-id="cdb16-103">Size Attribute (VMLFrame)</span></span>

<span data-ttu-id="cdb16-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cdb16-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cdb16-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="cdb16-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cdb16-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="cdb16-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cdb16-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="cdb16-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cdb16-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cdb16-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cdb16-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cdb16-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cdb16-110">Define o tamanho da região de recorte do quadro.</span><span class="sxs-lookup"><span data-stu-id="cdb16-110">Defines the size of the clipping region of the frame.</span></span> <span data-ttu-id="cdb16-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cdb16-111">Read/write.</span></span> <span data-ttu-id="cdb16-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="cdb16-112">**VgVector2D**.</span></span>

<span data-ttu-id="cdb16-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="cdb16-113">**Applies To**</span></span>

[<span data-ttu-id="cdb16-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="cdb16-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="cdb16-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="cdb16-115">**Tag Syntax**</span></span>

<span data-ttu-id="cdb16-116"><v: *Element* tamanho = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="cdb16-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="cdb16-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="cdb16-117">**Script Syntax**</span></span>

<span data-ttu-id="cdb16-118">*elemento* . Size = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="cdb16-118">*element* .size="*expression*"</span></span>

<span data-ttu-id="cdb16-119">*expressão* = de *elemento*. Size</span><span class="sxs-lookup"><span data-stu-id="cdb16-119">*expression*=*element*.size</span></span>

<span data-ttu-id="cdb16-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="cdb16-120">**Remarks**</span></span>

<span data-ttu-id="cdb16-121">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="cdb16-121">The default value is 0,0.</span></span> <span data-ttu-id="cdb16-122">Observe que o **tamanho** funciona apenas se o [clipe](msdn-online-vml-clip-attribute.md) for **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="cdb16-122">Note that **Size** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="cdb16-123">Nesse atributo, o tamanho é definido como a largura e a altura do quadro.</span><span class="sxs-lookup"><span data-stu-id="cdb16-123">In this attribute, the size is defined as the width and height of the frame.</span></span>

<span data-ttu-id="cdb16-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="cdb16-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="cdb16-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="cdb16-125">**Example**</span></span>

<span data-ttu-id="cdb16-126">O tamanho da região de recorte será 50pt, 50pt.</span><span class="sxs-lookup"><span data-stu-id="cdb16-126">The size of the clipping region will be 50pt, 50pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 