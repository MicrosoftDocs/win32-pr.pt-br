---
title: Atributo Color2 (Stroke) (VML)
description: Atributo Color2 (Stroke) (VML)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d577843b7d65de4f6197beabc877c308cf00154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454226"
---
# <a name="color2-attribute-strokevml"></a><span data-ttu-id="b82b4-103">Atributo Color2 (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="b82b4-103">Color2 Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="b82b4-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b82b4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b82b4-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="b82b4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b82b4-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="b82b4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b82b4-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="b82b4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b82b4-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b82b4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b82b4-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b82b4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b82b4-110">Define uma segunda cor para traços.</span><span class="sxs-lookup"><span data-stu-id="b82b4-110">Defines a second color for strokes.</span></span> <span data-ttu-id="b82b4-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b82b4-111">Read/write.</span></span> <span data-ttu-id="b82b4-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="b82b4-112">**String**.</span></span>

<span data-ttu-id="b82b4-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="b82b4-113">**Applies To**</span></span>

[<span data-ttu-id="b82b4-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="b82b4-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="b82b4-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="b82b4-115">**Tag Syntax**</span></span>

<span data-ttu-id="b82b4-116"><v: *Element* color2 = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="b82b4-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="b82b4-117">Sintaxe do script</span><span class="sxs-lookup"><span data-stu-id="b82b4-117">Script Syntax</span></span>

<span data-ttu-id="b82b4-118">*Element* . color2 = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="b82b4-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="b82b4-119">*expressão* = de *elemento*. color2</span><span class="sxs-lookup"><span data-stu-id="b82b4-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="b82b4-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="b82b4-120">**Remarks**</span></span>

<span data-ttu-id="b82b4-121">Uma segunda cor é usada quando o tipo de preenchimento de um traço é um padrão.</span><span class="sxs-lookup"><span data-stu-id="b82b4-121">A second color is used when a stroke's fill type is a pattern.</span></span>

<span data-ttu-id="b82b4-122">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="b82b4-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="b82b4-123">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="b82b4-123">**Example**</span></span>

<span data-ttu-id="b82b4-124">O traço da forma é um preenchimento de padrão em que o preenchimento é definido pela imagem de origem, mas o plano de fundo transparente é definido pela segunda cor.</span><span class="sxs-lookup"><span data-stu-id="b82b4-124">The shape's stroke is a pattern fill where the fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 