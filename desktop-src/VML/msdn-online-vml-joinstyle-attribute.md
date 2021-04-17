---
title: Atributo de junção de VML
description: Atributo de junção de VML
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d3c815d6165cecd853f394780237ad0b89f0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105784962"
---
# <a name="vml-joinstyle-attribute"></a><span data-ttu-id="20cae-103">Atributo de junção de VML</span><span class="sxs-lookup"><span data-stu-id="20cae-103">VML JoinStyle Attribute</span></span>

<span data-ttu-id="20cae-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="20cae-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="20cae-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="20cae-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="20cae-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="20cae-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="20cae-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="20cae-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="20cae-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="20cae-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="20cae-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="20cae-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="20cae-110">Define o estilo de junção de uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="20cae-110">Defines the join style of a polyline.</span></span> <span data-ttu-id="20cae-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="20cae-111">Read/write.</span></span> <span data-ttu-id="20cae-112">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="20cae-112">String.</span></span>

<span data-ttu-id="20cae-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="20cae-113">**Applies To**</span></span>

[<span data-ttu-id="20cae-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="20cae-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="20cae-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="20cae-115">**Tag Syntax**</span></span>

<span data-ttu-id="20cae-116"><v: *Element* joinstyle = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="20cae-116"><v: *element* joinstyle=" *expression* "></span></span>

<span data-ttu-id="20cae-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="20cae-117">**Script Syntax**</span></span>

<span data-ttu-id="20cae-118">*elemento* . joinstyle = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="20cae-118">*element* .joinstyle="*expression*"</span></span>

<span data-ttu-id="20cae-119">*expressão* = de *elemento*. joinstyle</span><span class="sxs-lookup"><span data-stu-id="20cae-119">*expression*=*element*.joinstyle</span></span>

<span data-ttu-id="20cae-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="20cae-120">**Remarks**</span></span>

<span data-ttu-id="20cae-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="20cae-121">Values include:</span></span>

-   <span data-ttu-id="20cae-122">Round (padrão)</span><span class="sxs-lookup"><span data-stu-id="20cae-122">round (default)</span></span>
-   <span data-ttu-id="20cae-123">emoldura</span><span class="sxs-lookup"><span data-stu-id="20cae-123">bevel</span></span>
-   <span data-ttu-id="20cae-124">União</span><span class="sxs-lookup"><span data-stu-id="20cae-124">miter</span></span>

<span data-ttu-id="20cae-125">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="20cae-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="20cae-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="20cae-126">**Example**</span></span>

<span data-ttu-id="20cae-127">As junções na polilinha são chanfradas.</span><span class="sxs-lookup"><span data-stu-id="20cae-127">The joints on the polyline are beveled.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 