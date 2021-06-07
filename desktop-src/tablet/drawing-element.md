---
description: Contém o conteúdo que foi classificado pelo analisador ou pelo usuário como um desenho.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Elemento Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87c0a3d8879fb5f3146c46c9c88d83a6e658d8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432508"
---
# <a name="drawing-element"></a><span data-ttu-id="d4b87-103">Elemento Drawing</span><span class="sxs-lookup"><span data-stu-id="d4b87-103">Drawing Element</span></span>

<span data-ttu-id="d4b87-104">Contém o conteúdo que foi classificado pelo analisador ou pelo usuário como um desenho.</span><span class="sxs-lookup"><span data-stu-id="d4b87-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="d4b87-105">Definição</span><span class="sxs-lookup"><span data-stu-id="d4b87-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="d4b87-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d4b87-106">Parent Elements</span></span>

[<span data-ttu-id="d4b87-107">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="d4b87-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="d4b87-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="d4b87-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="d4b87-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d4b87-109">Child Elements</span></span>

[<span data-ttu-id="d4b87-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="d4b87-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="d4b87-111">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="d4b87-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="d4b87-112">**InkClass**</span><span class="sxs-lookup"><span data-stu-id="d4b87-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="d4b87-113">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="d4b87-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="d4b87-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="d4b87-114">Attributes</span></span>



| <span data-ttu-id="d4b87-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="d4b87-115">Attribute</span></span>  | <span data-ttu-id="d4b87-116">Type</span><span class="sxs-lookup"><span data-stu-id="d4b87-116">Type</span></span>                      | <span data-ttu-id="d4b87-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d4b87-117">Required</span></span> | <span data-ttu-id="d4b87-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4b87-118">Description</span></span>                                                                             | <span data-ttu-id="d4b87-119">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="d4b87-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="d4b87-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="d4b87-120">**Left**</span></span>   | <span data-ttu-id="d4b87-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="d4b87-121">**xs:integer**</span></span>            | <span data-ttu-id="d4b87-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d4b87-122">Required</span></span> | <span data-ttu-id="d4b87-123">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="d4b87-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="d4b87-124">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="d4b87-124">Any integer.</span></span>              |
| <span data-ttu-id="d4b87-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="d4b87-125">**Top**</span></span>    | <span data-ttu-id="d4b87-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="d4b87-126">**xs:integer**</span></span>            | <span data-ttu-id="d4b87-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d4b87-127">Required</span></span> | <span data-ttu-id="d4b87-128">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="d4b87-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="d4b87-129">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="d4b87-129">Any integer.</span></span>              |
| <span data-ttu-id="d4b87-130">**Largura**</span><span class="sxs-lookup"><span data-stu-id="d4b87-130">**Width**</span></span>  | <span data-ttu-id="d4b87-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="d4b87-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="d4b87-132">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d4b87-132">Required</span></span> | <span data-ttu-id="d4b87-133">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="d4b87-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="d4b87-134">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="d4b87-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="d4b87-135">**Altura**</span><span class="sxs-lookup"><span data-stu-id="d4b87-135">**Height**</span></span> | <span data-ttu-id="d4b87-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="d4b87-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="d4b87-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d4b87-137">Required</span></span> | <span data-ttu-id="d4b87-138">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="d4b87-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="d4b87-139">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="d4b87-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="d4b87-140">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d4b87-140">Element Information</span></span>



|  <span data-ttu-id="d4b87-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="d4b87-141">Element</span></span>     | <span data-ttu-id="d4b87-142">Valor</span><span class="sxs-lookup"><span data-stu-id="d4b87-142">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="d4b87-143">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d4b87-143">Element type</span></span> | <span data-ttu-id="d4b87-144">ComplexType de [**drawingtype**](drawingtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="d4b87-144">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="d4b87-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4b87-145">Namespace</span></span>    | <span data-ttu-id="d4b87-146">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="d4b87-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="d4b87-147">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="d4b87-147">Schema name</span></span>  | <span data-ttu-id="d4b87-148">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="d4b87-148">Journal Reader</span></span>                                              |



 

 

 



