---
description: Contém informações sobre uma determinada palavra de tinta na nota Do diário, incluindo posição, alternativas e os dados reais de tinta.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dc9baea7cda0346e82c11331c45f453e61f192
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432388"
---
# <a name="inkword-element"></a><span data-ttu-id="71278-103">Elemento InkWord</span><span class="sxs-lookup"><span data-stu-id="71278-103">InkWord Element</span></span>

<span data-ttu-id="71278-104">Contém informações sobre uma determinada palavra de tinta na nota Do diário, incluindo posição, alternativas e os dados reais de tinta.</span><span class="sxs-lookup"><span data-stu-id="71278-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="71278-105">Definição</span><span class="sxs-lookup"><span data-stu-id="71278-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="71278-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="71278-106">Parent Elements</span></span>

[<span data-ttu-id="71278-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="71278-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="71278-108">**Linha**</span><span class="sxs-lookup"><span data-stu-id="71278-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="71278-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="71278-109">Child Elements</span></span>

[<span data-ttu-id="71278-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="71278-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="71278-111">**AlternateList**</span><span class="sxs-lookup"><span data-stu-id="71278-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="71278-112">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="71278-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="71278-113">**Confiança**</span><span class="sxs-lookup"><span data-stu-id="71278-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="71278-114">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="71278-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="71278-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="71278-115">Attributes</span></span>



| <span data-ttu-id="71278-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="71278-116">Attribute</span></span>  | <span data-ttu-id="71278-117">Type</span><span class="sxs-lookup"><span data-stu-id="71278-117">Type</span></span>                      | <span data-ttu-id="71278-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="71278-118">Required</span></span> | <span data-ttu-id="71278-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="71278-119">Description</span></span>                                                                             | <span data-ttu-id="71278-120">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="71278-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="71278-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="71278-121">**Left**</span></span>   | <span data-ttu-id="71278-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="71278-122">**xs:integer**</span></span>            | <span data-ttu-id="71278-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="71278-123">Required</span></span> | <span data-ttu-id="71278-124">A distância da origem até o ponto mais à esquerda na caixa delimitante do elemento.</span><span class="sxs-lookup"><span data-stu-id="71278-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="71278-125">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="71278-125">Any integer.</span></span>              |
| <span data-ttu-id="71278-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="71278-126">**Top**</span></span>    | <span data-ttu-id="71278-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="71278-127">**xs:integer**</span></span>            | <span data-ttu-id="71278-128">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="71278-128">Required</span></span> | <span data-ttu-id="71278-129">A distância da origem até o ponto mais alto na caixa delimitada do elemento.</span><span class="sxs-lookup"><span data-stu-id="71278-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="71278-130">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="71278-130">Any integer.</span></span>              |
| <span data-ttu-id="71278-131">**Largura**</span><span class="sxs-lookup"><span data-stu-id="71278-131">**Width**</span></span>  | <span data-ttu-id="71278-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="71278-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="71278-133">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="71278-133">Required</span></span> | <span data-ttu-id="71278-134">A largura da caixa delimitada para o elemento.</span><span class="sxs-lookup"><span data-stu-id="71278-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="71278-135">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="71278-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="71278-136">**Altura**</span><span class="sxs-lookup"><span data-stu-id="71278-136">**Height**</span></span> | <span data-ttu-id="71278-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="71278-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="71278-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="71278-138">Required</span></span> | <span data-ttu-id="71278-139">A altura da caixa delimitada para o elemento.</span><span class="sxs-lookup"><span data-stu-id="71278-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="71278-140">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="71278-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="71278-141">O mapeamento de coordenadas interno da palavra de tinta é Unidades de Métrica em Inglês e um multiplicador de 2,54 precisará ser usado pelo seu aplicativo para converter os valores de Largura e Altura nas unidades HIMETRIC usadas pelas APIs da plataforma tablet PC.</span><span class="sxs-lookup"><span data-stu-id="71278-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="71278-142">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="71278-142">Element Information</span></span>



|  <span data-ttu-id="71278-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="71278-143">Element</span></span>     | <span data-ttu-id="71278-144">Valor</span><span class="sxs-lookup"><span data-stu-id="71278-144">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="71278-145">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="71278-145">Element type</span></span> | <span data-ttu-id="71278-146">[**ComplexType InkWordType**](inkwordtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="71278-146">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="71278-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="71278-147">Namespace</span></span>    | <span data-ttu-id="71278-148">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="71278-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="71278-149">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="71278-149">Schema name</span></span>  | <span data-ttu-id="71278-150">Leitor de Diário</span><span class="sxs-lookup"><span data-stu-id="71278-150">Journal Reader</span></span>                                              |



 

 

 



