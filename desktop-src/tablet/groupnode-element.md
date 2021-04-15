---
description: Contém um conjunto de elementos&\# 8212; Parágrafo, InkWord, desenho, texto, imagem ou sinalizador&\# 8212; que são agrupados juntos na nota do diário.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento GroupNode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747473"
---
# <a name="groupnode-element"></a><span data-ttu-id="edd09-103">Elemento GroupNode</span><span class="sxs-lookup"><span data-stu-id="edd09-103">GroupNode Element</span></span>

<span data-ttu-id="edd09-104">Contém um conjunto de elementos ([**parágrafo**](paragraph-element.md), [**InkWord**](inkword-element.md), [**desenho**](drawing-element.md), [**texto**](text-element.md), [**imagem**](image-element.md)ou [**sinalizador**](flag-element.md)) que são agrupados na nota do diário.</span><span class="sxs-lookup"><span data-stu-id="edd09-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="edd09-105">Definição</span><span class="sxs-lookup"><span data-stu-id="edd09-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="edd09-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="edd09-106">Parent Elements</span></span>

[<span data-ttu-id="edd09-107">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="edd09-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="edd09-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="edd09-108">Child Elements</span></span>

[<span data-ttu-id="edd09-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="edd09-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="edd09-110">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="edd09-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="edd09-111">**Senha**</span><span class="sxs-lookup"><span data-stu-id="edd09-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="edd09-112">**Texto**</span><span class="sxs-lookup"><span data-stu-id="edd09-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="edd09-113">**Imagem**</span><span class="sxs-lookup"><span data-stu-id="edd09-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="edd09-114">**Sinalizador**</span><span class="sxs-lookup"><span data-stu-id="edd09-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="edd09-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="edd09-115">Attributes</span></span>



| <span data-ttu-id="edd09-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="edd09-116">Attribute</span></span>  | <span data-ttu-id="edd09-117">Type</span><span class="sxs-lookup"><span data-stu-id="edd09-117">Type</span></span>                      | <span data-ttu-id="edd09-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="edd09-118">Required</span></span> | <span data-ttu-id="edd09-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="edd09-119">Description</span></span>                                                                             | <span data-ttu-id="edd09-120">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="edd09-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="edd09-121">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="edd09-121">**Left**</span></span>   | <span data-ttu-id="edd09-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="edd09-122">**xs:integer**</span></span>            | <span data-ttu-id="edd09-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="edd09-123">Required</span></span> | <span data-ttu-id="edd09-124">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="edd09-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="edd09-125">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="edd09-125">Any integer.</span></span>              |
| <span data-ttu-id="edd09-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="edd09-126">**Top**</span></span>    | <span data-ttu-id="edd09-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="edd09-127">**xs:integer**</span></span>            | <span data-ttu-id="edd09-128">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="edd09-128">Required</span></span> | <span data-ttu-id="edd09-129">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="edd09-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="edd09-130">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="edd09-130">Any integer.</span></span>              |
| <span data-ttu-id="edd09-131">**Largura**</span><span class="sxs-lookup"><span data-stu-id="edd09-131">**Width**</span></span>  | <span data-ttu-id="edd09-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="edd09-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="edd09-133">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="edd09-133">Required</span></span> | <span data-ttu-id="edd09-134">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="edd09-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="edd09-135">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="edd09-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="edd09-136">**Altura**</span><span class="sxs-lookup"><span data-stu-id="edd09-136">**Height**</span></span> | <span data-ttu-id="edd09-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="edd09-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="edd09-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="edd09-138">Required</span></span> | <span data-ttu-id="edd09-139">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="edd09-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="edd09-140">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="edd09-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="edd09-141">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="edd09-141">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="edd09-142">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="edd09-142">Element type</span></span> | <span data-ttu-id="edd09-143">ComplexType [**GroupNodeType**](groupnodetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="edd09-143">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="edd09-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="edd09-144">Namespace</span></span>    | <span data-ttu-id="edd09-145">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="edd09-145">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="edd09-146">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="edd09-146">Schema name</span></span>  | <span data-ttu-id="edd09-147">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="edd09-147">Journal Reader</span></span>                                                  |



 

 

 



