---
title: Atributo Text-Decoration de VML
description: Atributo Text-Decoration de VML
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee85007db2dbca04221604cafd79c5d7052c91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917373"
---
# <a name="vml-text-decoration-attribute"></a><span data-ttu-id="457c3-103">Atributo Text-Decoration de VML</span><span class="sxs-lookup"><span data-stu-id="457c3-103">VML Text-Decoration Attribute</span></span>

<span data-ttu-id="457c3-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="457c3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="457c3-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="457c3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="457c3-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="457c3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="457c3-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="457c3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="457c3-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="457c3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="457c3-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="457c3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="457c3-110">Define o estilo de decoração de texto.</span><span class="sxs-lookup"><span data-stu-id="457c3-110">Defines the style of text decoration.</span></span> <span data-ttu-id="457c3-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="457c3-111">Read/write.</span></span> <span data-ttu-id="457c3-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="457c3-112">**String**.</span></span>

<span data-ttu-id="457c3-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="457c3-113">**Applies To**</span></span>

[<span data-ttu-id="457c3-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="457c3-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="457c3-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="457c3-115">**Tag Syntax**</span></span>

<span data-ttu-id="457c3-116"><v: *Element* Style = "Text-decoração: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="457c3-116"><v: *element* style="text-decoration: *expression* "></span></span>

<span data-ttu-id="457c3-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="457c3-117">**Script Syntax**</span></span>

<span data-ttu-id="457c3-118">*elemento* . Style. TextDecoration = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="457c3-118">*element* .style.textdecoration="*expression*"</span></span>

<span data-ttu-id="457c3-119">*expressão* = de *elemento*. Style. TextDecoration</span><span class="sxs-lookup"><span data-stu-id="457c3-119">*expression*=*element*.style.textdecoration</span></span>

<span data-ttu-id="457c3-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="457c3-120">**Remarks**</span></span>

<span data-ttu-id="457c3-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="457c3-121">Values include:</span></span>

-   <span data-ttu-id="457c3-122">Nenhum (padrão)</span><span class="sxs-lookup"><span data-stu-id="457c3-122">none (default)</span></span>
-   <span data-ttu-id="457c3-123">underline</span><span class="sxs-lookup"><span data-stu-id="457c3-123">underline</span></span>
-   <span data-ttu-id="457c3-124">sobreposta</span><span class="sxs-lookup"><span data-stu-id="457c3-124">overline</span></span>
-   <span data-ttu-id="457c3-125">linha por</span><span class="sxs-lookup"><span data-stu-id="457c3-125">line-through</span></span>
-   <span data-ttu-id="457c3-126">blink</span><span class="sxs-lookup"><span data-stu-id="457c3-126">blink</span></span>

<span data-ttu-id="457c3-127">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="457c3-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="457c3-128">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="457c3-128">**Example**</span></span>

<span data-ttu-id="457c3-129">O texto será sublinhado.</span><span class="sxs-lookup"><span data-stu-id="457c3-129">The text will be underlined.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 