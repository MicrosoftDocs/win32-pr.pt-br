---
title: Atributo CropBottom de VML
description: Atributo CropBottom de VML
ms.assetid: 9548d0fa-1708-4206-90d8-1d90cb42de87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b847fcd061e13418efe04b6ea27795a19002abf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294123"
---
# <a name="vml-cropbottom-attribute"></a><span data-ttu-id="d7a5d-103">Atributo CropBottom de VML</span><span class="sxs-lookup"><span data-stu-id="d7a5d-103">VML CropBottom Attribute</span></span>

<span data-ttu-id="d7a5d-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d7a5d-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d7a5d-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d7a5d-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d7a5d-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d7a5d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d7a5d-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d7a5d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d7a5d-110">Define a porcentagem de remoção de imagem do lado inferior.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-110">Defines the percentage of picture removal from the bottom side.</span></span> <span data-ttu-id="d7a5d-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-111">Read/write.</span></span> <span data-ttu-id="d7a5d-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-112">**VgNumber**.</span></span>

<span data-ttu-id="d7a5d-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="d7a5d-113">**Applies To**</span></span>

[<span data-ttu-id="d7a5d-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="d7a5d-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="d7a5d-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="d7a5d-115">**Tag Syntax**</span></span>

<span data-ttu-id="d7a5d-116"><v: *Element* cropbottom = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="d7a5d-116"><v: *element* cropbottom=" *expression* "></span></span>

<span data-ttu-id="d7a5d-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="d7a5d-117">**Script Syntax**</span></span>

<span data-ttu-id="d7a5d-118">*Element* . cropbottom = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="d7a5d-118">*element* .cropbottom="*expression*"</span></span>

<span data-ttu-id="d7a5d-119">*expressão* = de *elemento*. cropbottom</span><span class="sxs-lookup"><span data-stu-id="d7a5d-119">*expression*=*element*.cropbottom</span></span>

<span data-ttu-id="d7a5d-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="d7a5d-120">**Remarks**</span></span>

<span data-ttu-id="d7a5d-121">A quantidade de corte pode variar de-1,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="d7a5d-122">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-122">The default value is 0.</span></span> <span data-ttu-id="d7a5d-123">Observe que um valor de 1 não exibirá nenhuma imagem.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="d7a5d-124">Valores negativos resultarão na imagem que está sendo descompactada da borda que está sendo cortada (o espaço vazio entre a imagem e a borda cortada será preenchido pela cor de preenchimento da forma).</span><span class="sxs-lookup"><span data-stu-id="d7a5d-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="d7a5d-125">Valores positivos menores que 1 resultarão na imagem restante sendo ampliada para se ajustar à forma.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="d7a5d-126">Atributo padrão da VML</span><span class="sxs-lookup"><span data-stu-id="d7a5d-126">VML Standard Attribute</span></span>

<span data-ttu-id="d7a5d-127">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="d7a5d-127">**Example**</span></span>

<span data-ttu-id="d7a5d-128">Nenhuma imagem será exibida porque a imagem é 100% cortada da parte inferior.</span><span class="sxs-lookup"><span data-stu-id="d7a5d-128">No image will be displayed because the image is 100% cropped from the bottom.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropbottom="1" src="kids.jpg"/>
   </v:shape>
```



 

 