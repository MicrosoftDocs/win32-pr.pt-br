---
title: Atributo EndArrowWidth de VML
description: Atributo EndArrowWidth de VML
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641813"
---
# <a name="vml-endarrowwidth-attribute"></a><span data-ttu-id="e1232-103">Atributo EndArrowWidth de VML</span><span class="sxs-lookup"><span data-stu-id="e1232-103">VML EndArrowWidth Attribute</span></span>

<span data-ttu-id="e1232-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e1232-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e1232-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="e1232-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e1232-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="e1232-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e1232-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="e1232-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e1232-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e1232-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e1232-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e1232-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e1232-110">Define uma largura de seta para o fim de uma linha.</span><span class="sxs-lookup"><span data-stu-id="e1232-110">Defines an arrowhead width for the end of a line.</span></span> <span data-ttu-id="e1232-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e1232-111">Read/write.</span></span> <span data-ttu-id="e1232-112">**VgArrowheadWidth**.</span><span class="sxs-lookup"><span data-stu-id="e1232-112">**VgArrowheadWidth**.</span></span>

<span data-ttu-id="e1232-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="e1232-113">**Applies To**</span></span>

[<span data-ttu-id="e1232-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="e1232-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="e1232-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="e1232-115">**Tag Syntax**</span></span>

<span data-ttu-id="e1232-116"><v: *Element* endarrowwidth = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="e1232-116"><v: *element* endarrowwidth=" *expression* "></span></span>

<span data-ttu-id="e1232-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="e1232-117">**Script Syntax**</span></span>

<span data-ttu-id="e1232-118">*Element* . endarrowwidth = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="e1232-118">*element* .endarrowwidth="*expression*"</span></span>

<span data-ttu-id="e1232-119">*expressão* = de *elemento*. endarrowwidth</span><span class="sxs-lookup"><span data-stu-id="e1232-119">*expression*=*element*.endarrowwidth</span></span>

<span data-ttu-id="e1232-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="e1232-120">**Remarks**</span></span>

<span data-ttu-id="e1232-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="e1232-121">Values include:</span></span>

-   <span data-ttu-id="e1232-122">Encontrar</span><span class="sxs-lookup"><span data-stu-id="e1232-122">Narrow</span></span>
-   <span data-ttu-id="e1232-123">Médio (padrão)</span><span class="sxs-lookup"><span data-stu-id="e1232-123">Medium (default)</span></span>
-   <span data-ttu-id="e1232-124">Ampla</span><span class="sxs-lookup"><span data-stu-id="e1232-124">Wide</span></span>

<span data-ttu-id="e1232-125">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="e1232-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="e1232-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="e1232-126">**Example**</span></span>

<span data-ttu-id="e1232-127">Uma linha é desenhada com uma ponta de seta clássica no final do traço.</span><span class="sxs-lookup"><span data-stu-id="e1232-127">A line is drawn with a wide classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 