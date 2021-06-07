---
description: Contém um conjunto de elementos&\# 8212; Parágrafo, InkWord, desenho, texto, imagem ou sinalizador&\# 8212; que são agrupados juntos na nota do diário.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento GroupNode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc4d39a592b5b6328bd31ff37761cfd3f0138c0
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432561"
---
# <a name="groupnode-element"></a><span data-ttu-id="969fe-103">Elemento GroupNode</span><span class="sxs-lookup"><span data-stu-id="969fe-103">GroupNode Element</span></span>

<span data-ttu-id="969fe-104">Contém um conjunto de elementos ([**parágrafo**](paragraph-element.md), [**InkWord**](inkword-element.md), [**desenho**](drawing-element.md), [**texto**](text-element.md), [**imagem**](image-element.md)ou [**sinalizador**](flag-element.md)) que são agrupados na nota do diário.</span><span class="sxs-lookup"><span data-stu-id="969fe-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="969fe-105">Definição</span><span class="sxs-lookup"><span data-stu-id="969fe-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="969fe-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="969fe-106">Parent Elements</span></span>

[<span data-ttu-id="969fe-107">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="969fe-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="969fe-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="969fe-108">Child Elements</span></span>

[<span data-ttu-id="969fe-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="969fe-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="969fe-110">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="969fe-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="969fe-111">**Desenho**</span><span class="sxs-lookup"><span data-stu-id="969fe-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="969fe-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="969fe-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="969fe-113">**Imagem**</span><span class="sxs-lookup"><span data-stu-id="969fe-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="969fe-114">**Identificar**</span><span class="sxs-lookup"><span data-stu-id="969fe-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="969fe-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="969fe-115">Attributes</span></span>



| <span data-ttu-id="969fe-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="969fe-116">Attribute</span></span>  | <span data-ttu-id="969fe-117">Type</span><span class="sxs-lookup"><span data-stu-id="969fe-117">Type</span></span>                      | <span data-ttu-id="969fe-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="969fe-118">Required</span></span> | <span data-ttu-id="969fe-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="969fe-119">Description</span></span>                                                                             | <span data-ttu-id="969fe-120">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="969fe-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="969fe-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="969fe-121">**Left**</span></span>   | <span data-ttu-id="969fe-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="969fe-122">**xs:integer**</span></span>            | <span data-ttu-id="969fe-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="969fe-123">Required</span></span> | <span data-ttu-id="969fe-124">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="969fe-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="969fe-125">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="969fe-125">Any integer.</span></span>              |
| <span data-ttu-id="969fe-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="969fe-126">**Top**</span></span>    | <span data-ttu-id="969fe-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="969fe-127">**xs:integer**</span></span>            | <span data-ttu-id="969fe-128">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="969fe-128">Required</span></span> | <span data-ttu-id="969fe-129">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="969fe-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="969fe-130">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="969fe-130">Any integer.</span></span>              |
| <span data-ttu-id="969fe-131">**Largura**</span><span class="sxs-lookup"><span data-stu-id="969fe-131">**Width**</span></span>  | <span data-ttu-id="969fe-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="969fe-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="969fe-133">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="969fe-133">Required</span></span> | <span data-ttu-id="969fe-134">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="969fe-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="969fe-135">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="969fe-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="969fe-136">**Altura**</span><span class="sxs-lookup"><span data-stu-id="969fe-136">**Height**</span></span> | <span data-ttu-id="969fe-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="969fe-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="969fe-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="969fe-138">Required</span></span> | <span data-ttu-id="969fe-139">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="969fe-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="969fe-140">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="969fe-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="969fe-141">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="969fe-141">Element Information</span></span>



|  <span data-ttu-id="969fe-142">Elemento</span><span class="sxs-lookup"><span data-stu-id="969fe-142">Element</span></span>     | <span data-ttu-id="969fe-143">Valor</span><span class="sxs-lookup"><span data-stu-id="969fe-143">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="969fe-144">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="969fe-144">Element type</span></span> | <span data-ttu-id="969fe-145">ComplexType [**GroupNodeType**](groupnodetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="969fe-145">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="969fe-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="969fe-146">Namespace</span></span>    | <span data-ttu-id="969fe-147">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="969fe-147">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="969fe-148">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="969fe-148">Schema name</span></span>  | <span data-ttu-id="969fe-149">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="969fe-149">Journal Reader</span></span>                                                  |



 

 

 



