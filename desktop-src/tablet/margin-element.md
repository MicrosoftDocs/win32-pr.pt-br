---
description: Define as linhas de margem desenhadas na página.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Elemento Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547177a10fc3724f3b9bf3dde65f857d03f0f2a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432128"
---
# <a name="margin-element"></a><span data-ttu-id="31edb-103">Elemento Margin</span><span class="sxs-lookup"><span data-stu-id="31edb-103">Margin Element</span></span>

<span data-ttu-id="31edb-104">Define as linhas de margem desenhadas na página.</span><span class="sxs-lookup"><span data-stu-id="31edb-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="31edb-105">Definição</span><span class="sxs-lookup"><span data-stu-id="31edb-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="31edb-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="31edb-106">Parent Elements</span></span>

<span data-ttu-id="31edb-107">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="31edb-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="31edb-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="31edb-108">Child Elements</span></span>

<span data-ttu-id="31edb-109">Nenhum..</span><span class="sxs-lookup"><span data-stu-id="31edb-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="31edb-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="31edb-110">Attributes</span></span>



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
<th><span data-ttu-id="31edb-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="31edb-111">Attribute</span></span></th>
<th><span data-ttu-id="31edb-112">Type</span><span class="sxs-lookup"><span data-stu-id="31edb-112">Type</span></span></th>
<th><span data-ttu-id="31edb-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="31edb-113">Required</span></span></th>
<th><span data-ttu-id="31edb-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="31edb-114">Description</span></span></th>
<th><span data-ttu-id="31edb-115">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="31edb-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31edb-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="31edb-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="31edb-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="31edb-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="31edb-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="31edb-118">Required</span></span></td>
<td><span data-ttu-id="31edb-119">Especifica o tipo de linha a ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="31edb-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="31edb-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="31edb-120">None</span></span></li>
<li><span data-ttu-id="31edb-121">Sólido</span><span class="sxs-lookup"><span data-stu-id="31edb-121">Solid</span></span></li>
<li><span data-ttu-id="31edb-122">Traço</span><span class="sxs-lookup"><span data-stu-id="31edb-122">Dash</span></span></li>
<li><span data-ttu-id="31edb-123">Ponto</span><span class="sxs-lookup"><span data-stu-id="31edb-123">Dot</span></span></li>
<li><span data-ttu-id="31edb-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="31edb-124">DashDot</span></span></li>
<li><span data-ttu-id="31edb-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="31edb-125">DashDotDot</span></span></li>
<li><span data-ttu-id="31edb-126">Double</span><span class="sxs-lookup"><span data-stu-id="31edb-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31edb-127"><strong>Cor</strong></span><span class="sxs-lookup"><span data-stu-id="31edb-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="31edb-128">SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="31edb-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="31edb-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="31edb-129">Optional</span></span></td>
<td><span data-ttu-id="31edb-130">Cor do elemento.</span><span class="sxs-lookup"><span data-stu-id="31edb-130">Color of the element.</span></span></td>
<td><span data-ttu-id="31edb-131">Um valor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="31edb-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="31edb-132">Corresponde à seguinte expressão regular: # [0-9A-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="31edb-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="31edb-133">Por exemplo, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="31edb-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31edb-134"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="31edb-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="31edb-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="31edb-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="31edb-136">Opcional</span><span class="sxs-lookup"><span data-stu-id="31edb-136">Optional</span></span></td>
<td><span data-ttu-id="31edb-137">Indica a margem esquerda ou direita.</span><span class="sxs-lookup"><span data-stu-id="31edb-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="31edb-138">Esquerda</span><span class="sxs-lookup"><span data-stu-id="31edb-138">Left</span></span></li>
<li><span data-ttu-id="31edb-139">Direita</span><span class="sxs-lookup"><span data-stu-id="31edb-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31edb-140"><strong>Espaçamento</strong></span><span class="sxs-lookup"><span data-stu-id="31edb-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="31edb-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="31edb-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="31edb-142">Opcional</span><span class="sxs-lookup"><span data-stu-id="31edb-142">Optional</span></span></td>
<td><span data-ttu-id="31edb-143">Espaçamento entre a borda da página e a margem.</span><span class="sxs-lookup"><span data-stu-id="31edb-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="31edb-144">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="31edb-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="31edb-145">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="31edb-145">Element Information</span></span>



|  <span data-ttu-id="31edb-146">Elemento</span><span class="sxs-lookup"><span data-stu-id="31edb-146">Element</span></span>     | <span data-ttu-id="31edb-147">Valor</span><span class="sxs-lookup"><span data-stu-id="31edb-147">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="31edb-148">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="31edb-148">Element type</span></span> | <span data-ttu-id="31edb-149">ComplexType de [**margintype**](margintype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="31edb-149">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="31edb-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="31edb-150">Namespace</span></span>    | <span data-ttu-id="31edb-151">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="31edb-151">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="31edb-152">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="31edb-152">Schema name</span></span>  | <span data-ttu-id="31edb-153">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="31edb-153">Journal Reader</span></span>                                            |



 

 

 




