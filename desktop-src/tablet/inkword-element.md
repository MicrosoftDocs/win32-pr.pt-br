---
description: Contém informações sobre uma determinada palavra de tinta na nota do diário, incluindo posição, alternativas e dados reais de tinta.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782624"
---
# <a name="inkword-element"></a><span data-ttu-id="5eec1-103">Elemento InkWord</span><span class="sxs-lookup"><span data-stu-id="5eec1-103">InkWord Element</span></span>

<span data-ttu-id="5eec1-104">Contém informações sobre uma determinada palavra de tinta na nota do diário, incluindo posição, alternativas e dados reais de tinta.</span><span class="sxs-lookup"><span data-stu-id="5eec1-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="5eec1-105">Definição</span><span class="sxs-lookup"><span data-stu-id="5eec1-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="5eec1-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5eec1-106">Parent Elements</span></span>

[<span data-ttu-id="5eec1-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="5eec1-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="5eec1-108">**Linha**</span><span class="sxs-lookup"><span data-stu-id="5eec1-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="5eec1-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5eec1-109">Child Elements</span></span>

[<span data-ttu-id="5eec1-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="5eec1-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="5eec1-111">**Alternativolist**</span><span class="sxs-lookup"><span data-stu-id="5eec1-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="5eec1-112">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="5eec1-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="5eec1-113">**Confiança**</span><span class="sxs-lookup"><span data-stu-id="5eec1-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="5eec1-114">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="5eec1-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="5eec1-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="5eec1-115">Attributes</span></span>



| <span data-ttu-id="5eec1-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="5eec1-116">Attribute</span></span>  | <span data-ttu-id="5eec1-117">Type</span><span class="sxs-lookup"><span data-stu-id="5eec1-117">Type</span></span>                      | <span data-ttu-id="5eec1-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5eec1-118">Required</span></span> | <span data-ttu-id="5eec1-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="5eec1-119">Description</span></span>                                                                             | <span data-ttu-id="5eec1-120">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5eec1-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="5eec1-121">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="5eec1-121">**Left**</span></span>   | <span data-ttu-id="5eec1-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5eec1-122">**xs:integer**</span></span>            | <span data-ttu-id="5eec1-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5eec1-123">Required</span></span> | <span data-ttu-id="5eec1-124">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5eec1-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="5eec1-125">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="5eec1-125">Any integer.</span></span>              |
| <span data-ttu-id="5eec1-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="5eec1-126">**Top**</span></span>    | <span data-ttu-id="5eec1-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5eec1-127">**xs:integer**</span></span>            | <span data-ttu-id="5eec1-128">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5eec1-128">Required</span></span> | <span data-ttu-id="5eec1-129">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5eec1-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="5eec1-130">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="5eec1-130">Any integer.</span></span>              |
| <span data-ttu-id="5eec1-131">**Largura**</span><span class="sxs-lookup"><span data-stu-id="5eec1-131">**Width**</span></span>  | <span data-ttu-id="5eec1-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5eec1-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5eec1-133">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5eec1-133">Required</span></span> | <span data-ttu-id="5eec1-134">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5eec1-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="5eec1-135">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="5eec1-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="5eec1-136">**Altura**</span><span class="sxs-lookup"><span data-stu-id="5eec1-136">**Height**</span></span> | <span data-ttu-id="5eec1-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5eec1-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5eec1-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5eec1-138">Required</span></span> | <span data-ttu-id="5eec1-139">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5eec1-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="5eec1-140">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="5eec1-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="5eec1-141">O mapeamento de coordenadas internas da palavra de tinta é a unidade de métrica em inglês e um multiplicador de 2,54 precisará ser usado pelo seu aplicativo para converter os valores de largura e altura nas unidades HIMETRIC usadas pelas APIs da plataforma do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="5eec1-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="5eec1-142">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5eec1-142">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="5eec1-143">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5eec1-143">Element type</span></span> | <span data-ttu-id="5eec1-144">ComplexType [**InkWordType**](inkwordtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="5eec1-144">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="5eec1-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="5eec1-145">Namespace</span></span>    | <span data-ttu-id="5eec1-146">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="5eec1-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="5eec1-147">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="5eec1-147">Schema name</span></span>  | <span data-ttu-id="5eec1-148">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="5eec1-148">Journal Reader</span></span>                                              |



 

 

 



