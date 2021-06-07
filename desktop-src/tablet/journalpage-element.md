---
description: Contém os detalhes sobre uma página individual em uma nota de Diário.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0939194585b067525fa841d6d41674180a40adb9
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432138"
---
# <a name="journalpage-element"></a><span data-ttu-id="94954-103">Elemento JournalPage</span><span class="sxs-lookup"><span data-stu-id="94954-103">JournalPage Element</span></span>

<span data-ttu-id="94954-104">Contém os detalhes sobre uma página individual em uma nota de Diário.</span><span class="sxs-lookup"><span data-stu-id="94954-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="94954-105">Definição</span><span class="sxs-lookup"><span data-stu-id="94954-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="94954-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="94954-106">Parent Elements</span></span>

[<span data-ttu-id="94954-107">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="94954-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="94954-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="94954-108">Child Elements</span></span>

[<span data-ttu-id="94954-109">**Estático**</span><span class="sxs-lookup"><span data-stu-id="94954-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="94954-110">**DocImage**</span><span class="sxs-lookup"><span data-stu-id="94954-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="94954-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="94954-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="94954-112">**Conteúdo**</span><span class="sxs-lookup"><span data-stu-id="94954-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="94954-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="94954-113">Attributes</span></span>



| <span data-ttu-id="94954-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="94954-114">Attribute</span></span>      | <span data-ttu-id="94954-115">Type</span><span class="sxs-lookup"><span data-stu-id="94954-115">Type</span></span>                      | <span data-ttu-id="94954-116">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="94954-116">Required</span></span> | <span data-ttu-id="94954-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="94954-117">Description</span></span>                                                                        | <span data-ttu-id="94954-118">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="94954-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="94954-119">**Número**</span><span class="sxs-lookup"><span data-stu-id="94954-119">**Number**</span></span>     | <span data-ttu-id="94954-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="94954-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="94954-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="94954-121">Required</span></span> | <span data-ttu-id="94954-122">O número ordinal da página dentro do documento Diário, começando com um (1).</span><span class="sxs-lookup"><span data-stu-id="94954-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="94954-123">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="94954-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="94954-124">**Largura**</span><span class="sxs-lookup"><span data-stu-id="94954-124">**Width**</span></span>      | <span data-ttu-id="94954-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="94954-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="94954-126">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="94954-126">Required</span></span> | <span data-ttu-id="94954-127">A largura da página.</span><span class="sxs-lookup"><span data-stu-id="94954-127">The width of the page.</span></span>                                                             | <span data-ttu-id="94954-128">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="94954-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="94954-129">**Altura**</span><span class="sxs-lookup"><span data-stu-id="94954-129">**Height**</span></span>     | <span data-ttu-id="94954-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="94954-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="94954-131">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="94954-131">Required</span></span> | <span data-ttu-id="94954-132">A altura da página.</span><span class="sxs-lookup"><span data-stu-id="94954-132">The height of the page.</span></span>                                                            | <span data-ttu-id="94954-133">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="94954-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="94954-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="94954-134">**LineHeight**</span></span> | <span data-ttu-id="94954-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="94954-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="94954-136">Opcional</span><span class="sxs-lookup"><span data-stu-id="94954-136">Optional</span></span> | <span data-ttu-id="94954-137">A altura da linha usada na página.</span><span class="sxs-lookup"><span data-stu-id="94954-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="94954-138">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="94954-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="94954-139">**Languageid**</span><span class="sxs-lookup"><span data-stu-id="94954-139">**LanguageId**</span></span> | <span data-ttu-id="94954-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="94954-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="94954-141">Opcional</span><span class="sxs-lookup"><span data-stu-id="94954-141">Optional</span></span> | <span data-ttu-id="94954-142">A ID de idioma usada para a página.</span><span class="sxs-lookup"><span data-stu-id="94954-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="94954-143">Um inteiro não negativo que representa uma ID de idioma válida.</span><span class="sxs-lookup"><span data-stu-id="94954-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="94954-144">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="94954-144">Element Information</span></span>



|  <span data-ttu-id="94954-145">Elemento</span><span class="sxs-lookup"><span data-stu-id="94954-145">Element</span></span>     | <span data-ttu-id="94954-146">Valor</span><span class="sxs-lookup"><span data-stu-id="94954-146">Value</span></span>                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="94954-147">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="94954-147">Element type</span></span> | <span data-ttu-id="94954-148">[**ComplexType JournalPageType**](journalpagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="94954-148">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="94954-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="94954-149">Namespace</span></span>    | <span data-ttu-id="94954-150">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="94954-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="94954-151">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="94954-151">Schema name</span></span>  | <span data-ttu-id="94954-152">Leitor de Diário</span><span class="sxs-lookup"><span data-stu-id="94954-152">Journal Reader</span></span>                                                      |



 

 

 



