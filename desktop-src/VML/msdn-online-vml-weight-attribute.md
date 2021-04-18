---
title: Atributo de peso da VML
description: Atributo de peso da VML
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7a1a4d5dca91da6b3750f0d901d4e278a80dd7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105807189"
---
# <a name="vml-weight-attribute"></a><span data-ttu-id="abb32-103">Atributo de peso da VML</span><span class="sxs-lookup"><span data-stu-id="abb32-103">VML Weight Attribute</span></span>

<span data-ttu-id="abb32-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="abb32-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="abb32-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="abb32-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="abb32-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="abb32-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="abb32-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="abb32-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="abb32-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="abb32-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="abb32-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="abb32-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="abb32-110">Define a espessura de um traço.</span><span class="sxs-lookup"><span data-stu-id="abb32-110">Defines the thickness of a stroke.</span></span> <span data-ttu-id="abb32-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="abb32-111">Read/write.</span></span> <span data-ttu-id="abb32-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="abb32-112">**String**.</span></span>

<span data-ttu-id="abb32-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="abb32-113">**Applies To**</span></span>

[<span data-ttu-id="abb32-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="abb32-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="abb32-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="abb32-115">**Tag Syntax**</span></span>

<span data-ttu-id="abb32-116"><v: *elemento* Weight = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="abb32-116"><v: *element* weight=" *expression* "></span></span>

<span data-ttu-id="abb32-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="abb32-117">**Script Syntax**</span></span>

<span data-ttu-id="abb32-118">*elemento* . Weight = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="abb32-118">*element* .weight="*expression*"</span></span>

<span data-ttu-id="abb32-119">*expressão* = de *elemento*. Weight</span><span class="sxs-lookup"><span data-stu-id="abb32-119">*expression*=*element*.weight</span></span>

<span data-ttu-id="abb32-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="abb32-120">**Remarks**</span></span>

<span data-ttu-id="abb32-121">Esse atributo é o mesmo que o atributo **StrokeWeight** da **forma** e o substitui.</span><span class="sxs-lookup"><span data-stu-id="abb32-121">This attribute is the same as the **StrokeWeight** attribute of **Shape** and overrides it.</span></span> <span data-ttu-id="abb32-122">O valor padrão é 1 ponto.</span><span class="sxs-lookup"><span data-stu-id="abb32-122">The default value is 1 point.</span></span>

<span data-ttu-id="abb32-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="abb32-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="abb32-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="abb32-124">**Example**</span></span>

<span data-ttu-id="abb32-125">O traço tem uma espessura de 5 pontos, e não dois pontos.</span><span class="sxs-lookup"><span data-stu-id="abb32-125">The stroke has a thickness of 5 points, not 2 points.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 