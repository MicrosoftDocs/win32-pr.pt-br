---
title: Atributo de tamanho (Fill) (VML)
description: Atributo de tamanho (Fill) (VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917367"
---
# <a name="size-attribute-fillvml"></a><span data-ttu-id="32c38-103">Atributo de tamanho (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="32c38-103">Size Attribute (Fill)(VML)</span></span>

<span data-ttu-id="32c38-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="32c38-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="32c38-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="32c38-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="32c38-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="32c38-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="32c38-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="32c38-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="32c38-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="32c38-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="32c38-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="32c38-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="32c38-110">Define o tamanho da imagem para o preenchimento.</span><span class="sxs-lookup"><span data-stu-id="32c38-110">Defines the size of the image for the fill.</span></span> <span data-ttu-id="32c38-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="32c38-111">Read/write.</span></span> <span data-ttu-id="32c38-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="32c38-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="32c38-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="32c38-113">**Applies To**</span></span>

[<span data-ttu-id="32c38-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="32c38-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="32c38-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="32c38-115">**Tag Syntax**</span></span>

<span data-ttu-id="32c38-116"><v: *Element* tamanho = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="32c38-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="32c38-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="32c38-117">**Script Syntax**</span></span>

<span data-ttu-id="32c38-118">*elemento* . Size = "*expressão \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="32c38-118">*element* .size="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="32c38-119">*expressão* = de *elemento*. Size</span><span class="sxs-lookup"><span data-stu-id="32c38-119">*expression*=*element*.size</span></span>

<span data-ttu-id="32c38-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="32c38-120">**Remarks**</span></span>

<span data-ttu-id="32c38-121">O padrão é o tamanho da imagem original.</span><span class="sxs-lookup"><span data-stu-id="32c38-121">The default is the size of the original image.</span></span> <span data-ttu-id="32c38-122">Os tamanhos maiores que o shapewill exibem uma versão ampliada, mas recortada da imagem.</span><span class="sxs-lookup"><span data-stu-id="32c38-122">Sizes that are larger than the shapewill display a magnified but clipped version of the image.</span></span>

<span data-ttu-id="32c38-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="32c38-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="32c38-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="32c38-124">**Example**</span></span>

<span data-ttu-id="32c38-125">Embora o tamanho original da imagem seja de 50 a 50 pontos, a imagem será exibida como uma imagem de 10 por 10 no centro do preenchimento.</span><span class="sxs-lookup"><span data-stu-id="32c38-125">Even though the original size of the image is 50-by-50 points, the image will be displayed as a 10-by-10 image in the center of the fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 