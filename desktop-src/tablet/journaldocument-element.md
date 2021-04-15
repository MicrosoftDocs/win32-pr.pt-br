---
description: O elemento de nível superior em um arquivo XML de nota do diário.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408df14347c130e6b0a73ba869b634ca2493fb56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506233"
---
# <a name="journaldocument-element"></a><span data-ttu-id="643b6-103">Elemento JournalDocument</span><span class="sxs-lookup"><span data-stu-id="643b6-103">JournalDocument Element</span></span>

<span data-ttu-id="643b6-104">O elemento de nível superior em um arquivo XML de nota do diário.</span><span class="sxs-lookup"><span data-stu-id="643b6-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="643b6-105">Definição</span><span class="sxs-lookup"><span data-stu-id="643b6-105">Definition</span></span>

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a><span data-ttu-id="643b6-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="643b6-106">Parent Elements</span></span>

<span data-ttu-id="643b6-107">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="643b6-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="643b6-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="643b6-108">Child Elements</span></span>

[<span data-ttu-id="643b6-109">**Telas**</span><span class="sxs-lookup"><span data-stu-id="643b6-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="643b6-110">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="643b6-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="643b6-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="643b6-111">Attributes</span></span>



| <span data-ttu-id="643b6-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="643b6-112">Attribute</span></span>             | <span data-ttu-id="643b6-113">Type</span><span class="sxs-lookup"><span data-stu-id="643b6-113">Type</span></span>                      | <span data-ttu-id="643b6-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="643b6-114">Required</span></span> | <span data-ttu-id="643b6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="643b6-115">Description</span></span>                                                      | <span data-ttu-id="643b6-116">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="643b6-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="643b6-117">**Versão**</span><span class="sxs-lookup"><span data-stu-id="643b6-117">**Version**</span></span>           | <span data-ttu-id="643b6-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="643b6-118">**xs:string**</span></span>             | <span data-ttu-id="643b6-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="643b6-119">Required</span></span> | <span data-ttu-id="643b6-120">A versão do documento de diário representada no arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="643b6-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="643b6-121">1.0</span><span class="sxs-lookup"><span data-stu-id="643b6-121">1.0</span></span>                       |
| <span data-ttu-id="643b6-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="643b6-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="643b6-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="643b6-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="643b6-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="643b6-124">Required</span></span> | <span data-ttu-id="643b6-125">A largura padrão da página para o documento do diário.</span><span class="sxs-lookup"><span data-stu-id="643b6-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="643b6-126">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="643b6-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="643b6-127">**DefaultPageHeight**</span><span class="sxs-lookup"><span data-stu-id="643b6-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="643b6-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="643b6-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="643b6-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="643b6-129">Required</span></span> | <span data-ttu-id="643b6-130">A altura padrão da página para o documento do diário.</span><span class="sxs-lookup"><span data-stu-id="643b6-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="643b6-131">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="643b6-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="643b6-132">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="643b6-132">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="643b6-133">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="643b6-133">Element type</span></span> | <span data-ttu-id="643b6-134">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="643b6-134">**JournalDocument**</span></span>                        |
| <span data-ttu-id="643b6-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="643b6-135">Namespace</span></span>    | <span data-ttu-id="643b6-136">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="643b6-136">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="643b6-137">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="643b6-137">Schema name</span></span>  | <span data-ttu-id="643b6-138">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="643b6-138">Journal Reader</span></span>                             |



 

 

 



