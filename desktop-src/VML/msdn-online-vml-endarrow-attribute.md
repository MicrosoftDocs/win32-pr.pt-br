---
title: Atributo de fim da seta de VML
description: Atributo de fim da seta de VML
ms.assetid: 056cd011-bb3b-4f9a-83d0-9702e0e82e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542d6dbb3b30467c4bcad909f2b49d617f8bd886
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105770125"
---
# <a name="vml-endarrow-attribute"></a><span data-ttu-id="15895-103">Atributo de fim da seta de VML</span><span class="sxs-lookup"><span data-stu-id="15895-103">VML EndArrow Attribute</span></span>

<span data-ttu-id="15895-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="15895-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="15895-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="15895-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="15895-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="15895-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="15895-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="15895-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="15895-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="15895-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="15895-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="15895-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="15895-110">Define uma ponta de seta para o final de uma linha.</span><span class="sxs-lookup"><span data-stu-id="15895-110">Defines an arrowhead for the end of a line.</span></span> <span data-ttu-id="15895-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="15895-111">Read/write.</span></span> <span data-ttu-id="15895-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="15895-112">**String**.</span></span>

<span data-ttu-id="15895-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="15895-113">**Applies To**</span></span>

[<span data-ttu-id="15895-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="15895-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="15895-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="15895-115">**Tag Syntax**</span></span>

<span data-ttu-id="15895-116"><v: *elemento* endarrow = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="15895-116"><v: *element* endarrow=" *expression* "></span></span>

<span data-ttu-id="15895-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="15895-117">**Script Syntax**</span></span>

<span data-ttu-id="15895-118">*elemento* . endarrow = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="15895-118">*element* .endarrow="*expression*"</span></span>

<span data-ttu-id="15895-119">*expressão* = de *elemento*. endarrow</span><span class="sxs-lookup"><span data-stu-id="15895-119">*expression*=*element*.endarrow</span></span>

<span data-ttu-id="15895-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="15895-120">**Remarks**</span></span>

<span data-ttu-id="15895-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="15895-121">Values include:</span></span>

-   <span data-ttu-id="15895-122">Nenhum (padrão)</span><span class="sxs-lookup"><span data-stu-id="15895-122">None (default)</span></span>
-   <span data-ttu-id="15895-123">Bloquear</span><span class="sxs-lookup"><span data-stu-id="15895-123">Block</span></span>
-   <span data-ttu-id="15895-124">Clássico</span><span class="sxs-lookup"><span data-stu-id="15895-124">Classic</span></span>
-   <span data-ttu-id="15895-125">Diamond</span><span class="sxs-lookup"><span data-stu-id="15895-125">Diamond</span></span>
-   <span data-ttu-id="15895-126">Oval</span><span class="sxs-lookup"><span data-stu-id="15895-126">Oval</span></span>
-   <span data-ttu-id="15895-127">Aberto</span><span class="sxs-lookup"><span data-stu-id="15895-127">Open</span></span>

<span data-ttu-id="15895-128">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="15895-128">*VML Standard Attribute*</span></span>

<span data-ttu-id="15895-129">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="15895-129">**Example**</span></span>

<span data-ttu-id="15895-130">Uma linha é desenhada com uma ponta de seta clássica no final do traço.</span><span class="sxs-lookup"><span data-stu-id="15895-130">A line is drawn with a classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic"/>
   </v:line>
```



 

 