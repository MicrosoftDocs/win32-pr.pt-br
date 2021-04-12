---
title: Atributo de escala de cinza da VML
description: Atributo de escala de cinza da VML
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366226"
---
# <a name="vml-grayscale-attribute"></a><span data-ttu-id="cbee0-103">Atributo de escala de cinza da VML</span><span class="sxs-lookup"><span data-stu-id="cbee0-103">VML GrayScale Attribute</span></span>

<span data-ttu-id="cbee0-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cbee0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cbee0-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="cbee0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cbee0-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="cbee0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cbee0-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="cbee0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cbee0-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cbee0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cbee0-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cbee0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cbee0-110">Determina se uma imagem será exibida no modo de escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="cbee0-110">Determines whether a picture will be displayed in grayscale mode.</span></span> <span data-ttu-id="cbee0-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cbee0-111">Read/write.</span></span> <span data-ttu-id="cbee0-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="cbee0-112">**VgTriState**.</span></span>

<span data-ttu-id="cbee0-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="cbee0-113">**Applies To**</span></span>

[<span data-ttu-id="cbee0-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="cbee0-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="cbee0-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="cbee0-115">**Tag Syntax**</span></span>

<span data-ttu-id="cbee0-116"><v: *Element* tons de cinza = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="cbee0-116"><v: *element* grayscale=" *expression* "></span></span>

<span data-ttu-id="cbee0-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="cbee0-117">**Script Syntax**</span></span>

<span data-ttu-id="cbee0-118">*elemento* . escala de cinza = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="cbee0-118">*element* .grayscale="*expression*"</span></span>

<span data-ttu-id="cbee0-119">*expressão* = de *elemento*. escala de cinza</span><span class="sxs-lookup"><span data-stu-id="cbee0-119">*expression*=*element*.grayscale</span></span>

<span data-ttu-id="cbee0-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="cbee0-120">**Remarks**</span></span>

<span data-ttu-id="cbee0-121">Se **for true**, a imagem será exibida em escala de cinza em vez de cor.</span><span class="sxs-lookup"><span data-stu-id="cbee0-121">If **True**, the picture will be displayed in grayscale instead of color.</span></span> <span data-ttu-id="cbee0-122">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="cbee0-122">The default is **False**.</span></span>

<span data-ttu-id="cbee0-123">O valor é baseado de acordo com a recomendação de CCIR 709, que favorece mais o peso verde e produz resultados mais agradáveis para a cor natural.</span><span class="sxs-lookup"><span data-stu-id="cbee0-123">The value is based according to CCIR recommendation 709, which favors more green weight and produces more pleasing results for natural color.</span></span>

<span data-ttu-id="cbee0-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="cbee0-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="cbee0-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="cbee0-125">**Example**</span></span>

<span data-ttu-id="cbee0-126">A imagem será exibida em escala de cinza em vez de cor.</span><span class="sxs-lookup"><span data-stu-id="cbee0-126">The image will be displayed in grayscale instead of color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 