---
description: Contém informações de título sobre a nota do diário.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781133"
---
# <a name="title-element"></a><span data-ttu-id="a97c5-103">Elemento Title</span><span class="sxs-lookup"><span data-stu-id="a97c5-103">Title Element</span></span>

<span data-ttu-id="a97c5-104">Contém informações de título sobre a nota do diário.</span><span class="sxs-lookup"><span data-stu-id="a97c5-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="a97c5-105">Definição</span><span class="sxs-lookup"><span data-stu-id="a97c5-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="a97c5-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a97c5-106">Parent Elements</span></span>

[<span data-ttu-id="a97c5-107">**Telas**</span><span class="sxs-lookup"><span data-stu-id="a97c5-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="a97c5-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a97c5-108">Child Elements</span></span>

[<span data-ttu-id="a97c5-109">**TitleArea**</span><span class="sxs-lookup"><span data-stu-id="a97c5-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="a97c5-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="a97c5-110">Attributes</span></span>



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
<th><span data-ttu-id="a97c5-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="a97c5-111">Attribute</span></span></th>
<th><span data-ttu-id="a97c5-112">Type</span><span class="sxs-lookup"><span data-stu-id="a97c5-112">Type</span></span></th>
<th><span data-ttu-id="a97c5-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a97c5-113">Required</span></span></th>
<th><span data-ttu-id="a97c5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a97c5-114">Description</span></span></th>
<th><span data-ttu-id="a97c5-115">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="a97c5-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a97c5-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="a97c5-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="a97c5-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="a97c5-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="a97c5-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a97c5-118">Required</span></span></td>
<td><span data-ttu-id="a97c5-119">Especifica o tipo de borda ao redor do título da nota.</span><span class="sxs-lookup"><span data-stu-id="a97c5-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="a97c5-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a97c5-120">None</span></span></li>
<li><span data-ttu-id="a97c5-121">SolidSquare</span><span class="sxs-lookup"><span data-stu-id="a97c5-121">SolidSquare</span></span></li>
<li><span data-ttu-id="a97c5-122">OutlineSquare</span><span class="sxs-lookup"><span data-stu-id="a97c5-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="a97c5-123">SolidRoundRect</span><span class="sxs-lookup"><span data-stu-id="a97c5-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="a97c5-124">OutlineRoundRect</span><span class="sxs-lookup"><span data-stu-id="a97c5-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="a97c5-125">SolidRoundRectDottedBaseline</span><span class="sxs-lookup"><span data-stu-id="a97c5-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a97c5-126"><strong>Datastyle</strong></span><span class="sxs-lookup"><span data-stu-id="a97c5-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="a97c5-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="a97c5-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="a97c5-128">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a97c5-128">Required</span></span></td>
<td><span data-ttu-id="a97c5-129">Define se o título inclui uma data ou não.</span><span class="sxs-lookup"><span data-stu-id="a97c5-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="a97c5-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a97c5-130">None</span></span></li>
<li><span data-ttu-id="a97c5-131">Short</span><span class="sxs-lookup"><span data-stu-id="a97c5-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a97c5-132"><strong>Cor</strong></span><span class="sxs-lookup"><span data-stu-id="a97c5-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="a97c5-133"><a href="colortype-simple-type.md"><strong>SimpleType de ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="a97c5-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="a97c5-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="a97c5-134">Optional</span></span></td>
<td><span data-ttu-id="a97c5-135">Especifica a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="a97c5-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="a97c5-136">Confira <a href="colortype-simple-type.md"><strong>simpleType de ColorType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a97c5-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="a97c5-137">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a97c5-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="a97c5-138">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a97c5-138">Element type</span></span> | <span data-ttu-id="a97c5-139">ComplexType de [**títulotype**](titletype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="a97c5-139">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="a97c5-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="a97c5-140">Namespace</span></span>    | <span data-ttu-id="a97c5-141">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="a97c5-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="a97c5-142">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="a97c5-142">Schema name</span></span>  | <span data-ttu-id="a97c5-143">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="a97c5-143">Journal Reader</span></span>                                          |



 

 

 



