---
title: Atributo FitShape de VML
description: Atributo FitShape de VML
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b05d7bc31afc52c664217ff21d14b40fd0c27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105785389"
---
# <a name="vml-fitshape-attribute"></a><span data-ttu-id="0155f-103">Atributo FitShape de VML</span><span class="sxs-lookup"><span data-stu-id="0155f-103">VML FitShape Attribute</span></span>

<span data-ttu-id="0155f-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0155f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0155f-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="0155f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0155f-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="0155f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0155f-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="0155f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0155f-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0155f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0155f-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0155f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0155f-110">Define se o texto se ajusta à caixa delimitadora de uma forma.</span><span class="sxs-lookup"><span data-stu-id="0155f-110">Defines whether the text fits bounding box of a shape.</span></span> <span data-ttu-id="0155f-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0155f-111">Read/write.</span></span> <span data-ttu-id="0155f-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="0155f-112">**VgTriState**.</span></span>

<span data-ttu-id="0155f-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="0155f-113">**Applies To**</span></span>

[<span data-ttu-id="0155f-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="0155f-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="0155f-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="0155f-115">**Tag Syntax**</span></span>

<span data-ttu-id="0155f-116"><v: *Element* FitShape = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="0155f-116"><v: *element* fitshape=" *expression* "></span></span>

<span data-ttu-id="0155f-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="0155f-117">**Script Syntax**</span></span>

<span data-ttu-id="0155f-118">*Element* . FitShape = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="0155f-118">*element* .fitshape="*expression*"</span></span>

<span data-ttu-id="0155f-119">*expressão* = de *elemento*. FitShape</span><span class="sxs-lookup"><span data-stu-id="0155f-119">*expression*=*element*.fitshape</span></span>

<span data-ttu-id="0155f-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="0155f-120">**Remarks**</span></span>

<span data-ttu-id="0155f-121">Se **for true**, alongará o texto para as bordas da caixa que define a forma inteira.</span><span class="sxs-lookup"><span data-stu-id="0155f-121">If **True**, stretches the text out to the edges of the box that defines the entire shape.</span></span> <span data-ttu-id="0155f-122">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="0155f-122">The default is **False**.</span></span>

<span data-ttu-id="0155f-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="0155f-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0155f-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="0155f-124">**Example**</span></span>

<span data-ttu-id="0155f-125">O texto será alongado para se ajustar à forma.</span><span class="sxs-lookup"><span data-stu-id="0155f-125">The text will stretch to fit the shape.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 