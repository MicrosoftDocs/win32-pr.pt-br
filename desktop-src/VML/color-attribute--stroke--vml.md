---
title: Atributo Color (Stroke) (VML)
description: Atributo Color (Stroke) (VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa91522adcba5fa854d4749dc257f5489969270
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105784987"
---
# <a name="color-attribute-strokevml"></a><span data-ttu-id="a1377-103">Atributo Color (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="a1377-103">Color Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="a1377-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a1377-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a1377-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="a1377-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a1377-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="a1377-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a1377-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="a1377-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a1377-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a1377-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a1377-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a1377-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a1377-110">Define a cor de um traço.</span><span class="sxs-lookup"><span data-stu-id="a1377-110">Defines the color of a stroke.</span></span> <span data-ttu-id="a1377-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a1377-111">Read/write.</span></span> <span data-ttu-id="a1377-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="a1377-112">**VgColor**.</span></span>

<span data-ttu-id="a1377-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="a1377-113">**Applies To**</span></span>

[<span data-ttu-id="a1377-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="a1377-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="a1377-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="a1377-115">**Tag Syntax**</span></span>

<span data-ttu-id="a1377-116"><v: *Element* Color = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="a1377-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="a1377-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="a1377-117">**Script Syntax**</span></span>

<span data-ttu-id="a1377-118">*Element* . Color = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="a1377-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="a1377-119">*expressão* = de *elemento*. Color</span><span class="sxs-lookup"><span data-stu-id="a1377-119">*expression*=*element*.color</span></span>

<span data-ttu-id="a1377-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="a1377-120">**Remarks**</span></span>

<span data-ttu-id="a1377-121">Substitui o atributo **StrokeColor** de uma forma.</span><span class="sxs-lookup"><span data-stu-id="a1377-121">Overrides the **StrokeColor** attribute of a shape.</span></span> <span data-ttu-id="a1377-122">O valor padrão é **preto**.</span><span class="sxs-lookup"><span data-stu-id="a1377-122">The default value is **black**.</span></span>

<span data-ttu-id="a1377-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="a1377-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="a1377-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a1377-124">**Example**</span></span>

<span data-ttu-id="a1377-125">A forma tem uma cor de traço de **verde**, e não **vermelha**.</span><span class="sxs-lookup"><span data-stu-id="a1377-125">The shape has a stroke color of **green**, not **red**.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 