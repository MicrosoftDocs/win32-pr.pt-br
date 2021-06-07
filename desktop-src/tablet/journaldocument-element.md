---
description: O elemento de nível superior em um arquivo XML de nota do diário.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432168"
---
# <a name="journaldocument-element"></a><span data-ttu-id="1997e-103">Elemento JournalDocument</span><span class="sxs-lookup"><span data-stu-id="1997e-103">JournalDocument Element</span></span>

<span data-ttu-id="1997e-104">O elemento de nível superior em um arquivo XML de nota do diário.</span><span class="sxs-lookup"><span data-stu-id="1997e-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="1997e-105">Definição</span><span class="sxs-lookup"><span data-stu-id="1997e-105">Definition</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="1997e-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1997e-106">Parent Elements</span></span>

<span data-ttu-id="1997e-107">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1997e-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1997e-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1997e-108">Child Elements</span></span>

[<span data-ttu-id="1997e-109">**Telas**</span><span class="sxs-lookup"><span data-stu-id="1997e-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="1997e-110">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="1997e-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="1997e-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="1997e-111">Attributes</span></span>



| <span data-ttu-id="1997e-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="1997e-112">Attribute</span></span>             | <span data-ttu-id="1997e-113">Type</span><span class="sxs-lookup"><span data-stu-id="1997e-113">Type</span></span>                      | <span data-ttu-id="1997e-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1997e-114">Required</span></span> | <span data-ttu-id="1997e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1997e-115">Description</span></span>                                                      | <span data-ttu-id="1997e-116">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="1997e-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="1997e-117">**Versão**</span><span class="sxs-lookup"><span data-stu-id="1997e-117">**Version**</span></span>           | <span data-ttu-id="1997e-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="1997e-118">**xs:string**</span></span>             | <span data-ttu-id="1997e-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1997e-119">Required</span></span> | <span data-ttu-id="1997e-120">A versão do documento de diário representada no arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="1997e-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="1997e-121">1.0</span><span class="sxs-lookup"><span data-stu-id="1997e-121">1.0</span></span>                       |
| <span data-ttu-id="1997e-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="1997e-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="1997e-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="1997e-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="1997e-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1997e-124">Required</span></span> | <span data-ttu-id="1997e-125">A largura padrão da página para o documento do diário.</span><span class="sxs-lookup"><span data-stu-id="1997e-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="1997e-126">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="1997e-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="1997e-127">**DefaultPageHeight**</span><span class="sxs-lookup"><span data-stu-id="1997e-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="1997e-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="1997e-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="1997e-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1997e-129">Required</span></span> | <span data-ttu-id="1997e-130">A altura padrão da página para o documento do diário.</span><span class="sxs-lookup"><span data-stu-id="1997e-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="1997e-131">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="1997e-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="1997e-132">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1997e-132">Element Information</span></span>



|  <span data-ttu-id="1997e-133">Elemento</span><span class="sxs-lookup"><span data-stu-id="1997e-133">Element</span></span>     | <span data-ttu-id="1997e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="1997e-134">Value</span></span>                                                     |
|--------------|--------------------------------------------|
| <span data-ttu-id="1997e-135">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1997e-135">Element type</span></span> | <span data-ttu-id="1997e-136">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="1997e-136">**JournalDocument**</span></span>                        |
| <span data-ttu-id="1997e-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="1997e-137">Namespace</span></span>    | <span data-ttu-id="1997e-138">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="1997e-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="1997e-139">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="1997e-139">Schema name</span></span>  | <span data-ttu-id="1997e-140">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="1997e-140">Journal Reader</span></span>                             |



 

 

 



