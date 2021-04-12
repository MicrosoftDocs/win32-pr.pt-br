---
title: Atributo EndCap de VML
description: Atributo EndCap de VML
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726d2bba2128ebb1897f306ae608f4bebb48d63f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294487"
---
# <a name="vml-endcap-attribute"></a><span data-ttu-id="24c73-103">Atributo EndCap de VML</span><span class="sxs-lookup"><span data-stu-id="24c73-103">VML EndCap Attribute</span></span>

<span data-ttu-id="24c73-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="24c73-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="24c73-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="24c73-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="24c73-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="24c73-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="24c73-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="24c73-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="24c73-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="24c73-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="24c73-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="24c73-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="24c73-110">Define o estilo de extremidade para o final de um traço.</span><span class="sxs-lookup"><span data-stu-id="24c73-110">Defines the cap style for the end of a stroke.</span></span> <span data-ttu-id="24c73-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="24c73-111">Read/write.</span></span> <span data-ttu-id="24c73-112">**VgLineEndCapStyle**.</span><span class="sxs-lookup"><span data-stu-id="24c73-112">**VgLineEndCapStyle**.</span></span>

<span data-ttu-id="24c73-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="24c73-113">**Applies To**</span></span>

[<span data-ttu-id="24c73-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="24c73-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="24c73-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="24c73-115">**Tag Syntax**</span></span>

<span data-ttu-id="24c73-116"><v: *Element* EndCap = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="24c73-116"><v: *element* endcap=" *expression* "></span></span>

<span data-ttu-id="24c73-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="24c73-117">**Script Syntax**</span></span>

<span data-ttu-id="24c73-118">*Element* . EndCap = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="24c73-118">*element* .endcap="*expression*"</span></span>

<span data-ttu-id="24c73-119">*expressão* = de *elemento*. EndCap</span><span class="sxs-lookup"><span data-stu-id="24c73-119">*expression*=*element*.endcap</span></span>

<span data-ttu-id="24c73-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="24c73-120">**Remarks**</span></span>

<span data-ttu-id="24c73-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="24c73-121">Values include:</span></span>

-   <span data-ttu-id="24c73-122">Simples (padrão)</span><span class="sxs-lookup"><span data-stu-id="24c73-122">Flat (default)</span></span>
-   <span data-ttu-id="24c73-123">Square</span><span class="sxs-lookup"><span data-stu-id="24c73-123">Square</span></span>
-   <span data-ttu-id="24c73-124">Round</span><span class="sxs-lookup"><span data-stu-id="24c73-124">Round</span></span>

<span data-ttu-id="24c73-125">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="24c73-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="24c73-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="24c73-126">**Example**</span></span>

<span data-ttu-id="24c73-127">Uma linha é desenhada com uma extremidade plana no final do traço.</span><span class="sxs-lookup"><span data-stu-id="24c73-127">A line is drawn with a flat cap on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 