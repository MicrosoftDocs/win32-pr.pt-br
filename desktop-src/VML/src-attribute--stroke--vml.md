---
title: Atributo src (Stroke) (VML)
description: Atributo src (Stroke) (VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641160"
---
# <a name="src-attribute-strokevml"></a><span data-ttu-id="9edce-103">Atributo src (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="9edce-103">Src Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="9edce-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9edce-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9edce-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="9edce-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9edce-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="9edce-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9edce-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="9edce-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9edce-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9edce-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9edce-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9edce-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9edce-110">Define a imagem de origem a ser carregada para um preenchimento de traço.</span><span class="sxs-lookup"><span data-stu-id="9edce-110">Defines the source image to load for a stroke fill.</span></span> <span data-ttu-id="9edce-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9edce-111">Read/write.</span></span> <span data-ttu-id="9edce-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9edce-112">**String**.</span></span>

<span data-ttu-id="9edce-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="9edce-113">**Applies To**</span></span>

[<span data-ttu-id="9edce-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="9edce-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="9edce-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="9edce-115">**Tag Syntax**</span></span>

<span data-ttu-id="9edce-116"><v: *Element* src = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="9edce-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="9edce-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="9edce-117">**Script Syntax**</span></span>

<span data-ttu-id="9edce-118">*Element* . src = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="9edce-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="9edce-119">*expressão* = de *elemento*. src</span><span class="sxs-lookup"><span data-stu-id="9edce-119">*expression*=*element*.src</span></span>

<span data-ttu-id="9edce-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="9edce-120">**Remarks**</span></span>

<span data-ttu-id="9edce-121">URL para uma imagem a ser carregada para preenchimentos de imagem e padrão.</span><span class="sxs-lookup"><span data-stu-id="9edce-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="9edce-122">Esse atributo sempre deve estar presente e apontar para dados de imagem válidos para que uma imagem apareça.</span><span class="sxs-lookup"><span data-stu-id="9edce-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="9edce-123">Se esse atributo aparecer sozinho, ou seja, não **href** ou **title**, a imagem será vinculada.</span><span class="sxs-lookup"><span data-stu-id="9edce-123">If this attribute appears alone, that is, no **HRef** or **Title**, then the image is linked.</span></span>

<span data-ttu-id="9edce-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="9edce-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="9edce-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="9edce-125">**Example**</span></span>

<span data-ttu-id="9edce-126">O traço é criado com a imagem especificada pelo arquivo de cylinder.gif.</span><span class="sxs-lookup"><span data-stu-id="9edce-126">The stroke is created with the image specified by the cylinder.gif file.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 