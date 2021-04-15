---
title: Atributo Offset2 de VML
description: Atributo Offset2 de VML
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499132"
---
# <a name="vml-offset2-attribute"></a><span data-ttu-id="a81d6-103">Atributo Offset2 de VML</span><span class="sxs-lookup"><span data-stu-id="a81d6-103">VML Offset2 Attribute</span></span>

<span data-ttu-id="a81d6-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a81d6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a81d6-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="a81d6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a81d6-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="a81d6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a81d6-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="a81d6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a81d6-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a81d6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a81d6-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a81d6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a81d6-110">Determina um segundo deslocamento.</span><span class="sxs-lookup"><span data-stu-id="a81d6-110">Determines a second offset.</span></span> <span data-ttu-id="a81d6-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a81d6-111">Read/write.</span></span> <span data-ttu-id="a81d6-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="a81d6-112">**VgVector2D**.</span></span>

<span data-ttu-id="a81d6-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="a81d6-113">**Applies To**</span></span>

[<span data-ttu-id="a81d6-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="a81d6-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="a81d6-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="a81d6-115">**Tag Syntax**</span></span>

<span data-ttu-id="a81d6-116"><v: *Element* offset2 = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="a81d6-116"><v: *element* offset2=" *expression* "></span></span>

<span data-ttu-id="a81d6-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="a81d6-117">**Script Syntax**</span></span>

<span data-ttu-id="a81d6-118">*Element* . offset2 = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="a81d6-118">*element* .offset2="*expression*"</span></span>

<span data-ttu-id="a81d6-119">*expressão* = de *elemento*. offset2</span><span class="sxs-lookup"><span data-stu-id="a81d6-119">*expression*=*element*.offset2</span></span>

<span data-ttu-id="a81d6-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="a81d6-120">**Remarks**</span></span>

<span data-ttu-id="a81d6-121">O padrão para um segundo deslocamento para o valor x é 0 e o padrão para o valor y é 0.</span><span class="sxs-lookup"><span data-stu-id="a81d6-121">The default for a second offset for the x value is 0 and the default for the y value is 0.</span></span> <span data-ttu-id="a81d6-122">Os valores são uma medida absoluta ou um valor fracionário de Shape.</span><span class="sxs-lookup"><span data-stu-id="a81d6-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="a81d6-123">Se fracionários, os valores variam de 50% a-50%.</span><span class="sxs-lookup"><span data-stu-id="a81d6-123">If fractional, the values range from 50% to -50%.</span></span>

<span data-ttu-id="a81d6-124">Use um segundo deslocamento para criar efeitos de sombra especiais.</span><span class="sxs-lookup"><span data-stu-id="a81d6-124">Use a second offset to create special shadow effects.</span></span> <span data-ttu-id="a81d6-125">Consulte o atributo [Type](type-attribute--shadow--vml.md) para obter mais informações sobre os segundos deslocamentos.</span><span class="sxs-lookup"><span data-stu-id="a81d6-125">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second offsets.</span></span>

<span data-ttu-id="a81d6-126">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="a81d6-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="a81d6-127">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a81d6-127">**Example**</span></span>

<span data-ttu-id="a81d6-128">Uma sombra dupla é criada para a forma.</span><span class="sxs-lookup"><span data-stu-id="a81d6-128">A double shadow is created for the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 