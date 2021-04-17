---
title: Atributo EndArrowLength de VML
description: Atributo EndArrowLength de VML
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d9d8bfbd24a6a1b79208d50d4d2aef956a5bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105770566"
---
# <a name="vml-endarrowlength-attribute"></a><span data-ttu-id="ec979-103">Atributo EndArrowLength de VML</span><span class="sxs-lookup"><span data-stu-id="ec979-103">VML EndArrowLength Attribute</span></span>

<span data-ttu-id="ec979-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ec979-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ec979-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="ec979-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ec979-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="ec979-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ec979-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="ec979-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ec979-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ec979-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ec979-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ec979-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ec979-110">Define um comprimento de ponta de seta para o fim de uma linha.</span><span class="sxs-lookup"><span data-stu-id="ec979-110">Defines an arrowhead length for the end of a line.</span></span> <span data-ttu-id="ec979-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ec979-111">Read/write.</span></span> <span data-ttu-id="ec979-112">**VgArrowheadLength**.</span><span class="sxs-lookup"><span data-stu-id="ec979-112">**VgArrowheadLength**.</span></span>

<span data-ttu-id="ec979-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="ec979-113">**Applies To**</span></span>

[<span data-ttu-id="ec979-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="ec979-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="ec979-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="ec979-115">**Tag Syntax**</span></span>

<span data-ttu-id="ec979-116"><v: *Element* endarrowlength = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="ec979-116"><v: *element* endarrowlength=" *expression* "></span></span>

<span data-ttu-id="ec979-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="ec979-117">**Script Syntax**</span></span>

<span data-ttu-id="ec979-118">*Element* . endarrowlength = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="ec979-118">*element* .endarrowlength="*expression*"</span></span>

<span data-ttu-id="ec979-119">*expressão* = de *elemento*. endarrowlength</span><span class="sxs-lookup"><span data-stu-id="ec979-119">*expression*=*element*.endarrowlength</span></span>

<span data-ttu-id="ec979-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="ec979-120">**Remarks**</span></span>

<span data-ttu-id="ec979-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="ec979-121">Values include:</span></span>

-   <span data-ttu-id="ec979-122">Short</span><span class="sxs-lookup"><span data-stu-id="ec979-122">Short</span></span>
-   <span data-ttu-id="ec979-123">Médio (padrão)</span><span class="sxs-lookup"><span data-stu-id="ec979-123">Medium (default)</span></span>
-   <span data-ttu-id="ec979-124">long</span><span class="sxs-lookup"><span data-stu-id="ec979-124">Long</span></span>

<span data-ttu-id="ec979-125">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="ec979-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="ec979-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="ec979-126">**Example**</span></span>

<span data-ttu-id="ec979-127">Uma linha é desenhada com uma seta clássica curta no final do traço.</span><span class="sxs-lookup"><span data-stu-id="ec979-127">A line is drawn with a short classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 