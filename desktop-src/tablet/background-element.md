---
description: Contém o plano de fundo de um elemento JournalDocument ou de um elemento JournalPage.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Elemento background
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58a836c7cfd13130779c1cd6b017105bcaa6321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787626"
---
# <a name="background-element"></a><span data-ttu-id="b6b1d-103">Elemento background</span><span class="sxs-lookup"><span data-stu-id="b6b1d-103">Background Element</span></span>

<span data-ttu-id="b6b1d-104">Contém o plano de fundo de um elemento [**JournalDocument**](journaldocument-element.md) ou de um elemento [**JournalPage**](journalpage-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b6b1d-104">Contains the background for a [**JournalDocument**](journaldocument-element.md) element or [**JournalPage**](journalpage-element.md) element.</span></span>

## <a name="definition"></a><span data-ttu-id="b6b1d-105">Definição</span><span class="sxs-lookup"><span data-stu-id="b6b1d-105">Definition</span></span>

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="b6b1d-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b6b1d-106">Parent Elements</span></span>

[<span data-ttu-id="b6b1d-107">**Telas**</span><span class="sxs-lookup"><span data-stu-id="b6b1d-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="b6b1d-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b6b1d-108">Child Elements</span></span>

[<span data-ttu-id="b6b1d-109">**Imagem**</span><span class="sxs-lookup"><span data-stu-id="b6b1d-109">**Image**</span></span>](image-element.md)

## <a name="attributes"></a><span data-ttu-id="b6b1d-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6b1d-110">Attributes</span></span>



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
<th><span data-ttu-id="b6b1d-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6b1d-111">Attribute</span></span></th>
<th><span data-ttu-id="b6b1d-112">Type</span><span class="sxs-lookup"><span data-stu-id="b6b1d-112">Type</span></span></th>
<th><span data-ttu-id="b6b1d-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b6b1d-113">Required</span></span></th>
<th><span data-ttu-id="b6b1d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6b1d-114">Description</span></span></th>
<th><span data-ttu-id="b6b1d-115">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="b6b1d-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6b1d-116"><strong>Estilo</strong></span><span class="sxs-lookup"><span data-stu-id="b6b1d-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="b6b1d-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="b6b1d-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="b6b1d-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b6b1d-118">Required</span></span></td>
<td><span data-ttu-id="b6b1d-119">Especifica o estilo do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="b6b1d-119">Specifies the style of the background.</span></span></td>
<td><ul>
<li><span data-ttu-id="b6b1d-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b6b1d-120">None</span></span></li>
<li><span data-ttu-id="b6b1d-121">Sólido</span><span class="sxs-lookup"><span data-stu-id="b6b1d-121">Solid</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6b1d-122"><strong>Cor</strong></span><span class="sxs-lookup"><span data-stu-id="b6b1d-122"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="b6b1d-123">SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6b1d-123"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="b6b1d-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="b6b1d-124">Optional</span></span></td>
<td><span data-ttu-id="b6b1d-125">Especifica a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="b6b1d-125">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="b6b1d-126">Confira simpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b6b1d-126">See <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="b6b1d-127">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b6b1d-127">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="b6b1d-128">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b6b1d-128">Element type</span></span> | <span data-ttu-id="b6b1d-129">ComplexType [**em segundo plano**](backgroundtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="b6b1d-129">[**BackgroundType**](backgroundtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="b6b1d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6b1d-130">Namespace</span></span>    | <span data-ttu-id="b6b1d-131">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="b6b1d-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="b6b1d-132">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="b6b1d-132">Schema name</span></span>  | <span data-ttu-id="b6b1d-133">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="b6b1d-133">Journal Reader</span></span>                                                    |



 

 

 



