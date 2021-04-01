---
title: Atributo biníveis da VML
description: Atributo biníveis da VML
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263a9d538a76ba0c9b203cbcf04f8413d4286c34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641352"
---
# <a name="vml-bilevel-attribute"></a><span data-ttu-id="c97d5-103">Atributo biníveis da VML</span><span class="sxs-lookup"><span data-stu-id="c97d5-103">VML Bilevel Attribute</span></span>

<span data-ttu-id="c97d5-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c97d5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c97d5-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="c97d5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c97d5-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="c97d5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c97d5-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="c97d5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c97d5-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c97d5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c97d5-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c97d5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c97d5-110">Determina se uma imagem será exibida em preto e branco.</span><span class="sxs-lookup"><span data-stu-id="c97d5-110">Determines whether an image will be displayed in black and white.</span></span> <span data-ttu-id="c97d5-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c97d5-111">Read/write.</span></span> <span data-ttu-id="c97d5-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="c97d5-112">**VgTriState**.</span></span>

<span data-ttu-id="c97d5-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="c97d5-113">**Applies To**</span></span>

[<span data-ttu-id="c97d5-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="c97d5-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="c97d5-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="c97d5-115">**Tag Syntax**</span></span>

<span data-ttu-id="c97d5-116"><v: *Element* bilevement = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c97d5-116"><v: *element* bilevel=" *expression* "></span></span>

<span data-ttu-id="c97d5-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="c97d5-117">**Script Syntax**</span></span>

<span data-ttu-id="c97d5-118">*elemento* . bilevel = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="c97d5-118">*element* .bilevel="*expression*"</span></span>

<span data-ttu-id="c97d5-119">*expressão* = de *elemento*. binível</span><span class="sxs-lookup"><span data-stu-id="c97d5-119">*expression*=*element*.bilevel</span></span>

<span data-ttu-id="c97d5-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="c97d5-120">**Remarks**</span></span>

<span data-ttu-id="c97d5-121">Se **for true**, a imagem será exibida usando duas cores (preto e branco).</span><span class="sxs-lookup"><span data-stu-id="c97d5-121">If **True**, the image will be displayed using two colors (black and white).</span></span> <span data-ttu-id="c97d5-122">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="c97d5-122">The default is **False**.</span></span> <span data-ttu-id="c97d5-123">Isso cria um efeito semelhante à Posterização.</span><span class="sxs-lookup"><span data-stu-id="c97d5-123">This creates an effect similar to posterization.</span></span>

<span data-ttu-id="c97d5-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="c97d5-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="c97d5-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="c97d5-125">**Example**</span></span>

<span data-ttu-id="c97d5-126">A imagem será exibida somente em preto e branco.</span><span class="sxs-lookup"><span data-stu-id="c97d5-126">The image will be displayed in black and white only.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 