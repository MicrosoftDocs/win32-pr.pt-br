---
title: Atributo de espaçamento da VML V-Text-
description: Atributo de espaçamento da VML V-Text-
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366364"
---
# <a name="vml-v-text-spacing-attribute"></a><span data-ttu-id="181b0-103">Atributo de espaçamento da VML V-Text-</span><span class="sxs-lookup"><span data-stu-id="181b0-103">VML V-Text-Spacing Attribute</span></span>

<span data-ttu-id="181b0-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="181b0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="181b0-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="181b0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="181b0-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="181b0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="181b0-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="181b0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="181b0-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="181b0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="181b0-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="181b0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="181b0-110">Define a quantidade de espaçamento do texto.</span><span class="sxs-lookup"><span data-stu-id="181b0-110">Defines the amount of spacing for text.</span></span> <span data-ttu-id="181b0-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="181b0-111">Read/write.</span></span> <span data-ttu-id="181b0-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="181b0-112">**VgNumber**.</span></span>

<span data-ttu-id="181b0-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="181b0-113">**Applies To**</span></span>

[<span data-ttu-id="181b0-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="181b0-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="181b0-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="181b0-115">**Tag Syntax**</span></span>

<span data-ttu-id="181b0-116"><v: *elemento* Style = "v-texto-Spacing: *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="181b0-116"><v: *element* style="v-text-spacing: *expression* "></span></span>

<span data-ttu-id="181b0-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="181b0-117">**Script Syntax**</span></span>

<span data-ttu-id="181b0-118">*elemento* . Style. v-espaçamento de texto = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="181b0-118">*element* .style.v-text-spacing="*expression*"</span></span>

<span data-ttu-id="181b0-119">*expressão* = de *elemento*. Style. v-espaçamento de texto</span><span class="sxs-lookup"><span data-stu-id="181b0-119">*expression*=*element*.style.v-text-spacing</span></span>

<span data-ttu-id="181b0-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="181b0-120">**Remarks**</span></span>

<span data-ttu-id="181b0-121">O valor padrão é 100.</span><span class="sxs-lookup"><span data-stu-id="181b0-121">The default value is 100.</span></span> <span data-ttu-id="181b0-122">Consulte o atributo [V-Text-Spacing-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) para obter mais informações sobre o espaçamento de texto.</span><span class="sxs-lookup"><span data-stu-id="181b0-122">See the [V-Text-Spacing-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) attribute for more information about text spacing.</span></span>

<span data-ttu-id="181b0-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="181b0-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="181b0-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="181b0-124">**Example**</span></span>

<span data-ttu-id="181b0-125">O espaçamento entre cada letra é reforçado por 200 unidades.</span><span class="sxs-lookup"><span data-stu-id="181b0-125">The letterspacing between each letter is tightened by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 