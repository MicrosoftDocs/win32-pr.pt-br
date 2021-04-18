---
title: Atributo Font-Variant de VML
description: Atributo Font-Variant de VML
ms.assetid: f58bf3e0-e285-474c-83b1-203fce4f3c3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 243f8b36d36d8bb9b210a916cef239cda6061e0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366081"
---
# <a name="vml-font-variant-attribute"></a><span data-ttu-id="55b97-103">Atributo Font-Variant de VML</span><span class="sxs-lookup"><span data-stu-id="55b97-103">VML Font-Variant Attribute</span></span>

<span data-ttu-id="55b97-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="55b97-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="55b97-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="55b97-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="55b97-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="55b97-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="55b97-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="55b97-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="55b97-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="55b97-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="55b97-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="55b97-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="55b97-110">Define o estilo de variante de uma fonte.</span><span class="sxs-lookup"><span data-stu-id="55b97-110">Defines the variant style of a font.</span></span> <span data-ttu-id="55b97-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="55b97-111">Read/write.</span></span> <span data-ttu-id="55b97-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="55b97-112">**String**.</span></span>

<span data-ttu-id="55b97-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="55b97-113">**Applies To**</span></span>

[<span data-ttu-id="55b97-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="55b97-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="55b97-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="55b97-115">**Tag Syntax**</span></span>

<span data-ttu-id="55b97-116"><v: *Element* Style = "font-Variance: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="55b97-116"><v: *element* style="font-variant: *expression* "></span></span>

<span data-ttu-id="55b97-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="55b97-117">**Script Syntax**</span></span>

<span data-ttu-id="55b97-118">*elemento* . Style. fontvariant = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="55b97-118">*element* .style.fontvariant="*expression*"</span></span>

<span data-ttu-id="55b97-119">*expressão* = de *elemento*. Style. fontvariant</span><span class="sxs-lookup"><span data-stu-id="55b97-119">*expression*=*element*.style.fontvariant</span></span>

<span data-ttu-id="55b97-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="55b97-120">**Remarks**</span></span>

<span data-ttu-id="55b97-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="55b97-121">The values are:</span></span>

-   <span data-ttu-id="55b97-122">normal (padrão)</span><span class="sxs-lookup"><span data-stu-id="55b97-122">normal (default)</span></span>
-   <span data-ttu-id="55b97-123">versalete</span><span class="sxs-lookup"><span data-stu-id="55b97-123">small-caps</span></span>

<span data-ttu-id="55b97-124">Os valores são os mesmos que os atributos de estilo HTML padrão.</span><span class="sxs-lookup"><span data-stu-id="55b97-124">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="55b97-125">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="55b97-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="55b97-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="55b97-126">**Example**</span></span>

<span data-ttu-id="55b97-127">A fonte é renderizada como letras maiúsculas pequenas.</span><span class="sxs-lookup"><span data-stu-id="55b97-127">The font is rendered as small capital letters.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal small-caps normal 36pt Arial"/>
   </v:line>
```



 

 