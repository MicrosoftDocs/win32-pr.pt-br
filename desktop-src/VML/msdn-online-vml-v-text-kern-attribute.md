---
title: Atributo de kerning da VML V-Text-
description: Atributo de kerning da VML V-Text-
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917513"
---
# <a name="vml-v-text-kern-attribute"></a><span data-ttu-id="aa5f9-103">Atributo de kerning da VML V-Text-</span><span class="sxs-lookup"><span data-stu-id="aa5f9-103">VML V-Text-Kern Attribute</span></span>

<span data-ttu-id="aa5f9-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="aa5f9-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="aa5f9-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="aa5f9-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="aa5f9-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="aa5f9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="aa5f9-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="aa5f9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="aa5f9-110">Determina se o kerning está ativado.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-110">Determines whether kerning is turned on.</span></span> <span data-ttu-id="aa5f9-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-111">Read/write.</span></span> <span data-ttu-id="aa5f9-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-112">**VgTriState**.</span></span>

<span data-ttu-id="aa5f9-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="aa5f9-113">**Applies To**</span></span>

[<span data-ttu-id="aa5f9-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="aa5f9-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="aa5f9-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="aa5f9-115">**Tag Syntax**</span></span>

<span data-ttu-id="aa5f9-116"><v: *elemento* Style = "v-Text-kerning: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="aa5f9-116"><v: *element* style="v-text-kern: *expression* "></span></span>

<span data-ttu-id="aa5f9-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="aa5f9-117">**Script Syntax**</span></span>

<span data-ttu-id="aa5f9-118">*elemento* . Style. v-Text-kerning = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="aa5f9-118">*element* .style.v-text-kern="*expression*"</span></span>

<span data-ttu-id="aa5f9-119">*expressão* = de *elemento*. Style. v-ajuste de texto</span><span class="sxs-lookup"><span data-stu-id="aa5f9-119">*expression*=*element*.style.v-text-kern</span></span>

<span data-ttu-id="aa5f9-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="aa5f9-120">**Remarks**</span></span>

<span data-ttu-id="aa5f9-121">Se for **true**, o kerning será ativado.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-121">If **True**, the kerning is turned on.</span></span> <span data-ttu-id="aa5f9-122">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-122">The default is **False**.</span></span> <span data-ttu-id="aa5f9-123">O kerning é a remoção de espaço entre determinados pares de letras para compensar letterformss desiguais.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-123">Kerning is the removal of space between certain letter pairs to compensate for uneven letterforms.</span></span> <span data-ttu-id="aa5f9-124">Por exemplo, se o kerning for ativado, o espaço extra entre um "T" maiúsculo e um "i" minúsculo seriam removidos.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-124">For example, if kerning is turned on, extra space between a capital "T" and a lowercase "i" would be removed.</span></span>

<span data-ttu-id="aa5f9-125">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="aa5f9-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="aa5f9-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="aa5f9-126">**Example**</span></span>

<span data-ttu-id="aa5f9-127">O kerning está ativado.</span><span class="sxs-lookup"><span data-stu-id="aa5f9-127">Kerning is turned on.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 