---
description: Contém o conteúdo de uma página De diário.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Elemento Content [Leitor de Diário]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432148"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="63658-103">Leitor de Diário \[ do Elemento de Conteúdo\]</span><span class="sxs-lookup"><span data-stu-id="63658-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="63658-104">Contém o conteúdo de uma página De diário.</span><span class="sxs-lookup"><span data-stu-id="63658-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="63658-105">Definição</span><span class="sxs-lookup"><span data-stu-id="63658-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="63658-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="63658-106">Parent Elements</span></span>

[<span data-ttu-id="63658-107">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="63658-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="63658-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="63658-108">Child Elements</span></span>

[<span data-ttu-id="63658-109">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="63658-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="63658-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="63658-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="63658-111">**Desenho**</span><span class="sxs-lookup"><span data-stu-id="63658-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="63658-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="63658-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="63658-113">**Imagem**</span><span class="sxs-lookup"><span data-stu-id="63658-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="63658-114">**Bandeira**</span><span class="sxs-lookup"><span data-stu-id="63658-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="63658-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="63658-115">Attributes</span></span>



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
<th><span data-ttu-id="63658-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="63658-116">Attribute</span></span></th>
<th><span data-ttu-id="63658-117">Type</span><span class="sxs-lookup"><span data-stu-id="63658-117">Type</span></span></th>
<th><span data-ttu-id="63658-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="63658-118">Required</span></span></th>
<th><span data-ttu-id="63658-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="63658-119">Description</span></span></th>
<th><span data-ttu-id="63658-120">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="63658-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63658-121"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="63658-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="63658-122"><a href="contenttype-complex-type.md"><strong>ComplexType ContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="63658-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="63658-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="63658-123">Required</span></span></td>
<td><span data-ttu-id="63658-124">Se o tipo for &quot; Inert &quot; , o conteúdo não poderá ser modificado.</span><span class="sxs-lookup"><span data-stu-id="63658-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="63658-125">Normal</span><span class="sxs-lookup"><span data-stu-id="63658-125">Normal</span></span></li>
<li><span data-ttu-id="63658-126">Inerte</span><span class="sxs-lookup"><span data-stu-id="63658-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="63658-127">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="63658-127">Element Information</span></span>



|  <span data-ttu-id="63658-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="63658-128">Element</span></span>     | <span data-ttu-id="63658-129">Valor</span><span class="sxs-lookup"><span data-stu-id="63658-129">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="63658-130">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="63658-130">Element type</span></span> | <span data-ttu-id="63658-131">[**ComplexType ContentType**](contenttype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="63658-131">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="63658-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="63658-132">Namespace</span></span>    | <span data-ttu-id="63658-133">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="63658-133">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="63658-134">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="63658-134">Schema name</span></span>  | <span data-ttu-id="63658-135">Leitor de Diário</span><span class="sxs-lookup"><span data-stu-id="63658-135">Journal Reader</span></span>                                              |



 

 

 




