---
title: Atributo de CropTop da VML
description: Atributo de CropTop da VML
ms.assetid: b54939b6-0505-43b0-bf82-c3df82dc2633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8b2606c7ac5835caeecc145a885de48eaeaf8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294121"
---
# <a name="vml-croptop-attribute"></a><span data-ttu-id="bbcec-103">Atributo de CropTop da VML</span><span class="sxs-lookup"><span data-stu-id="bbcec-103">VML CropTop Attribute</span></span>

<span data-ttu-id="bbcec-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bbcec-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bbcec-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="bbcec-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bbcec-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="bbcec-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bbcec-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="bbcec-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bbcec-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bbcec-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bbcec-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bbcec-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bbcec-110">Define a porcentagem de remoção de imagem do lado superior.</span><span class="sxs-lookup"><span data-stu-id="bbcec-110">Defines the percentage of picture removal from the top side.</span></span> <span data-ttu-id="bbcec-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bbcec-111">Read/write.</span></span> <span data-ttu-id="bbcec-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="bbcec-112">**VgNumber**.</span></span>

<span data-ttu-id="bbcec-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="bbcec-113">**Applies To**</span></span>

[<span data-ttu-id="bbcec-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="bbcec-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="bbcec-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="bbcec-115">**Tag Syntax**</span></span>

<span data-ttu-id="bbcec-116"><v: *Element* croptop = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="bbcec-116"><v: *element* croptop=" *expression* "></span></span>

<span data-ttu-id="bbcec-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="bbcec-117">**Script Syntax**</span></span>

<span data-ttu-id="bbcec-118">*Element* . croptop = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="bbcec-118">*element* .croptop="*expression*"</span></span>

<span data-ttu-id="bbcec-119">*expressão* = de *elemento*. croptop</span><span class="sxs-lookup"><span data-stu-id="bbcec-119">*expression*=*element*.croptop</span></span>

<span data-ttu-id="bbcec-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="bbcec-120">**Remarks**</span></span>

<span data-ttu-id="bbcec-121">A quantidade de corte pode variar de-1,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="bbcec-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="bbcec-122">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="bbcec-122">The default value is 0.</span></span> <span data-ttu-id="bbcec-123">Observe que um valor de 1 não exibirá nenhuma imagem.</span><span class="sxs-lookup"><span data-stu-id="bbcec-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="bbcec-124">Valores negativos resultarão na imagem que está sendo descompactada da borda que está sendo cortada (o espaço vazio entre a imagem e a borda cortada será preenchido pela cor de preenchimento da forma).</span><span class="sxs-lookup"><span data-stu-id="bbcec-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="bbcec-125">Valores positivos menores que 1 resultarão na imagem restante sendo ampliada para se ajustar à forma.</span><span class="sxs-lookup"><span data-stu-id="bbcec-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="bbcec-126">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="bbcec-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="bbcec-127">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="bbcec-127">**Example**</span></span>

<span data-ttu-id="bbcec-128">A imagem será enpremida em um prata estreito na parte inferior da forma.</span><span class="sxs-lookup"><span data-stu-id="bbcec-128">The picture will be squeezed into a narrow sliver at the bottom of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata croptop="-.8" src="kids.jpg"/>
   </v:shape>
```





 

 