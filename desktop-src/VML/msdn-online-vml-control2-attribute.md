---
title: Atributo Control2 de VML
description: Atributo Control2 de VML
ms.assetid: fd0f92fa-ae70-46c9-bfbe-fad8deea34f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7af3871981e26ff7eff471651de555483fd540
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084566"
---
# <a name="vml-control2-attribute"></a><span data-ttu-id="62069-103">Atributo Control2 de VML</span><span class="sxs-lookup"><span data-stu-id="62069-103">VML Control2 Attribute</span></span>

<span data-ttu-id="62069-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="62069-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="62069-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="62069-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="62069-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="62069-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="62069-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="62069-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="62069-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="62069-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="62069-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="62069-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="62069-110">Define o segundo ponto de controle de uma curva de Bézier.</span><span class="sxs-lookup"><span data-stu-id="62069-110">Defines the second control point of a bezier curve.</span></span> <span data-ttu-id="62069-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="62069-111">Read/write.</span></span> <span data-ttu-id="62069-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="62069-112">**VgVector2D**.</span></span>

<span data-ttu-id="62069-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="62069-113">**Applies To**</span></span>

[<span data-ttu-id="62069-114">Curva</span><span class="sxs-lookup"><span data-stu-id="62069-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="62069-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="62069-115">**Tag Syntax**</span></span>

<span data-ttu-id="62069-116"><v: *Element* Control2 = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="62069-116"><v: *element* control2=" *expression* "></span></span>

<span data-ttu-id="62069-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="62069-117">**Script Syntax**</span></span>

<span data-ttu-id="62069-118">*Element* . Control2 = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="62069-118">*element* .control2="*expression*"</span></span>

<span data-ttu-id="62069-119">*expressão* = de *elemento*. Control2</span><span class="sxs-lookup"><span data-stu-id="62069-119">*expression*=*element*.control2</span></span>

<span data-ttu-id="62069-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="62069-120">**Remarks**</span></span>

<span data-ttu-id="62069-121">Define o segundo ponto de controle de uma curva de Bézier cúbica no espaço de coordenadas do elemento pai. Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado).</span><span class="sxs-lookup"><span data-stu-id="62069-121">Defines the second control point of a cubic bezier curve in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="62069-122">O padrão é 20,0.</span><span class="sxs-lookup"><span data-stu-id="62069-122">Default is 20.0.</span></span>

<span data-ttu-id="62069-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="62069-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="62069-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="62069-124">**Example**</span></span>

<span data-ttu-id="62069-125">A curva é sorrindo.</span><span class="sxs-lookup"><span data-stu-id="62069-125">The curve is smiling.</span></span> <span data-ttu-id="62069-126">Ele começa à esquerda e termina à direita.</span><span class="sxs-lookup"><span data-stu-id="62069-126">It starts at the left and ends at the right.</span></span> <span data-ttu-id="62069-127">Os dois pontos de controle estão situados ao longo do caminho para puxar a curva para dar a aparência de um sorriso.</span><span class="sxs-lookup"><span data-stu-id="62069-127">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 