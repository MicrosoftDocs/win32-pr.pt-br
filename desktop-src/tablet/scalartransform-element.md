---
description: Transformação escalar usada pelo desenho ou InkWord.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: Elemento ScalarTransform
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ed5f7d3b44456522b45c7243b15390b7c52433
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432428"
---
# <a name="scalartransform-element"></a><span data-ttu-id="75162-103">Elemento ScalarTransform</span><span class="sxs-lookup"><span data-stu-id="75162-103">ScalarTransform Element</span></span>

<span data-ttu-id="75162-104">Transformação escalar usada pelo [**desenho**](drawing-element.md) ou [**InkWord**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="75162-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="75162-105">Definição</span><span class="sxs-lookup"><span data-stu-id="75162-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="75162-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="75162-106">Parent Elements</span></span>

[<span data-ttu-id="75162-107">**Desenho**</span><span class="sxs-lookup"><span data-stu-id="75162-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="75162-108">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="75162-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="75162-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="75162-109">Child Elements</span></span>

<span data-ttu-id="75162-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="75162-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="75162-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="75162-111">Attributes</span></span>



| <span data-ttu-id="75162-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="75162-112">Attribute</span></span> | <span data-ttu-id="75162-113">Type</span><span class="sxs-lookup"><span data-stu-id="75162-113">Type</span></span>           | <span data-ttu-id="75162-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="75162-114">Required</span></span> | <span data-ttu-id="75162-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="75162-115">Description</span></span> | <span data-ttu-id="75162-116">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="75162-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="75162-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="75162-117">**Mat1**</span></span>  | <span data-ttu-id="75162-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="75162-118">**xs:decimal**</span></span> | <span data-ttu-id="75162-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="75162-119">Required</span></span> |             | <span data-ttu-id="75162-120">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="75162-120">Any decimal number.</span></span> |
| <span data-ttu-id="75162-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="75162-121">**Mat2**</span></span>  | <span data-ttu-id="75162-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="75162-122">**xs:decimal**</span></span> | <span data-ttu-id="75162-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="75162-123">Required</span></span> |             | <span data-ttu-id="75162-124">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="75162-124">Any decimal number.</span></span> |
| <span data-ttu-id="75162-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="75162-125">**Mat3**</span></span>  | <span data-ttu-id="75162-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="75162-126">**xs:decimal**</span></span> | <span data-ttu-id="75162-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="75162-127">Required</span></span> |             | <span data-ttu-id="75162-128">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="75162-128">Any decimal number.</span></span> |
| <span data-ttu-id="75162-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="75162-129">**Mat4**</span></span>  | <span data-ttu-id="75162-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="75162-130">**xs:decimal**</span></span> | <span data-ttu-id="75162-131">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="75162-131">Required</span></span> |             | <span data-ttu-id="75162-132">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="75162-132">Any decimal number.</span></span> |
| <span data-ttu-id="75162-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="75162-133">**Mat5**</span></span>  | <span data-ttu-id="75162-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="75162-134">**xs:decimal**</span></span> | <span data-ttu-id="75162-135">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="75162-135">Required</span></span> |             | <span data-ttu-id="75162-136">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="75162-136">Any decimal number.</span></span> |
| <span data-ttu-id="75162-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="75162-137">**Mat6**</span></span>  | <span data-ttu-id="75162-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="75162-138">**xs:decimal**</span></span> | <span data-ttu-id="75162-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="75162-139">Required</span></span> |             | <span data-ttu-id="75162-140">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="75162-140">Any decimal number.</span></span> |
| <span data-ttu-id="75162-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="75162-141">**Mat7**</span></span>  | <span data-ttu-id="75162-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="75162-142">**xs:decimal**</span></span> | <span data-ttu-id="75162-143">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="75162-143">Required</span></span> |             | <span data-ttu-id="75162-144">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="75162-144">Any decimal number.</span></span> |
| <span data-ttu-id="75162-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="75162-145">**Mat8**</span></span>  | <span data-ttu-id="75162-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="75162-146">**xs:decimal**</span></span> | <span data-ttu-id="75162-147">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="75162-147">Required</span></span> |             | <span data-ttu-id="75162-148">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="75162-148">Any decimal number.</span></span> |
| <span data-ttu-id="75162-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="75162-149">**Mat9**</span></span>  | <span data-ttu-id="75162-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="75162-150">**xs:decimal**</span></span> | <span data-ttu-id="75162-151">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="75162-151">Required</span></span> |             | <span data-ttu-id="75162-152">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="75162-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="75162-153">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="75162-153">Element Information</span></span>



| <span data-ttu-id="75162-154">Elemento</span><span class="sxs-lookup"><span data-stu-id="75162-154">Element</span></span>      | <span data-ttu-id="75162-155">Valor</span><span class="sxs-lookup"><span data-stu-id="75162-155">Value</span></span>                                                                       |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="75162-156">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="75162-156">Element type</span></span> | <span data-ttu-id="75162-157">ComplexType [**ScalarTransformType**](scalartransformtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="75162-157">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="75162-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="75162-158">Namespace</span></span>    | <span data-ttu-id="75162-159">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="75162-159">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="75162-160">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="75162-160">Schema name</span></span>  | <span data-ttu-id="75162-161">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="75162-161">Journal Reader</span></span>                                                              |



 

 

 



