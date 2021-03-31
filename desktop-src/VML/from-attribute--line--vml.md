---
title: Atributo from (line) (VML)
description: Atributo from (line) (VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641776"
---
# <a name="from-attribute-linevml"></a><span data-ttu-id="96f9c-103">Atributo from (line) (VML)</span><span class="sxs-lookup"><span data-stu-id="96f9c-103">From Attribute (Line)(VML)</span></span>

<span data-ttu-id="96f9c-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="96f9c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="96f9c-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="96f9c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="96f9c-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="96f9c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="96f9c-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="96f9c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="96f9c-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="96f9c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="96f9c-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="96f9c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="96f9c-110">Define o ponto de partida de uma linha.</span><span class="sxs-lookup"><span data-stu-id="96f9c-110">Defines the starting point of a line.</span></span> <span data-ttu-id="96f9c-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="96f9c-111">Read/write.</span></span> <span data-ttu-id="96f9c-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="96f9c-112">**VgVector2D**.</span></span>

<span data-ttu-id="96f9c-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="96f9c-113">**Applies To**</span></span>

[<span data-ttu-id="96f9c-114">Linha</span><span class="sxs-lookup"><span data-stu-id="96f9c-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="96f9c-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="96f9c-115">**Tag Syntax**</span></span>

<span data-ttu-id="96f9c-116"><v: *Element* de = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="96f9c-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="96f9c-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="96f9c-117">**Script Syntax**</span></span>

<span data-ttu-id="96f9c-118">*elemento* . from = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="96f9c-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="96f9c-119">*expressão* = de *elemento*. from</span><span class="sxs-lookup"><span data-stu-id="96f9c-119">*expression*=*element*.from</span></span>

<span data-ttu-id="96f9c-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="96f9c-120">**Remarks**</span></span>

<span data-ttu-id="96f9c-121">Define o ponto inicial da linha no espaço de coordenadas do elemento pai. Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado).</span><span class="sxs-lookup"><span data-stu-id="96f9c-121">Defines the starting point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="96f9c-122">O padrão é 0, 0.</span><span class="sxs-lookup"><span data-stu-id="96f9c-122">Default is 0,0.</span></span>

<span data-ttu-id="96f9c-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="96f9c-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="96f9c-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="96f9c-124">**Example**</span></span>

<span data-ttu-id="96f9c-125">A linha começa em um local 10 aponta para baixo e 10 pontos à direita do canto superior esquerdo do espaço pai.</span><span class="sxs-lookup"><span data-stu-id="96f9c-125">The line starts at a location 10 points down and 10 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 