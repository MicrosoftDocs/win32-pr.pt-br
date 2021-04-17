---
title: Atributo de fonte VML
description: Atributo de fonte VML
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bace73b90cac7519ea6abacb73c80506c655e133
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105794576"
---
# <a name="vml-font-attribute"></a><span data-ttu-id="a7752-103">Atributo de fonte VML</span><span class="sxs-lookup"><span data-stu-id="a7752-103">VML Font Attribute</span></span>

<span data-ttu-id="a7752-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a7752-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a7752-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="a7752-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a7752-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="a7752-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a7752-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="a7752-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a7752-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a7752-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a7752-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a7752-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a7752-110">Especifica um valor composto de atributos de fonte.</span><span class="sxs-lookup"><span data-stu-id="a7752-110">Specifies a compound value of font attributes.</span></span> <span data-ttu-id="a7752-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a7752-111">Read/write.</span></span> <span data-ttu-id="a7752-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="a7752-112">**String**.</span></span>

<span data-ttu-id="a7752-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="a7752-113">**Applies To**</span></span>

[<span data-ttu-id="a7752-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="a7752-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="a7752-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="a7752-115">**Tag Syntax**</span></span>

<span data-ttu-id="a7752-116"><v: *Element* Style = "font: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a7752-116"><v: *element* style="font: *expression* "></span></span>

<span data-ttu-id="a7752-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="a7752-117">**Script Syntax**</span></span>

<span data-ttu-id="a7752-118">*elemento* . Style. Font = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="a7752-118">*element* .style.font="*expression*"</span></span>

<span data-ttu-id="a7752-119">*expressão* = de *elemento*. Style. Font</span><span class="sxs-lookup"><span data-stu-id="a7752-119">*expression*=*element*.style.font</span></span>

<span data-ttu-id="a7752-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="a7752-120">**Remarks**</span></span>

<span data-ttu-id="a7752-121">Define os atributos de uma fonte, incluindo família, estilo, peso, tamanho e variante.</span><span class="sxs-lookup"><span data-stu-id="a7752-121">Defines the attributes of a font, including family, style, weight, size, and variant.</span></span> <span data-ttu-id="a7752-122">A ordem das definições na cadeia de caracteres é: **estilo de fonte**, **fonte-variante**, **espessura da fonte**, tamanho da **fonte**, altura da **linha** e **família de fontes**.</span><span class="sxs-lookup"><span data-stu-id="a7752-122">The order of definitions in the string is: **font-style**, **font-variant**, **font-weight**, **font-size**, **line-height**, and **font-family**.</span></span> <span data-ttu-id="a7752-123">Os valores são os mesmos que os atributos de estilo HTML padrão.</span><span class="sxs-lookup"><span data-stu-id="a7752-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="a7752-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="a7752-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="a7752-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a7752-125">**Example**</span></span>

<span data-ttu-id="a7752-126">A fonte do texto TextPath é itálico, versalete, negrito, 36 ponto Arial.</span><span class="sxs-lookup"><span data-stu-id="a7752-126">The font of the textpath text is italic, small-caps, bold, 36 point Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 