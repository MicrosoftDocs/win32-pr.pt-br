---
description: Contém as informações que descrevem o componente vertical das linhas no papel de carta usado pela anotação do diário. Usado, por exemplo, quando a observação tem linhas de grade.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Elemento vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191a9c5cb3190cff9b1e379a68dbfab49ddc25a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296303"
---
# <a name="vertical-element"></a><span data-ttu-id="10914-104">Elemento vertical</span><span class="sxs-lookup"><span data-stu-id="10914-104">Vertical Element</span></span>

<span data-ttu-id="10914-105">Contém as informações que descrevem o componente vertical das linhas no papel de carta usado pela anotação do diário.</span><span class="sxs-lookup"><span data-stu-id="10914-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="10914-106">Usado, por exemplo, quando a observação tem linhas de grade.</span><span class="sxs-lookup"><span data-stu-id="10914-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="10914-107">Definição</span><span class="sxs-lookup"><span data-stu-id="10914-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="10914-108">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="10914-108">Parent Elements</span></span>

[<span data-ttu-id="10914-109">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="10914-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="10914-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="10914-110">Child Elements</span></span>

<span data-ttu-id="10914-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="10914-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="10914-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="10914-112">Attributes</span></span>



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
<th><span data-ttu-id="10914-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="10914-113">Attribute</span></span></th>
<th><span data-ttu-id="10914-114">Type</span><span class="sxs-lookup"><span data-stu-id="10914-114">Type</span></span></th>
<th><span data-ttu-id="10914-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="10914-115">Required</span></span></th>
<th><span data-ttu-id="10914-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="10914-116">Description</span></span></th>
<th><span data-ttu-id="10914-117">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="10914-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10914-118"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="10914-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="10914-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="10914-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="10914-120">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="10914-120">Required</span></span></td>
<td><span data-ttu-id="10914-121">Especifica o tipo de linha a ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="10914-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="10914-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="10914-122">None</span></span></li>
<li><span data-ttu-id="10914-123">Sólido</span><span class="sxs-lookup"><span data-stu-id="10914-123">Solid</span></span></li>
<li><span data-ttu-id="10914-124">Traço</span><span class="sxs-lookup"><span data-stu-id="10914-124">Dash</span></span></li>
<li><span data-ttu-id="10914-125">Ponto</span><span class="sxs-lookup"><span data-stu-id="10914-125">Dot</span></span></li>
<li><span data-ttu-id="10914-126">DashDot</span><span class="sxs-lookup"><span data-stu-id="10914-126">DashDot</span></span></li>
<li><span data-ttu-id="10914-127">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="10914-127">DashDotDot</span></span></li>
<li><span data-ttu-id="10914-128">Double</span><span class="sxs-lookup"><span data-stu-id="10914-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10914-129"><strong>Cor</strong></span><span class="sxs-lookup"><span data-stu-id="10914-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="10914-130">SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="10914-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="10914-131">Opcional</span><span class="sxs-lookup"><span data-stu-id="10914-131">Optional</span></span></td>
<td><span data-ttu-id="10914-132">Cor do elemento.</span><span class="sxs-lookup"><span data-stu-id="10914-132">Color of the element.</span></span></td>
<td><span data-ttu-id="10914-133">Um valor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="10914-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="10914-134">Corresponde à seguinte expressão regular: # [0-9A-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="10914-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="10914-135">Por exemplo, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="10914-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10914-136"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="10914-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="10914-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="10914-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="10914-138">Opcional</span><span class="sxs-lookup"><span data-stu-id="10914-138">Optional</span></span></td>
<td><span data-ttu-id="10914-139">Espaçamento antes do elemento.</span><span class="sxs-lookup"><span data-stu-id="10914-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="10914-140">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="10914-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10914-141"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="10914-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="10914-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="10914-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="10914-143">Opcional</span><span class="sxs-lookup"><span data-stu-id="10914-143">Optional</span></span></td>
<td><span data-ttu-id="10914-144">Espaçamento entre este elemento e elementos circundantes.</span><span class="sxs-lookup"><span data-stu-id="10914-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="10914-145">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="10914-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="10914-146">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="10914-146">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="10914-147">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="10914-147">Element type</span></span> | <span data-ttu-id="10914-148">ComplexType de [**verticaltype**](verticaltype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="10914-148">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="10914-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="10914-149">Namespace</span></span>    | <span data-ttu-id="10914-150">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="10914-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="10914-151">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="10914-151">Schema name</span></span>  | <span data-ttu-id="10914-152">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="10914-152">Journal Reader</span></span>                                                |



 

 

 




