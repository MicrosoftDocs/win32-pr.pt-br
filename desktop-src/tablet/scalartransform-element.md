---
description: Transformação escalar usada pelo desenho ou InkWord.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: Elemento ScalarTransform
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5853c0fab76cd5a4857ae0235127a2fe103872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768388"
---
# <a name="scalartransform-element"></a><span data-ttu-id="c1ecc-103">Elemento ScalarTransform</span><span class="sxs-lookup"><span data-stu-id="c1ecc-103">ScalarTransform Element</span></span>

<span data-ttu-id="c1ecc-104">Transformação escalar usada pelo [**desenho**](drawing-element.md) ou [**InkWord**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="c1ecc-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="c1ecc-105">Definição</span><span class="sxs-lookup"><span data-stu-id="c1ecc-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="c1ecc-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c1ecc-106">Parent Elements</span></span>

[<span data-ttu-id="c1ecc-107">**Senha**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="c1ecc-108">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="c1ecc-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c1ecc-109">Child Elements</span></span>

<span data-ttu-id="c1ecc-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c1ecc-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="c1ecc-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1ecc-111">Attributes</span></span>



| <span data-ttu-id="c1ecc-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="c1ecc-112">Attribute</span></span> | <span data-ttu-id="c1ecc-113">Type</span><span class="sxs-lookup"><span data-stu-id="c1ecc-113">Type</span></span>           | <span data-ttu-id="c1ecc-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c1ecc-114">Required</span></span> | <span data-ttu-id="c1ecc-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ecc-115">Description</span></span> | <span data-ttu-id="c1ecc-116">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="c1ecc-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="c1ecc-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-117">**Mat1**</span></span>  | <span data-ttu-id="c1ecc-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-118">**xs:decimal**</span></span> | <span data-ttu-id="c1ecc-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c1ecc-119">Required</span></span> |             | <span data-ttu-id="c1ecc-120">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="c1ecc-120">Any decimal number.</span></span> |
| <span data-ttu-id="c1ecc-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-121">**Mat2**</span></span>  | <span data-ttu-id="c1ecc-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-122">**xs:decimal**</span></span> | <span data-ttu-id="c1ecc-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c1ecc-123">Required</span></span> |             | <span data-ttu-id="c1ecc-124">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="c1ecc-124">Any decimal number.</span></span> |
| <span data-ttu-id="c1ecc-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-125">**Mat3**</span></span>  | <span data-ttu-id="c1ecc-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-126">**xs:decimal**</span></span> | <span data-ttu-id="c1ecc-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c1ecc-127">Required</span></span> |             | <span data-ttu-id="c1ecc-128">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="c1ecc-128">Any decimal number.</span></span> |
| <span data-ttu-id="c1ecc-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-129">**Mat4**</span></span>  | <span data-ttu-id="c1ecc-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-130">**xs:decimal**</span></span> | <span data-ttu-id="c1ecc-131">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c1ecc-131">Required</span></span> |             | <span data-ttu-id="c1ecc-132">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="c1ecc-132">Any decimal number.</span></span> |
| <span data-ttu-id="c1ecc-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-133">**Mat5**</span></span>  | <span data-ttu-id="c1ecc-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-134">**xs:decimal**</span></span> | <span data-ttu-id="c1ecc-135">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c1ecc-135">Required</span></span> |             | <span data-ttu-id="c1ecc-136">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="c1ecc-136">Any decimal number.</span></span> |
| <span data-ttu-id="c1ecc-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-137">**Mat6**</span></span>  | <span data-ttu-id="c1ecc-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-138">**xs:decimal**</span></span> | <span data-ttu-id="c1ecc-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c1ecc-139">Required</span></span> |             | <span data-ttu-id="c1ecc-140">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="c1ecc-140">Any decimal number.</span></span> |
| <span data-ttu-id="c1ecc-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-141">**Mat7**</span></span>  | <span data-ttu-id="c1ecc-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-142">**xs:decimal**</span></span> | <span data-ttu-id="c1ecc-143">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c1ecc-143">Required</span></span> |             | <span data-ttu-id="c1ecc-144">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="c1ecc-144">Any decimal number.</span></span> |
| <span data-ttu-id="c1ecc-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-145">**Mat8**</span></span>  | <span data-ttu-id="c1ecc-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-146">**xs:decimal**</span></span> | <span data-ttu-id="c1ecc-147">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c1ecc-147">Required</span></span> |             | <span data-ttu-id="c1ecc-148">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="c1ecc-148">Any decimal number.</span></span> |
| <span data-ttu-id="c1ecc-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-149">**Mat9**</span></span>  | <span data-ttu-id="c1ecc-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="c1ecc-150">**xs:decimal**</span></span> | <span data-ttu-id="c1ecc-151">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c1ecc-151">Required</span></span> |             | <span data-ttu-id="c1ecc-152">Qualquer número decimal.</span><span class="sxs-lookup"><span data-stu-id="c1ecc-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="c1ecc-153">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c1ecc-153">Element Information</span></span>



|              |                                                                             |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="c1ecc-154">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c1ecc-154">Element type</span></span> | <span data-ttu-id="c1ecc-155">ComplexType [**ScalarTransformType**](scalartransformtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="c1ecc-155">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="c1ecc-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1ecc-156">Namespace</span></span>    | <span data-ttu-id="c1ecc-157">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="c1ecc-157">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="c1ecc-158">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="c1ecc-158">Schema name</span></span>  | <span data-ttu-id="c1ecc-159">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="c1ecc-159">Journal Reader</span></span>                                                              |



 

 

 



