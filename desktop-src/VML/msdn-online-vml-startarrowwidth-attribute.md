---
title: Atributo StartArrowWidth de VML
description: Atributo StartArrowWidth de VML
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ba4f5adddc328d1791fa2beb570f59da826f83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641409"
---
# <a name="vml-startarrowwidth-attribute"></a><span data-ttu-id="cdaca-103">Atributo StartArrowWidth de VML</span><span class="sxs-lookup"><span data-stu-id="cdaca-103">VML StartArrowWidth Attribute</span></span>

<span data-ttu-id="cdaca-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cdaca-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cdaca-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="cdaca-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cdaca-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="cdaca-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cdaca-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="cdaca-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cdaca-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cdaca-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cdaca-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cdaca-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cdaca-110">Define a largura da ponta de seta para o início de uma linha.</span><span class="sxs-lookup"><span data-stu-id="cdaca-110">Defines the arrowhead width for the start of a line.</span></span> <span data-ttu-id="cdaca-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cdaca-111">Read/write.</span></span> <span data-ttu-id="cdaca-112">**VgArrowheadWidth**.</span><span class="sxs-lookup"><span data-stu-id="cdaca-112">**VgArrowheadWidth**.</span></span>

<span data-ttu-id="cdaca-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="cdaca-113">**Applies To**</span></span>

[<span data-ttu-id="cdaca-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="cdaca-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="cdaca-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="cdaca-115">**Tag Syntax**</span></span>

<span data-ttu-id="cdaca-116"><v: *Element* startarrowwidth = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="cdaca-116"><v: *element* startarrowwidth=" *expression* "></span></span>

<span data-ttu-id="cdaca-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="cdaca-117">**Script Syntax**</span></span>

<span data-ttu-id="cdaca-118">*Element* . startarrowwidth = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="cdaca-118">*element* .startarrowwidth="*expression*"</span></span>

<span data-ttu-id="cdaca-119">*expressão* = de *elemento*. startarrowwidth</span><span class="sxs-lookup"><span data-stu-id="cdaca-119">*expression*=*element*.startarrowwidth</span></span>

<span data-ttu-id="cdaca-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="cdaca-120">**Remarks**</span></span>

<span data-ttu-id="cdaca-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="cdaca-121">Values include:</span></span>

-   <span data-ttu-id="cdaca-122">Encontrar</span><span class="sxs-lookup"><span data-stu-id="cdaca-122">Narrow</span></span>
-   <span data-ttu-id="cdaca-123">Médio (padrão)</span><span class="sxs-lookup"><span data-stu-id="cdaca-123">Medium (default)</span></span>
-   <span data-ttu-id="cdaca-124">Ampla</span><span class="sxs-lookup"><span data-stu-id="cdaca-124">Wide</span></span>

<span data-ttu-id="cdaca-125">Atributo padrão da VML</span><span class="sxs-lookup"><span data-stu-id="cdaca-125">VML Standard Attribute</span></span>

<span data-ttu-id="cdaca-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="cdaca-126">**Example**</span></span>

<span data-ttu-id="cdaca-127">Uma linha é desenhada com uma ponta de seta clássica no início do traço.</span><span class="sxs-lookup"><span data-stu-id="cdaca-127">A line is drawn with a wide classic arrowhead on the start of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 