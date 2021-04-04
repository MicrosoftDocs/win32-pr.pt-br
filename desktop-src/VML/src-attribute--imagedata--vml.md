---
title: Atributo src (ImageData) (VML)
description: Atributo src (ImageData) (VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007611"
---
# <a name="src-attribute-imagedatavml"></a><span data-ttu-id="7be76-103">Atributo src (ImageData) (VML)</span><span class="sxs-lookup"><span data-stu-id="7be76-103">Src Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="7be76-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7be76-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7be76-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="7be76-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7be76-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="7be76-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7be76-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="7be76-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7be76-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7be76-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7be76-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7be76-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7be76-110">Define uma origem para a imagem.</span><span class="sxs-lookup"><span data-stu-id="7be76-110">Defines a source for the image.</span></span> <span data-ttu-id="7be76-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7be76-111">Read/write.</span></span> <span data-ttu-id="7be76-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="7be76-112">**String**.</span></span>

<span data-ttu-id="7be76-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="7be76-113">**Applies To**</span></span>

[<span data-ttu-id="7be76-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="7be76-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="7be76-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="7be76-115">**Tag Syntax**</span></span>

<span data-ttu-id="7be76-116"><v: *Element* src = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="7be76-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="7be76-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="7be76-117">**Script Syntax**</span></span>

<span data-ttu-id="7be76-118">*Element* . src = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="7be76-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="7be76-119">*expressão* = de *elemento*. src</span><span class="sxs-lookup"><span data-stu-id="7be76-119">*expression*=*element*.src</span></span>

<span data-ttu-id="7be76-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="7be76-120">**Remarks**</span></span>

<span data-ttu-id="7be76-121">Esse atributo sempre deve ser usado com o elemento [ImageData](msdn-online-vml-imagedata-element.md) e apontar para dados de imagem válidos para uma imagem a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="7be76-121">This attribute must always be used with the [ImageData](msdn-online-vml-imagedata-element.md) element and point to valid image data for a picture to be displayed.</span></span> <span data-ttu-id="7be76-122">Se esse atributo aparecer sem [href](https://www.bing.com/search?q=HRef) ou [title](title-attribute--imagedata--vml.md), a imagem será vinculada.</span><span class="sxs-lookup"><span data-stu-id="7be76-122">If this attribute appears without [HRef](https://www.bing.com/search?q=HRef) or [Title](title-attribute--imagedata--vml.md), then the image is linked.</span></span>

<span data-ttu-id="7be76-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="7be76-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="7be76-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="7be76-124">**Example**</span></span>

<span data-ttu-id="7be76-125">A origem da imagem é um arquivo chamado "kids.jpg".</span><span class="sxs-lookup"><span data-stu-id="7be76-125">The source of the image is a file named "kids.jpg".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 