---
title: Para atributo (curva) (VML)
description: Para atributo (curva) (VML)
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c0c9a858ff2cc8304ffacefb1cae477614e470
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823976"
---
# <a name="to-attribute-curvevml"></a><span data-ttu-id="e3a14-103">Para atributo (curva) (VML)</span><span class="sxs-lookup"><span data-stu-id="e3a14-103">To Attribute (Curve)(VML)</span></span>

<span data-ttu-id="e3a14-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e3a14-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e3a14-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="e3a14-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e3a14-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="e3a14-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e3a14-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="e3a14-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e3a14-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e3a14-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e3a14-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e3a14-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e3a14-110">Define o ponto final de uma curva.</span><span class="sxs-lookup"><span data-stu-id="e3a14-110">Defines the ending point of a curve.</span></span> <span data-ttu-id="e3a14-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e3a14-111">Read/write.</span></span> <span data-ttu-id="e3a14-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="e3a14-112">**VgVector2D**.</span></span>

<span data-ttu-id="e3a14-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="e3a14-113">**Applies To**</span></span>

[<span data-ttu-id="e3a14-114">Curva</span><span class="sxs-lookup"><span data-stu-id="e3a14-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="e3a14-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="e3a14-115">**Tag Syntax**</span></span>

<span data-ttu-id="e3a14-116"><v: *Element* para = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e3a14-116"><v: *element* to=" *expression* "></span></span>

<span data-ttu-id="e3a14-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="e3a14-117">**Script Syntax**</span></span>

<span data-ttu-id="e3a14-118">*elemento* . to = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e3a14-118">*element* .to="*expression*"</span></span>

<span data-ttu-id="e3a14-119">*expressão* = de *elemento*. para</span><span class="sxs-lookup"><span data-stu-id="e3a14-119">*expression*=*element*.to</span></span>

<span data-ttu-id="e3a14-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="e3a14-120">**Remarks**</span></span>

<span data-ttu-id="e3a14-121">Define o ponto final de uma curva de Bézier cúbica no espaço de coordenadas do elemento pai.</span><span class="sxs-lookup"><span data-stu-id="e3a14-121">Defines the ending point of a cubic bezier curve in the coordinate space of the parent element.</span></span> <span data-ttu-id="e3a14-122">Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado).</span><span class="sxs-lookup"><span data-stu-id="e3a14-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="e3a14-123">O padrão é 30, 20.</span><span class="sxs-lookup"><span data-stu-id="e3a14-123">Default is 30,20.</span></span>

<span data-ttu-id="e3a14-124">**Atributo padrão da VML**</span><span class="sxs-lookup"><span data-stu-id="e3a14-124">**VML Standard Attribute**</span></span>

<span data-ttu-id="e3a14-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="e3a14-125">**Example**</span></span>

<span data-ttu-id="e3a14-126">A curva é sorrindo.</span><span class="sxs-lookup"><span data-stu-id="e3a14-126">The curve is smiling.</span></span> <span data-ttu-id="e3a14-127">Ele começa à esquerda e termina à direita.</span><span class="sxs-lookup"><span data-stu-id="e3a14-127">It starts at the left and ends at the right.</span></span> <span data-ttu-id="e3a14-128">Os dois pontos de controle estão situados ao longo do caminho para puxar a curva para dar a aparência de um sorriso.</span><span class="sxs-lookup"><span data-stu-id="e3a14-128">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 