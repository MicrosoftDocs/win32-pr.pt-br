---
description: Contém informações de formatação para as linhas horizontais usadas para a papelaria em uma nota de Diário.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de08008d0243d27f8a8c5f64d6aeac5ddbcc1c
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432368"
---
# <a name="horizontal-element"></a><span data-ttu-id="da0a4-103">Elemento Horizontal</span><span class="sxs-lookup"><span data-stu-id="da0a4-103">Horizontal Element</span></span>

<span data-ttu-id="da0a4-104">Contém informações de formatação para as linhas horizontais usadas para a papelaria em uma nota de Diário.</span><span class="sxs-lookup"><span data-stu-id="da0a4-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="da0a4-105">Definição</span><span class="sxs-lookup"><span data-stu-id="da0a4-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="da0a4-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="da0a4-106">Parent Elements</span></span>

[<span data-ttu-id="da0a4-107">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="da0a4-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="da0a4-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="da0a4-108">Child Elements</span></span>

<span data-ttu-id="da0a4-109">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="da0a4-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="da0a4-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="da0a4-110">Attributes</span></span>



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da0a4-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="da0a4-111">Attribute</span></span></th>
<th><span data-ttu-id="da0a4-112">Type</span><span class="sxs-lookup"><span data-stu-id="da0a4-112">Type</span></span></th>
<th><span data-ttu-id="da0a4-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="da0a4-113">Required</span></span></th>
<th><span data-ttu-id="da0a4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="da0a4-114">Description</span></span></th>
<th><span data-ttu-id="da0a4-115">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="da0a4-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="da0a4-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="da0a4-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="da0a4-117"><a href="linelayoutstyletype-simple-type.md"><strong>SimpleType LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="da0a4-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="da0a4-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="da0a4-118">Required</span></span></td>
<td><span data-ttu-id="da0a4-119">Especifica o tipo de linha a ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="da0a4-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="da0a4-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="da0a4-120">None</span></span></li>
<li><span data-ttu-id="da0a4-121">Sólido</span><span class="sxs-lookup"><span data-stu-id="da0a4-121">Solid</span></span></li>
<li><span data-ttu-id="da0a4-122">Traço</span><span class="sxs-lookup"><span data-stu-id="da0a4-122">Dash</span></span></li>
<li><span data-ttu-id="da0a4-123">Ponto</span><span class="sxs-lookup"><span data-stu-id="da0a4-123">Dot</span></span></li>
<li><span data-ttu-id="da0a4-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="da0a4-124">DashDot</span></span></li>
<li><span data-ttu-id="da0a4-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="da0a4-125">DashDotDot</span></span></li>
<li><span data-ttu-id="da0a4-126">Double</span><span class="sxs-lookup"><span data-stu-id="da0a4-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da0a4-127"><strong>Cor</strong></span><span class="sxs-lookup"><span data-stu-id="da0a4-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="da0a4-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="da0a4-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="da0a4-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="da0a4-129">Optional</span></span></td>
<td><span data-ttu-id="da0a4-130">Cor do elemento.</span><span class="sxs-lookup"><span data-stu-id="da0a4-130">Color of the element.</span></span></td>
<td><span data-ttu-id="da0a4-131">Um valor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="da0a4-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="da0a4-132">Corresponde à seguinte expressão regular: #[0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="da0a4-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="da0a4-133">Por exemplo, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="da0a4-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da0a4-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="da0a4-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="da0a4-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="da0a4-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="da0a4-136">Opcional</span><span class="sxs-lookup"><span data-stu-id="da0a4-136">Optional</span></span></td>
<td><span data-ttu-id="da0a4-137">Espaçamento antes do elemento .</span><span class="sxs-lookup"><span data-stu-id="da0a4-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="da0a4-138">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="da0a4-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da0a4-139"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="da0a4-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="da0a4-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="da0a4-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="da0a4-141">Opcional</span><span class="sxs-lookup"><span data-stu-id="da0a4-141">Optional</span></span></td>
<td><span data-ttu-id="da0a4-142">Espaçamento entre esse elemento e elementos ao redor.</span><span class="sxs-lookup"><span data-stu-id="da0a4-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="da0a4-143">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="da0a4-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="da0a4-144">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="da0a4-144">Element Information</span></span>



|  <span data-ttu-id="da0a4-145">Elemento</span><span class="sxs-lookup"><span data-stu-id="da0a4-145">Element</span></span>     | <span data-ttu-id="da0a4-146">Valor</span><span class="sxs-lookup"><span data-stu-id="da0a4-146">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="da0a4-147">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="da0a4-147">Element type</span></span> | [<span data-ttu-id="da0a4-148">**ComplexType HorizontalType**</span><span class="sxs-lookup"><span data-stu-id="da0a4-148">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="da0a4-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="da0a4-149">Namespace</span></span>    | <span data-ttu-id="da0a4-150">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="da0a4-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="da0a4-151">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="da0a4-151">Schema name</span></span>  | <span data-ttu-id="da0a4-152">Leitor de Diário</span><span class="sxs-lookup"><span data-stu-id="da0a4-152">Journal Reader</span></span>                                                    |



 

 

 




