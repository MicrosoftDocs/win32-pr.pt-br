---
description: Contém o conteúdo que foi classificado pelo analisador ou pelo usuário como um desenho.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Elemento Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe516a4ba33e6e597b17ce8365d792f19468c3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790541"
---
# <a name="drawing-element"></a><span data-ttu-id="bad9f-103">Elemento Drawing</span><span class="sxs-lookup"><span data-stu-id="bad9f-103">Drawing Element</span></span>

<span data-ttu-id="bad9f-104">Contém o conteúdo que foi classificado pelo analisador ou pelo usuário como um desenho.</span><span class="sxs-lookup"><span data-stu-id="bad9f-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="bad9f-105">Definição</span><span class="sxs-lookup"><span data-stu-id="bad9f-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="bad9f-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="bad9f-106">Parent Elements</span></span>

[<span data-ttu-id="bad9f-107">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="bad9f-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="bad9f-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="bad9f-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="bad9f-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bad9f-109">Child Elements</span></span>

[<span data-ttu-id="bad9f-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="bad9f-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="bad9f-111">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="bad9f-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="bad9f-112">**InkClass**</span><span class="sxs-lookup"><span data-stu-id="bad9f-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="bad9f-113">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="bad9f-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="bad9f-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="bad9f-114">Attributes</span></span>



| <span data-ttu-id="bad9f-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="bad9f-115">Attribute</span></span>  | <span data-ttu-id="bad9f-116">Type</span><span class="sxs-lookup"><span data-stu-id="bad9f-116">Type</span></span>                      | <span data-ttu-id="bad9f-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bad9f-117">Required</span></span> | <span data-ttu-id="bad9f-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="bad9f-118">Description</span></span>                                                                             | <span data-ttu-id="bad9f-119">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="bad9f-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="bad9f-120">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="bad9f-120">**Left**</span></span>   | <span data-ttu-id="bad9f-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="bad9f-121">**xs:integer**</span></span>            | <span data-ttu-id="bad9f-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bad9f-122">Required</span></span> | <span data-ttu-id="bad9f-123">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="bad9f-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="bad9f-124">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="bad9f-124">Any integer.</span></span>              |
| <span data-ttu-id="bad9f-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="bad9f-125">**Top**</span></span>    | <span data-ttu-id="bad9f-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="bad9f-126">**xs:integer**</span></span>            | <span data-ttu-id="bad9f-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bad9f-127">Required</span></span> | <span data-ttu-id="bad9f-128">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="bad9f-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="bad9f-129">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="bad9f-129">Any integer.</span></span>              |
| <span data-ttu-id="bad9f-130">**Largura**</span><span class="sxs-lookup"><span data-stu-id="bad9f-130">**Width**</span></span>  | <span data-ttu-id="bad9f-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="bad9f-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="bad9f-132">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bad9f-132">Required</span></span> | <span data-ttu-id="bad9f-133">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="bad9f-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="bad9f-134">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="bad9f-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="bad9f-135">**Altura**</span><span class="sxs-lookup"><span data-stu-id="bad9f-135">**Height**</span></span> | <span data-ttu-id="bad9f-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="bad9f-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="bad9f-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bad9f-137">Required</span></span> | <span data-ttu-id="bad9f-138">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="bad9f-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="bad9f-139">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="bad9f-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="bad9f-140">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="bad9f-140">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="bad9f-141">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="bad9f-141">Element type</span></span> | <span data-ttu-id="bad9f-142">ComplexType de [**drawingtype**](drawingtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="bad9f-142">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="bad9f-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="bad9f-143">Namespace</span></span>    | <span data-ttu-id="bad9f-144">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="bad9f-144">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="bad9f-145">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="bad9f-145">Schema name</span></span>  | <span data-ttu-id="bad9f-146">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="bad9f-146">Journal Reader</span></span>                                              |



 

 

 



