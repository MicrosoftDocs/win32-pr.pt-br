---
title: Atributo Font-Size de VML
description: Atributo Font-Size de VML
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c02b2df8fb0076ed6df6342e40b980ed8aa248e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454330"
---
# <a name="vml-font-size-attribute"></a><span data-ttu-id="99a36-103">Atributo Font-Size de VML</span><span class="sxs-lookup"><span data-stu-id="99a36-103">VML Font-Size Attribute</span></span>

<span data-ttu-id="99a36-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="99a36-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="99a36-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="99a36-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="99a36-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="99a36-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="99a36-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="99a36-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="99a36-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="99a36-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="99a36-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="99a36-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="99a36-110">Define o tamanho da fonte.</span><span class="sxs-lookup"><span data-stu-id="99a36-110">Defines the size of the font.</span></span> <span data-ttu-id="99a36-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="99a36-111">Read/write.</span></span> <span data-ttu-id="99a36-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="99a36-112">**String**.</span></span>

<span data-ttu-id="99a36-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="99a36-113">**Applies To**</span></span>

[<span data-ttu-id="99a36-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="99a36-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="99a36-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="99a36-115">**Tag Syntax**</span></span>

<span data-ttu-id="99a36-116"><v: *elemento* Style = "fonte-tamanho: *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="99a36-116"><v: *element* style="font-size: *expression* "></span></span>

<span data-ttu-id="99a36-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="99a36-117">**Script Syntax**</span></span>

<span data-ttu-id="99a36-118">*elemento* . Style. FontSize = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="99a36-118">*element* .style.fontsize="*expression*"</span></span>

<span data-ttu-id="99a36-119">*expressão* = de *elemento*. Style. FontSize</span><span class="sxs-lookup"><span data-stu-id="99a36-119">*expression*=*element*.style.fontsize</span></span>

<span data-ttu-id="99a36-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="99a36-120">**Remarks**</span></span>

<span data-ttu-id="99a36-121">O tamanho da fonte é definido em pontos.</span><span class="sxs-lookup"><span data-stu-id="99a36-121">The font size is defined in points.</span></span> <span data-ttu-id="99a36-122">Os valores são os mesmos que os atributos de estilo HTML padrão.</span><span class="sxs-lookup"><span data-stu-id="99a36-122">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="99a36-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="99a36-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="99a36-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="99a36-124">**Example**</span></span>

<span data-ttu-id="99a36-125">O tamanho da fonte é de 36 pontos.</span><span class="sxs-lookup"><span data-stu-id="99a36-125">The font size is 36 points.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 