---
description: Contém informações de formatação para as linhas horizontais usadas para o papel de carta em uma nota do diário.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e380ca35f86ce1012084d31de732cd66c79363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647248"
---
# <a name="horizontal-element"></a><span data-ttu-id="2bf17-103">Elemento horizontal</span><span class="sxs-lookup"><span data-stu-id="2bf17-103">Horizontal Element</span></span>

<span data-ttu-id="2bf17-104">Contém informações de formatação para as linhas horizontais usadas para o papel de carta em uma nota do diário.</span><span class="sxs-lookup"><span data-stu-id="2bf17-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="2bf17-105">Definição</span><span class="sxs-lookup"><span data-stu-id="2bf17-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="2bf17-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2bf17-106">Parent Elements</span></span>

[<span data-ttu-id="2bf17-107">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="2bf17-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="2bf17-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2bf17-108">Child Elements</span></span>

<span data-ttu-id="2bf17-109">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2bf17-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="2bf17-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2bf17-110">Attributes</span></span>



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
<th><span data-ttu-id="2bf17-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="2bf17-111">Attribute</span></span></th>
<th><span data-ttu-id="2bf17-112">Type</span><span class="sxs-lookup"><span data-stu-id="2bf17-112">Type</span></span></th>
<th><span data-ttu-id="2bf17-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2bf17-113">Required</span></span></th>
<th><span data-ttu-id="2bf17-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2bf17-114">Description</span></span></th>
<th><span data-ttu-id="2bf17-115">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="2bf17-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bf17-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="2bf17-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="2bf17-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="2bf17-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="2bf17-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2bf17-118">Required</span></span></td>
<td><span data-ttu-id="2bf17-119">Especifica o tipo de linha a ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="2bf17-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="2bf17-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2bf17-120">None</span></span></li>
<li><span data-ttu-id="2bf17-121">Sólido</span><span class="sxs-lookup"><span data-stu-id="2bf17-121">Solid</span></span></li>
<li><span data-ttu-id="2bf17-122">Traço</span><span class="sxs-lookup"><span data-stu-id="2bf17-122">Dash</span></span></li>
<li><span data-ttu-id="2bf17-123">Ponto</span><span class="sxs-lookup"><span data-stu-id="2bf17-123">Dot</span></span></li>
<li><span data-ttu-id="2bf17-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="2bf17-124">DashDot</span></span></li>
<li><span data-ttu-id="2bf17-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="2bf17-125">DashDotDot</span></span></li>
<li><span data-ttu-id="2bf17-126">Double</span><span class="sxs-lookup"><span data-stu-id="2bf17-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bf17-127"><strong>Cor</strong></span><span class="sxs-lookup"><span data-stu-id="2bf17-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="2bf17-128">SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bf17-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="2bf17-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="2bf17-129">Optional</span></span></td>
<td><span data-ttu-id="2bf17-130">Cor do elemento.</span><span class="sxs-lookup"><span data-stu-id="2bf17-130">Color of the element.</span></span></td>
<td><span data-ttu-id="2bf17-131">Um valor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="2bf17-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="2bf17-132">Corresponde à seguinte expressão regular: # [0-9A-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="2bf17-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="2bf17-133">Por exemplo, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="2bf17-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bf17-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="2bf17-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="2bf17-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="2bf17-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="2bf17-136">Opcional</span><span class="sxs-lookup"><span data-stu-id="2bf17-136">Optional</span></span></td>
<td><span data-ttu-id="2bf17-137">Espaçamento antes do elemento.</span><span class="sxs-lookup"><span data-stu-id="2bf17-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="2bf17-138">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="2bf17-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bf17-139"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="2bf17-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="2bf17-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="2bf17-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="2bf17-141">Opcional</span><span class="sxs-lookup"><span data-stu-id="2bf17-141">Optional</span></span></td>
<td><span data-ttu-id="2bf17-142">Espaçamento entre este elemento e elementos circundantes.</span><span class="sxs-lookup"><span data-stu-id="2bf17-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="2bf17-143">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="2bf17-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="2bf17-144">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2bf17-144">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="2bf17-145">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2bf17-145">Element type</span></span> | [<span data-ttu-id="2bf17-146">**ComplexType de horizontaltype**</span><span class="sxs-lookup"><span data-stu-id="2bf17-146">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="2bf17-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="2bf17-147">Namespace</span></span>    | <span data-ttu-id="2bf17-148">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="2bf17-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="2bf17-149">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="2bf17-149">Schema name</span></span>  | <span data-ttu-id="2bf17-150">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="2bf17-150">Journal Reader</span></span>                                                    |



 

 

 




