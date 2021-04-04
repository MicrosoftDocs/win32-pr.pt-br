---
title: Atributo Font-Style de VML
description: Atributo Font-Style de VML
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f4fc2f299d78c3ccd8b194b8506cfce07abceb7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007622"
---
# <a name="vml-font-style-attribute"></a><span data-ttu-id="eb04e-103">Atributo Font-Style de VML</span><span class="sxs-lookup"><span data-stu-id="eb04e-103">VML Font-Style Attribute</span></span>

<span data-ttu-id="eb04e-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="eb04e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eb04e-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="eb04e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eb04e-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="eb04e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eb04e-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="eb04e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eb04e-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="eb04e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eb04e-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="eb04e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eb04e-110">Define a quantidade de inclinação de uma fonte.</span><span class="sxs-lookup"><span data-stu-id="eb04e-110">Defines the amount of slant for a font.</span></span> <span data-ttu-id="eb04e-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="eb04e-111">Read/write.</span></span> <span data-ttu-id="eb04e-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="eb04e-112">**String**.</span></span>

<span data-ttu-id="eb04e-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="eb04e-113">**Applies To**</span></span>

[<span data-ttu-id="eb04e-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="eb04e-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="eb04e-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="eb04e-115">**Tag Syntax**</span></span>

<span data-ttu-id="eb04e-116"><v: *elemento* Style = "fonte-estilo: *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="eb04e-116"><v: *element* style="font-style: *expression* "></span></span>

<span data-ttu-id="eb04e-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="eb04e-117">**Script Syntax**</span></span>

<span data-ttu-id="eb04e-118">*elemento* . Style. FontStyle = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="eb04e-118">*element* .style.fontstyle="*expression*"</span></span>

<span data-ttu-id="eb04e-119">*expressão* = de *elemento*. Style. FontStyle</span><span class="sxs-lookup"><span data-stu-id="eb04e-119">*expression*=*element*.style.fontstyle</span></span>

<span data-ttu-id="eb04e-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="eb04e-120">**Remarks**</span></span>

<span data-ttu-id="eb04e-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="eb04e-121">The values are:</span></span>

-   <span data-ttu-id="eb04e-122">normal (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb04e-122">normal (default)</span></span>
-   <span data-ttu-id="eb04e-123">oblíquo</span><span class="sxs-lookup"><span data-stu-id="eb04e-123">oblique</span></span>
-   <span data-ttu-id="eb04e-124">itálico</span><span class="sxs-lookup"><span data-stu-id="eb04e-124">italic</span></span>

<span data-ttu-id="eb04e-125">A maioria dos navegadores renderiza Oblique como itálico.</span><span class="sxs-lookup"><span data-stu-id="eb04e-125">Most browsers render oblique as italic.</span></span> <span data-ttu-id="eb04e-126">Os valores são os mesmos que os atributos de estilo HTML padrão.</span><span class="sxs-lookup"><span data-stu-id="eb04e-126">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="eb04e-127">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="eb04e-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="eb04e-128">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="eb04e-128">**Example**</span></span>

<span data-ttu-id="eb04e-129">A fonte é itálico (inclinada).</span><span class="sxs-lookup"><span data-stu-id="eb04e-129">The font is italic (slanted).</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 