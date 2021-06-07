---
description: Contém um bitmap codificado em Base64 de um sinalizador associado à seção de uma nota do diário.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Elemento Flag
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46508f9821379fbedb3291ba45d16dbdd0fb316f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432310"
---
# <a name="flag-element"></a><span data-ttu-id="db32d-103">Elemento Flag</span><span class="sxs-lookup"><span data-stu-id="db32d-103">Flag Element</span></span>

<span data-ttu-id="db32d-104">Contém um bitmap codificado em Base64 de um sinalizador associado à seção de uma nota do diário.</span><span class="sxs-lookup"><span data-stu-id="db32d-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="db32d-105">Definição</span><span class="sxs-lookup"><span data-stu-id="db32d-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="db32d-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="db32d-106">Parent Elements</span></span>

[<span data-ttu-id="db32d-107">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="db32d-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="db32d-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="db32d-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="db32d-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="db32d-109">Child Elements</span></span>

<span data-ttu-id="db32d-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="db32d-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="db32d-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="db32d-111">Attributes</span></span>



| <span data-ttu-id="db32d-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="db32d-112">Attribute</span></span>  | <span data-ttu-id="db32d-113">Type</span><span class="sxs-lookup"><span data-stu-id="db32d-113">Type</span></span>                      | <span data-ttu-id="db32d-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="db32d-114">Required</span></span> | <span data-ttu-id="db32d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="db32d-115">Description</span></span>                                                                             | <span data-ttu-id="db32d-116">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="db32d-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="db32d-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="db32d-117">**Left**</span></span>   | <span data-ttu-id="db32d-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="db32d-118">**xs:integer**</span></span>            | <span data-ttu-id="db32d-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="db32d-119">Required</span></span> | <span data-ttu-id="db32d-120">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="db32d-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="db32d-121">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="db32d-121">Any integer.</span></span>              |
| <span data-ttu-id="db32d-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="db32d-122">**Top**</span></span>    | <span data-ttu-id="db32d-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="db32d-123">**xs:integer**</span></span>            | <span data-ttu-id="db32d-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="db32d-124">Required</span></span> | <span data-ttu-id="db32d-125">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="db32d-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="db32d-126">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="db32d-126">Any integer.</span></span>              |
| <span data-ttu-id="db32d-127">**Largura**</span><span class="sxs-lookup"><span data-stu-id="db32d-127">**Width**</span></span>  | <span data-ttu-id="db32d-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="db32d-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="db32d-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="db32d-129">Required</span></span> | <span data-ttu-id="db32d-130">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="db32d-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="db32d-131">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="db32d-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="db32d-132">**Altura**</span><span class="sxs-lookup"><span data-stu-id="db32d-132">**Height**</span></span> | <span data-ttu-id="db32d-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="db32d-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="db32d-134">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="db32d-134">Required</span></span> | <span data-ttu-id="db32d-135">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="db32d-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="db32d-136">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="db32d-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="db32d-137">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="db32d-137">Element Information</span></span>



|  <span data-ttu-id="db32d-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="db32d-138">Element</span></span>     | <span data-ttu-id="db32d-139">Valor</span><span class="sxs-lookup"><span data-stu-id="db32d-139">Value</span></span>                                                     |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="db32d-140">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="db32d-140">Element type</span></span> | <span data-ttu-id="db32d-141">ComplexType de [**flagType**](flagtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="db32d-141">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="db32d-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="db32d-142">Namespace</span></span>    | <span data-ttu-id="db32d-143">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="db32d-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="db32d-144">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="db32d-144">Schema name</span></span>  | <span data-ttu-id="db32d-145">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="db32d-145">Journal Reader</span></span>                                        |



 

 

 



