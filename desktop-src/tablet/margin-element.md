---
description: Define as linhas de margem desenhadas na página.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Elemento Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171849"
---
# <a name="margin-element"></a><span data-ttu-id="b7bc7-103">Elemento Margin</span><span class="sxs-lookup"><span data-stu-id="b7bc7-103">Margin Element</span></span>

<span data-ttu-id="b7bc7-104">Define as linhas de margem desenhadas na página.</span><span class="sxs-lookup"><span data-stu-id="b7bc7-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="b7bc7-105">Definição</span><span class="sxs-lookup"><span data-stu-id="b7bc7-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="b7bc7-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b7bc7-106">Parent Elements</span></span>

<span data-ttu-id="b7bc7-107">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b7bc7-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b7bc7-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b7bc7-108">Child Elements</span></span>

<span data-ttu-id="b7bc7-109">Nenhum..</span><span class="sxs-lookup"><span data-stu-id="b7bc7-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="b7bc7-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="b7bc7-110">Attributes</span></span>



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
<th><span data-ttu-id="b7bc7-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="b7bc7-111">Attribute</span></span></th>
<th><span data-ttu-id="b7bc7-112">Type</span><span class="sxs-lookup"><span data-stu-id="b7bc7-112">Type</span></span></th>
<th><span data-ttu-id="b7bc7-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b7bc7-113">Required</span></span></th>
<th><span data-ttu-id="b7bc7-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7bc7-114">Description</span></span></th>
<th><span data-ttu-id="b7bc7-115">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="b7bc7-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7bc7-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc7-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="b7bc7-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="b7bc7-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="b7bc7-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b7bc7-118">Required</span></span></td>
<td><span data-ttu-id="b7bc7-119">Especifica o tipo de linha a ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="b7bc7-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7bc7-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b7bc7-120">None</span></span></li>
<li><span data-ttu-id="b7bc7-121">Sólido</span><span class="sxs-lookup"><span data-stu-id="b7bc7-121">Solid</span></span></li>
<li><span data-ttu-id="b7bc7-122">Traço</span><span class="sxs-lookup"><span data-stu-id="b7bc7-122">Dash</span></span></li>
<li><span data-ttu-id="b7bc7-123">Ponto</span><span class="sxs-lookup"><span data-stu-id="b7bc7-123">Dot</span></span></li>
<li><span data-ttu-id="b7bc7-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="b7bc7-124">DashDot</span></span></li>
<li><span data-ttu-id="b7bc7-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="b7bc7-125">DashDotDot</span></span></li>
<li><span data-ttu-id="b7bc7-126">Double</span><span class="sxs-lookup"><span data-stu-id="b7bc7-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc7-127"><strong>Cor</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc7-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="b7bc7-128">SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7bc7-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="b7bc7-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="b7bc7-129">Optional</span></span></td>
<td><span data-ttu-id="b7bc7-130">Cor do elemento.</span><span class="sxs-lookup"><span data-stu-id="b7bc7-130">Color of the element.</span></span></td>
<td><span data-ttu-id="b7bc7-131">Um valor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="b7bc7-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="b7bc7-132">Corresponde à seguinte expressão regular: # [0-9A-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="b7bc7-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="b7bc7-133">Por exemplo, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="b7bc7-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc7-134"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc7-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="b7bc7-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="b7bc7-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="b7bc7-136">Opcional</span><span class="sxs-lookup"><span data-stu-id="b7bc7-136">Optional</span></span></td>
<td><span data-ttu-id="b7bc7-137">Indica a margem esquerda ou direita.</span><span class="sxs-lookup"><span data-stu-id="b7bc7-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7bc7-138">Esquerda</span><span class="sxs-lookup"><span data-stu-id="b7bc7-138">Left</span></span></li>
<li><span data-ttu-id="b7bc7-139">Direita</span><span class="sxs-lookup"><span data-stu-id="b7bc7-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc7-140"><strong>Espaçamento</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc7-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="b7bc7-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc7-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="b7bc7-142">Opcional</span><span class="sxs-lookup"><span data-stu-id="b7bc7-142">Optional</span></span></td>
<td><span data-ttu-id="b7bc7-143">Espaçamento entre a borda da página e a margem.</span><span class="sxs-lookup"><span data-stu-id="b7bc7-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="b7bc7-144">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="b7bc7-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="b7bc7-145">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b7bc7-145">Element Information</span></span>



|              |                                                           |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="b7bc7-146">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b7bc7-146">Element type</span></span> | <span data-ttu-id="b7bc7-147">ComplexType de [**margintype**](margintype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="b7bc7-147">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="b7bc7-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7bc7-148">Namespace</span></span>    | <span data-ttu-id="b7bc7-149">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="b7bc7-149">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="b7bc7-150">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="b7bc7-150">Schema name</span></span>  | <span data-ttu-id="b7bc7-151">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="b7bc7-151">Journal Reader</span></span>                                            |



 

 

 




