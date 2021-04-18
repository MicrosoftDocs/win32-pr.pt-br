---
description: Contém um bitmap codificado em Base64 de um sinalizador associado à seção de uma nota do diário.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Elemento Flag
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6eda9aeb29c07c0de05eadffb8ba8d60f81954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760565"
---
# <a name="flag-element"></a><span data-ttu-id="ee6c9-103">Elemento Flag</span><span class="sxs-lookup"><span data-stu-id="ee6c9-103">Flag Element</span></span>

<span data-ttu-id="ee6c9-104">Contém um bitmap codificado em Base64 de um sinalizador associado à seção de uma nota do diário.</span><span class="sxs-lookup"><span data-stu-id="ee6c9-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="ee6c9-105">Definição</span><span class="sxs-lookup"><span data-stu-id="ee6c9-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="ee6c9-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ee6c9-106">Parent Elements</span></span>

[<span data-ttu-id="ee6c9-107">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="ee6c9-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="ee6c9-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="ee6c9-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="ee6c9-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ee6c9-109">Child Elements</span></span>

<span data-ttu-id="ee6c9-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ee6c9-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="ee6c9-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="ee6c9-111">Attributes</span></span>



| <span data-ttu-id="ee6c9-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="ee6c9-112">Attribute</span></span>  | <span data-ttu-id="ee6c9-113">Type</span><span class="sxs-lookup"><span data-stu-id="ee6c9-113">Type</span></span>                      | <span data-ttu-id="ee6c9-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ee6c9-114">Required</span></span> | <span data-ttu-id="ee6c9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee6c9-115">Description</span></span>                                                                             | <span data-ttu-id="ee6c9-116">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="ee6c9-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="ee6c9-117">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="ee6c9-117">**Left**</span></span>   | <span data-ttu-id="ee6c9-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="ee6c9-118">**xs:integer**</span></span>            | <span data-ttu-id="ee6c9-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ee6c9-119">Required</span></span> | <span data-ttu-id="ee6c9-120">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="ee6c9-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="ee6c9-121">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="ee6c9-121">Any integer.</span></span>              |
| <span data-ttu-id="ee6c9-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="ee6c9-122">**Top**</span></span>    | <span data-ttu-id="ee6c9-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="ee6c9-123">**xs:integer**</span></span>            | <span data-ttu-id="ee6c9-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ee6c9-124">Required</span></span> | <span data-ttu-id="ee6c9-125">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="ee6c9-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="ee6c9-126">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="ee6c9-126">Any integer.</span></span>              |
| <span data-ttu-id="ee6c9-127">**Largura**</span><span class="sxs-lookup"><span data-stu-id="ee6c9-127">**Width**</span></span>  | <span data-ttu-id="ee6c9-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ee6c9-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ee6c9-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ee6c9-129">Required</span></span> | <span data-ttu-id="ee6c9-130">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="ee6c9-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="ee6c9-131">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="ee6c9-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="ee6c9-132">**Altura**</span><span class="sxs-lookup"><span data-stu-id="ee6c9-132">**Height**</span></span> | <span data-ttu-id="ee6c9-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ee6c9-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ee6c9-134">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ee6c9-134">Required</span></span> | <span data-ttu-id="ee6c9-135">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="ee6c9-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="ee6c9-136">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="ee6c9-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="ee6c9-137">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ee6c9-137">Element Information</span></span>



|              |                                                       |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="ee6c9-138">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ee6c9-138">Element type</span></span> | <span data-ttu-id="ee6c9-139">ComplexType de [**flagType**](flagtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="ee6c9-139">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="ee6c9-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee6c9-140">Namespace</span></span>    | <span data-ttu-id="ee6c9-141">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="ee6c9-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="ee6c9-142">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="ee6c9-142">Schema name</span></span>  | <span data-ttu-id="ee6c9-143">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="ee6c9-143">Journal Reader</span></span>                                        |



 

 

 



