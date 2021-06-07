---
description: Contém informações de título sobre a nota Do diário.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef687f809aae5c3722cdad84ee63d79c7bfcfb21
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432218"
---
# <a name="title-element"></a><span data-ttu-id="5bfa4-103">Elemento Title</span><span class="sxs-lookup"><span data-stu-id="5bfa4-103">Title Element</span></span>

<span data-ttu-id="5bfa4-104">Contém informações de título sobre a nota Do diário.</span><span class="sxs-lookup"><span data-stu-id="5bfa4-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="5bfa4-105">Definição</span><span class="sxs-lookup"><span data-stu-id="5bfa4-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="5bfa4-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5bfa4-106">Parent Elements</span></span>

[<span data-ttu-id="5bfa4-107">**Papelaria**</span><span class="sxs-lookup"><span data-stu-id="5bfa4-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="5bfa4-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5bfa4-108">Child Elements</span></span>

[<span data-ttu-id="5bfa4-109">**TitleArea**</span><span class="sxs-lookup"><span data-stu-id="5bfa4-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="5bfa4-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="5bfa4-110">Attributes</span></span>



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
<th><span data-ttu-id="5bfa4-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="5bfa4-111">Attribute</span></span></th>
<th><span data-ttu-id="5bfa4-112">Type</span><span class="sxs-lookup"><span data-stu-id="5bfa4-112">Type</span></span></th>
<th><span data-ttu-id="5bfa4-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5bfa4-113">Required</span></span></th>
<th><span data-ttu-id="5bfa4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bfa4-114">Description</span></span></th>
<th><span data-ttu-id="5bfa4-115">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5bfa4-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5bfa4-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="5bfa4-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="5bfa4-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="5bfa4-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="5bfa4-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5bfa4-118">Required</span></span></td>
<td><span data-ttu-id="5bfa4-119">Especifica o tipo de borda em torno do título da nota.</span><span class="sxs-lookup"><span data-stu-id="5bfa4-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="5bfa4-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5bfa4-120">None</span></span></li>
<li><span data-ttu-id="5bfa4-121">SolidSquare</span><span class="sxs-lookup"><span data-stu-id="5bfa4-121">SolidSquare</span></span></li>
<li><span data-ttu-id="5bfa4-122">OutlineSquare</span><span class="sxs-lookup"><span data-stu-id="5bfa4-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="5bfa4-123">SolidRoundRect</span><span class="sxs-lookup"><span data-stu-id="5bfa4-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="5bfa4-124">OutlineRoundRect</span><span class="sxs-lookup"><span data-stu-id="5bfa4-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="5bfa4-125">SolidRoundRectDottedBaseline</span><span class="sxs-lookup"><span data-stu-id="5bfa4-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5bfa4-126"><strong>DateStyle</strong></span><span class="sxs-lookup"><span data-stu-id="5bfa4-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="5bfa4-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="5bfa4-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="5bfa4-128">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5bfa4-128">Required</span></span></td>
<td><span data-ttu-id="5bfa4-129">Define se o título inclui uma data ou não.</span><span class="sxs-lookup"><span data-stu-id="5bfa4-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="5bfa4-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5bfa4-130">None</span></span></li>
<li><span data-ttu-id="5bfa4-131">Short</span><span class="sxs-lookup"><span data-stu-id="5bfa4-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5bfa4-132"><strong>Cor</strong></span><span class="sxs-lookup"><span data-stu-id="5bfa4-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="5bfa4-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="5bfa4-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="5bfa4-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="5bfa4-134">Optional</span></span></td>
<td><span data-ttu-id="5bfa4-135">Especifica a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="5bfa4-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="5bfa4-136">Consulte <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5bfa4-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="5bfa4-137">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5bfa4-137">Element Information</span></span>



| <span data-ttu-id="5bfa4-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="5bfa4-138">Element</span></span>      | <span data-ttu-id="5bfa4-139">Valor</span><span class="sxs-lookup"><span data-stu-id="5bfa4-139">Value</span></span>                                                   |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="5bfa4-140">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5bfa4-140">Element type</span></span> | <span data-ttu-id="5bfa4-141">[**ComplexType TitleType**](titletype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="5bfa4-141">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="5bfa4-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="5bfa4-142">Namespace</span></span>    | <span data-ttu-id="5bfa4-143">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="5bfa4-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="5bfa4-144">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="5bfa4-144">Schema name</span></span>  | <span data-ttu-id="5bfa4-145">Leitor de Diário</span><span class="sxs-lookup"><span data-stu-id="5bfa4-145">Journal Reader</span></span>                                          |



 

 

 



