---
title: Atributo AlignShape de VML
description: Atributo AlignShape de VML
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294448"
---
# <a name="vml-alignshape-attribute"></a><span data-ttu-id="1d4de-103">Atributo AlignShape de VML</span><span class="sxs-lookup"><span data-stu-id="1d4de-103">VML AlignShape Attribute</span></span>

<span data-ttu-id="1d4de-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1d4de-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1d4de-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="1d4de-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1d4de-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="1d4de-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1d4de-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="1d4de-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1d4de-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1d4de-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1d4de-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1d4de-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1d4de-110">Determina se uma imagem será alinhada com uma forma.</span><span class="sxs-lookup"><span data-stu-id="1d4de-110">Determines whether an image will align with a shape.</span></span> <span data-ttu-id="1d4de-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1d4de-111">Read/write.</span></span> <span data-ttu-id="1d4de-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="1d4de-112">**VgTriState**.</span></span>

<span data-ttu-id="1d4de-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="1d4de-113">**Applies To**</span></span>

[<span data-ttu-id="1d4de-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="1d4de-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="1d4de-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="1d4de-115">**Tag Syntax**</span></span>

<span data-ttu-id="1d4de-116"><v: *Element* alignshape = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="1d4de-116"><v: *element* alignshape=" *expression* "></span></span>

<span data-ttu-id="1d4de-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="1d4de-117">**Script Syntax**</span></span>

<span data-ttu-id="1d4de-118">*Element* . alignshape = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="1d4de-118">*element* .alignshape="*expression*"</span></span>

<span data-ttu-id="1d4de-119">*expressão* = de *elemento*. alignshape</span><span class="sxs-lookup"><span data-stu-id="1d4de-119">*expression*=*element*.alignshape</span></span>

<span data-ttu-id="1d4de-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="1d4de-120">**Remarks**</span></span>

<span data-ttu-id="1d4de-121">Se **for true**, a imagem usada para criar o preenchimento será alinhada com a forma.</span><span class="sxs-lookup"><span data-stu-id="1d4de-121">If **True**, the image used to create the fill is aligned with the shape.</span></span> <span data-ttu-id="1d4de-122">Se **for false**, a imagem usada para criar o preenchimento será alinhada com a janela.</span><span class="sxs-lookup"><span data-stu-id="1d4de-122">If **False**, the image used to create the fill is aligned with the window.</span></span> <span data-ttu-id="1d4de-123">O padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="1d4de-123">Default is **True**.</span></span>

<span data-ttu-id="1d4de-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="1d4de-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="1d4de-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="1d4de-125">**Example**</span></span>

<span data-ttu-id="1d4de-126">A imagem de preenchimento à direita criada a partir de myimage.gif é alinhada com a janela, não a forma; Embora a forma seja girada, a imagem não é.</span><span class="sxs-lookup"><span data-stu-id="1d4de-126">The tiled fill image created from myimage.gif is aligned with the window, not the shape; even though the shape is rotated, the image is not.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 