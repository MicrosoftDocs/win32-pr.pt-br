---
title: Para atributo (linha) (VML)
description: Para atributo (linha) (VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641807"
---
# <a name="to-attribute-linevml"></a><span data-ttu-id="ba356-103">Para atributo (linha) (VML)</span><span class="sxs-lookup"><span data-stu-id="ba356-103">To Attribute (Line)(VML)</span></span>

<span data-ttu-id="ba356-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ba356-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ba356-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="ba356-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ba356-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="ba356-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ba356-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="ba356-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ba356-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ba356-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ba356-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ba356-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ba356-110">Define o ponto final de uma linha.</span><span class="sxs-lookup"><span data-stu-id="ba356-110">Defines the ending point of a line.</span></span> <span data-ttu-id="ba356-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ba356-111">Read/write.</span></span> <span data-ttu-id="ba356-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="ba356-112">**VgVector2D**.</span></span>

<span data-ttu-id="ba356-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="ba356-113">**Applies To**</span></span>

[<span data-ttu-id="ba356-114">Linha</span><span class="sxs-lookup"><span data-stu-id="ba356-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="ba356-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="ba356-115">**Tag Syntax**</span></span>

<span data-ttu-id="ba356-116"><v: *Element* para = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ba356-116"><v: *element* to=" *expression* "></span></span>

<span data-ttu-id="ba356-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="ba356-117">**Script Syntax**</span></span>

<span data-ttu-id="ba356-118">*elemento* . to = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ba356-118">*element* .to="*expression*"</span></span>

<span data-ttu-id="ba356-119">*expressão* = de *elemento*. para</span><span class="sxs-lookup"><span data-stu-id="ba356-119">*expression*=*element*.to</span></span>

<span data-ttu-id="ba356-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="ba356-120">**Remarks**</span></span>

<span data-ttu-id="ba356-121">Define o ponto final da linha no espaço de coordenadas do elemento pai. Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado).</span><span class="sxs-lookup"><span data-stu-id="ba356-121">Defines the ending point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="ba356-122">O padrão é 10, 10.</span><span class="sxs-lookup"><span data-stu-id="ba356-122">Default is 10,10.</span></span>

<span data-ttu-id="ba356-123">**Atributo padrão da VML**</span><span class="sxs-lookup"><span data-stu-id="ba356-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="ba356-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="ba356-124">**Example**</span></span>

<span data-ttu-id="ba356-125">A linha termina em um local 100 aponta para baixo e 100 pontos à direita do canto superior esquerdo do espaço pai.</span><span class="sxs-lookup"><span data-stu-id="ba356-125">The line ends at a location 100 points down and 100 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 