---
title: Atributo MiterLimit de VML
description: Atributo MiterLimit de VML
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454143"
---
# <a name="vml-miterlimit-attribute"></a><span data-ttu-id="82761-103">Atributo MiterLimit de VML</span><span class="sxs-lookup"><span data-stu-id="82761-103">VML MiterLimit Attribute</span></span>

<span data-ttu-id="82761-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="82761-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="82761-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="82761-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="82761-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="82761-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="82761-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="82761-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="82761-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="82761-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="82761-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="82761-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="82761-110">Define a suavidade da junção de mitre.</span><span class="sxs-lookup"><span data-stu-id="82761-110">Defines the smoothness of the miter joint.</span></span> <span data-ttu-id="82761-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="82761-111">Read/write.</span></span> <span data-ttu-id="82761-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="82761-112">**VgNumber**.</span></span>

<span data-ttu-id="82761-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="82761-113">**Applies To**</span></span>

[<span data-ttu-id="82761-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="82761-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="82761-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="82761-115">**Tag Syntax**</span></span>

<span data-ttu-id="82761-116"><v: *Element* MiterLimit = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="82761-116"><v: *element* miterlimit=" *expression* "></span></span>

<span data-ttu-id="82761-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="82761-117">**Script Syntax**</span></span>

<span data-ttu-id="82761-118">*Element* . MiterLimit = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="82761-118">*element* .miterlimit="*expression*"</span></span>

<span data-ttu-id="82761-119">*expressão* = de *elemento*. MiterLimit</span><span class="sxs-lookup"><span data-stu-id="82761-119">*expression*=*element*.miterlimit</span></span>

<span data-ttu-id="82761-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="82761-120">**Remarks**</span></span>

<span data-ttu-id="82761-121">A distância máxima entre o ponto interno e o ponto externo de uma junção.</span><span class="sxs-lookup"><span data-stu-id="82761-121">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="82761-122">Esse número é um múltiplo da espessura da linha.</span><span class="sxs-lookup"><span data-stu-id="82761-122">This number is a multiple of the thickness of the line.</span></span>

<span data-ttu-id="82761-123">O valor padrão é 8.</span><span class="sxs-lookup"><span data-stu-id="82761-123">The default value is 8.</span></span>

<span data-ttu-id="82761-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="82761-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="82761-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="82761-125">**Example**</span></span>

<span data-ttu-id="82761-126">As junções na polilinha são Mitre com um limite de 10, ou seja, 5 vezes 2 pontos.</span><span class="sxs-lookup"><span data-stu-id="82761-126">The joints on the polyline are mitered with a limit of 10, that is, 5 times 2 points.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 