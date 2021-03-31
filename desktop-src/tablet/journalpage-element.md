---
description: Contém os detalhes sobre uma página individual em uma nota do diário.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829217"
---
# <a name="journalpage-element"></a><span data-ttu-id="ebda2-103">Elemento JournalPage</span><span class="sxs-lookup"><span data-stu-id="ebda2-103">JournalPage Element</span></span>

<span data-ttu-id="ebda2-104">Contém os detalhes sobre uma página individual em uma nota do diário.</span><span class="sxs-lookup"><span data-stu-id="ebda2-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="ebda2-105">Definição</span><span class="sxs-lookup"><span data-stu-id="ebda2-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="ebda2-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ebda2-106">Parent Elements</span></span>

[<span data-ttu-id="ebda2-107">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="ebda2-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="ebda2-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ebda2-108">Child Elements</span></span>

[<span data-ttu-id="ebda2-109">**Estático**</span><span class="sxs-lookup"><span data-stu-id="ebda2-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="ebda2-110">**DocImage**</span><span class="sxs-lookup"><span data-stu-id="ebda2-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="ebda2-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="ebda2-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="ebda2-112">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="ebda2-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="ebda2-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="ebda2-113">Attributes</span></span>



| <span data-ttu-id="ebda2-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="ebda2-114">Attribute</span></span>      | <span data-ttu-id="ebda2-115">Type</span><span class="sxs-lookup"><span data-stu-id="ebda2-115">Type</span></span>                      | <span data-ttu-id="ebda2-116">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ebda2-116">Required</span></span> | <span data-ttu-id="ebda2-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ebda2-117">Description</span></span>                                                                        | <span data-ttu-id="ebda2-118">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="ebda2-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="ebda2-119">**Número**</span><span class="sxs-lookup"><span data-stu-id="ebda2-119">**Number**</span></span>     | <span data-ttu-id="ebda2-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ebda2-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ebda2-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ebda2-121">Required</span></span> | <span data-ttu-id="ebda2-122">O número ordinal da página dentro do documento do diário, começando com um (1).</span><span class="sxs-lookup"><span data-stu-id="ebda2-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="ebda2-123">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="ebda2-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="ebda2-124">**Largura**</span><span class="sxs-lookup"><span data-stu-id="ebda2-124">**Width**</span></span>      | <span data-ttu-id="ebda2-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ebda2-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ebda2-126">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ebda2-126">Required</span></span> | <span data-ttu-id="ebda2-127">A largura da página.</span><span class="sxs-lookup"><span data-stu-id="ebda2-127">The width of the page.</span></span>                                                             | <span data-ttu-id="ebda2-128">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="ebda2-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="ebda2-129">**Altura**</span><span class="sxs-lookup"><span data-stu-id="ebda2-129">**Height**</span></span>     | <span data-ttu-id="ebda2-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ebda2-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ebda2-131">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ebda2-131">Required</span></span> | <span data-ttu-id="ebda2-132">A altura da página.</span><span class="sxs-lookup"><span data-stu-id="ebda2-132">The height of the page.</span></span>                                                            | <span data-ttu-id="ebda2-133">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="ebda2-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="ebda2-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="ebda2-134">**LineHeight**</span></span> | <span data-ttu-id="ebda2-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ebda2-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ebda2-136">Opcional</span><span class="sxs-lookup"><span data-stu-id="ebda2-136">Optional</span></span> | <span data-ttu-id="ebda2-137">A altura da linha usada na página.</span><span class="sxs-lookup"><span data-stu-id="ebda2-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="ebda2-138">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="ebda2-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="ebda2-139">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="ebda2-139">**LanguageId**</span></span> | <span data-ttu-id="ebda2-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ebda2-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ebda2-141">Opcional</span><span class="sxs-lookup"><span data-stu-id="ebda2-141">Optional</span></span> | <span data-ttu-id="ebda2-142">A ID de idioma usada para a página.</span><span class="sxs-lookup"><span data-stu-id="ebda2-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="ebda2-143">Um inteiro não negativo que representa uma ID de idioma válida.</span><span class="sxs-lookup"><span data-stu-id="ebda2-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="ebda2-144">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ebda2-144">Element Information</span></span>



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="ebda2-145">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ebda2-145">Element type</span></span> | <span data-ttu-id="ebda2-146">ComplexType [**JournalPageType**](journalpagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="ebda2-146">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="ebda2-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebda2-147">Namespace</span></span>    | <span data-ttu-id="ebda2-148">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="ebda2-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="ebda2-149">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="ebda2-149">Schema name</span></span>  | <span data-ttu-id="ebda2-150">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="ebda2-150">Journal Reader</span></span>                                                      |



 

 

 



