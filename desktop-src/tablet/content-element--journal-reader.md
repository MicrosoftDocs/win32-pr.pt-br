---
description: Contém o conteúdo de uma página de diário.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Elemento Content [leitor de diário]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b5a7c9631cd69d38b8db54e2a2f8e69636f7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813347"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="1029b-103">Leitor de diário de elementos de conteúdo \[\]</span><span class="sxs-lookup"><span data-stu-id="1029b-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="1029b-104">Contém o conteúdo de uma página de diário.</span><span class="sxs-lookup"><span data-stu-id="1029b-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="1029b-105">Definição</span><span class="sxs-lookup"><span data-stu-id="1029b-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="1029b-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1029b-106">Parent Elements</span></span>

[<span data-ttu-id="1029b-107">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="1029b-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="1029b-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1029b-108">Child Elements</span></span>

[<span data-ttu-id="1029b-109">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="1029b-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="1029b-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="1029b-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="1029b-111">**Senha**</span><span class="sxs-lookup"><span data-stu-id="1029b-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="1029b-112">**Texto**</span><span class="sxs-lookup"><span data-stu-id="1029b-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="1029b-113">**Imagem**</span><span class="sxs-lookup"><span data-stu-id="1029b-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="1029b-114">**Sinalizador**</span><span class="sxs-lookup"><span data-stu-id="1029b-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="1029b-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="1029b-115">Attributes</span></span>



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
<th><span data-ttu-id="1029b-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="1029b-116">Attribute</span></span></th>
<th><span data-ttu-id="1029b-117">Type</span><span class="sxs-lookup"><span data-stu-id="1029b-117">Type</span></span></th>
<th><span data-ttu-id="1029b-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1029b-118">Required</span></span></th>
<th><span data-ttu-id="1029b-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="1029b-119">Description</span></span></th>
<th><span data-ttu-id="1029b-120">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="1029b-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1029b-121"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="1029b-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="1029b-122"><a href="contenttype-complex-type.md"><strong>ComplexType ContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="1029b-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="1029b-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1029b-123">Required</span></span></td>
<td><span data-ttu-id="1029b-124">Se o tipo for &quot; Inert &quot; , o conteúdo não poderá ser modificado.</span><span class="sxs-lookup"><span data-stu-id="1029b-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="1029b-125">Normal</span><span class="sxs-lookup"><span data-stu-id="1029b-125">Normal</span></span></li>
<li><span data-ttu-id="1029b-126">Inert</span><span class="sxs-lookup"><span data-stu-id="1029b-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="1029b-127">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1029b-127">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="1029b-128">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1029b-128">Element type</span></span> | <span data-ttu-id="1029b-129">ComplexType [**ContentType**](contenttype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="1029b-129">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="1029b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1029b-130">Namespace</span></span>    | <span data-ttu-id="1029b-131">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="1029b-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="1029b-132">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="1029b-132">Schema name</span></span>  | <span data-ttu-id="1029b-133">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="1029b-133">Journal Reader</span></span>                                              |



 

 

 




