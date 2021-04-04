---
title: Atributo imagesização de VML
description: Atributo imagesização de VML
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ae01d3162fdff67f0385736e5f0450b14ed6115
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641296"
---
# <a name="vml-imagesize-attribute"></a><span data-ttu-id="5f7f7-103">Atributo imagesização de VML</span><span class="sxs-lookup"><span data-stu-id="5f7f7-103">VML ImageSize Attribute</span></span>

<span data-ttu-id="5f7f7-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5f7f7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5f7f7-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="5f7f7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5f7f7-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="5f7f7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5f7f7-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="5f7f7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5f7f7-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5f7f7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5f7f7-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5f7f7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5f7f7-110">Define o tamanho da imagem para o traço.</span><span class="sxs-lookup"><span data-stu-id="5f7f7-110">Defines the size of the image for the stroke.</span></span> <span data-ttu-id="5f7f7-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5f7f7-111">Read/write.</span></span> <span data-ttu-id="5f7f7-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="5f7f7-112">**VgVector2D**.</span></span>

<span data-ttu-id="5f7f7-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="5f7f7-113">**Applies To**</span></span>

[<span data-ttu-id="5f7f7-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="5f7f7-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="5f7f7-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="5f7f7-115">**Tag Syntax**</span></span>

<span data-ttu-id="5f7f7-116"><v: *Element* ImageSize = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="5f7f7-116"><v: *element* imagesize=" *expression* "></span></span>

<span data-ttu-id="5f7f7-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="5f7f7-117">**Script Syntax**</span></span>

<span data-ttu-id="5f7f7-118">*Element* . ImageSize = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="5f7f7-118">*element* .imagesize="*expression*"</span></span>

<span data-ttu-id="5f7f7-119">*expressão* = de *elemento*. ImageSize</span><span class="sxs-lookup"><span data-stu-id="5f7f7-119">*expression*=*element*.imagesize</span></span>

<span data-ttu-id="5f7f7-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="5f7f7-120">**Remarks**</span></span>

<span data-ttu-id="5f7f7-121">O padrão é o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="5f7f7-121">Default is the size of the image.</span></span>

<span data-ttu-id="5f7f7-122">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="5f7f7-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="5f7f7-123">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="5f7f7-123">**Example**</span></span>

<span data-ttu-id="5f7f7-124">A imagem de traço será de um tamanho de 10 a 10 pontos.</span><span class="sxs-lookup"><span data-stu-id="5f7f7-124">The stroke image will be a 10-by-10 point size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 