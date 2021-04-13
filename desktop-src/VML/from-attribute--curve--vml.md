---
title: Atributo from (curva) (VML)
description: Atributo from (curva) (VML)
ms.assetid: 70e940c1-3fa8-4a30-9ca8-584483cea485
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d5f78dee46192efed48172a7d1f4d9cc77582f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366622"
---
# <a name="from-attribute-curvevml"></a><span data-ttu-id="f817a-103">Atributo from (curva) (VML)</span><span class="sxs-lookup"><span data-stu-id="f817a-103">From Attribute (Curve)(VML)</span></span>

<span data-ttu-id="f817a-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f817a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f817a-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="f817a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f817a-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="f817a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f817a-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="f817a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f817a-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f817a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f817a-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f817a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f817a-110">Define o ponto de partida de uma curva.</span><span class="sxs-lookup"><span data-stu-id="f817a-110">Defines the starting point of a curve.</span></span> <span data-ttu-id="f817a-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f817a-111">Read/write.</span></span> <span data-ttu-id="f817a-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="f817a-112">**VgVector2D**.</span></span>

<span data-ttu-id="f817a-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="f817a-113">**Applies To**</span></span>

[<span data-ttu-id="f817a-114">Curva</span><span class="sxs-lookup"><span data-stu-id="f817a-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="f817a-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="f817a-115">**Tag Syntax**</span></span>

<span data-ttu-id="f817a-116"><v: *Element* de = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="f817a-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="f817a-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="f817a-117">**Script Syntax**</span></span>

<span data-ttu-id="f817a-118">*elemento* . from = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="f817a-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="f817a-119">*expressão* = de *elemento*. from</span><span class="sxs-lookup"><span data-stu-id="f817a-119">*expression*=*element*.from</span></span>

<span data-ttu-id="f817a-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="f817a-120">**Remarks**</span></span>

<span data-ttu-id="f817a-121">Define o ponto inicial de uma curva de Bézier cúbica no espaço de coordenadas do elemento pai.</span><span class="sxs-lookup"><span data-stu-id="f817a-121">Defines the starting point of a cubic bezier curve in the coordinate space of the parent element.</span></span> <span data-ttu-id="f817a-122">Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado).</span><span class="sxs-lookup"><span data-stu-id="f817a-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="f817a-123">O padrão é 0, 0.</span><span class="sxs-lookup"><span data-stu-id="f817a-123">Default is 0,0.</span></span>

<span data-ttu-id="f817a-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="f817a-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="f817a-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="f817a-125">**Example**</span></span>

<span data-ttu-id="f817a-126">A curva é sorrindo.</span><span class="sxs-lookup"><span data-stu-id="f817a-126">The curve is smiling.</span></span> <span data-ttu-id="f817a-127">Ele começa à esquerda e termina à direita.</span><span class="sxs-lookup"><span data-stu-id="f817a-127">It starts at the left and ends at the right.</span></span> <span data-ttu-id="f817a-128">Os dois pontos de controle estão situados ao longo do caminho para puxar a curva para dar a aparência de um sorriso.</span><span class="sxs-lookup"><span data-stu-id="f817a-128">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```



 

 