---
title: Atributo StartArrowLength de VML
description: Atributo StartArrowLength de VML
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a57e10c9cf7b9a8683f4b1856355232afc16be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366283"
---
# <a name="vml-startarrowlength-attribute"></a><span data-ttu-id="63e84-103">Atributo StartArrowLength de VML</span><span class="sxs-lookup"><span data-stu-id="63e84-103">VML StartArrowLength Attribute</span></span>

<span data-ttu-id="63e84-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="63e84-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="63e84-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="63e84-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="63e84-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="63e84-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="63e84-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="63e84-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="63e84-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="63e84-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="63e84-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="63e84-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="63e84-110">Define o comprimento da ponta de seta para o início de uma linha.</span><span class="sxs-lookup"><span data-stu-id="63e84-110">Defines the arrowhead length for the start of a line.</span></span> <span data-ttu-id="63e84-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="63e84-111">Read/write.</span></span> <span data-ttu-id="63e84-112">**VgArrowheadLength**.</span><span class="sxs-lookup"><span data-stu-id="63e84-112">**VgArrowheadLength**.</span></span>

<span data-ttu-id="63e84-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="63e84-113">**Applies To**</span></span>

[<span data-ttu-id="63e84-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="63e84-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="63e84-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="63e84-115">**Tag Syntax**</span></span>

<span data-ttu-id="63e84-116"><v: *Element* startarrowlength = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="63e84-116"><v: *element* startarrowlength=" *expression* "></span></span>

<span data-ttu-id="63e84-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="63e84-117">**Script Syntax**</span></span>

<span data-ttu-id="63e84-118">*Element* . startarrowlength = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="63e84-118">*element* .startarrowlength="*expression*"</span></span>

<span data-ttu-id="63e84-119">*expressão* = de *elemento*. startarrowlength</span><span class="sxs-lookup"><span data-stu-id="63e84-119">*expression*=*element*.startarrowlength</span></span>

<span data-ttu-id="63e84-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="63e84-120">**Remarks**</span></span>

<span data-ttu-id="63e84-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="63e84-121">Values include:</span></span>

-   <span data-ttu-id="63e84-122">Short</span><span class="sxs-lookup"><span data-stu-id="63e84-122">Short</span></span>
-   <span data-ttu-id="63e84-123">Médio (padrão)</span><span class="sxs-lookup"><span data-stu-id="63e84-123">Medium (default)</span></span>
-   <span data-ttu-id="63e84-124">long</span><span class="sxs-lookup"><span data-stu-id="63e84-124">Long</span></span>

<span data-ttu-id="63e84-125">Atributo padrão da VML</span><span class="sxs-lookup"><span data-stu-id="63e84-125">VML Standard Attribute</span></span>

<span data-ttu-id="63e84-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="63e84-126">**Example**</span></span>

<span data-ttu-id="63e84-127">Uma linha é desenhada com uma pequena ponta de seta clássica no início do traço.</span><span class="sxs-lookup"><span data-stu-id="63e84-127">A line is drawn with a short classic arrowhead on the start of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 