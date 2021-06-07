---
description: Contém informações de localização e limite para o título da nota, se presente.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Elemento TitleArea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d563e8d7f6fc0107bc3302d3f8d94d29dfbfb8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432188"
---
# <a name="titlearea-element"></a><span data-ttu-id="5ef4d-103">Elemento TitleArea</span><span class="sxs-lookup"><span data-stu-id="5ef4d-103">TitleArea Element</span></span>

<span data-ttu-id="5ef4d-104">Contém informações de localização e limite para o título da nota, se presente.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="5ef4d-105">Definição</span><span class="sxs-lookup"><span data-stu-id="5ef4d-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="5ef4d-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5ef4d-106">Parent Elements</span></span>

[<span data-ttu-id="5ef4d-107">**Título**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="5ef4d-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5ef4d-108">Child Elements</span></span>

<span data-ttu-id="5ef4d-109">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="5ef4d-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="5ef4d-110">Attributes</span></span>



| <span data-ttu-id="5ef4d-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="5ef4d-111">Attribute</span></span>  | <span data-ttu-id="5ef4d-112">Type</span><span class="sxs-lookup"><span data-stu-id="5ef4d-112">Type</span></span>                      | <span data-ttu-id="5ef4d-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5ef4d-113">Required</span></span> | <span data-ttu-id="5ef4d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ef4d-114">Description</span></span>                                                                             | <span data-ttu-id="5ef4d-115">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5ef4d-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="5ef4d-116">**Left**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-116">**Left**</span></span>   | <span data-ttu-id="5ef4d-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-117">**xs:integer**</span></span>            | <span data-ttu-id="5ef4d-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5ef4d-118">Required</span></span> | <span data-ttu-id="5ef4d-119">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="5ef4d-120">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-120">Any integer.</span></span>              |
| <span data-ttu-id="5ef4d-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-121">**Top**</span></span>    | <span data-ttu-id="5ef4d-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-122">**xs:integer**</span></span>            | <span data-ttu-id="5ef4d-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5ef4d-123">Required</span></span> | <span data-ttu-id="5ef4d-124">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="5ef4d-125">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-125">Any integer.</span></span>              |
| <span data-ttu-id="5ef4d-126">**Largura**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-126">**Width**</span></span>  | <span data-ttu-id="5ef4d-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5ef4d-128">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5ef4d-128">Required</span></span> | <span data-ttu-id="5ef4d-129">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="5ef4d-130">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="5ef4d-131">**Altura**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-131">**Height**</span></span> | <span data-ttu-id="5ef4d-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5ef4d-133">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5ef4d-133">Required</span></span> | <span data-ttu-id="5ef4d-134">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="5ef4d-135">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="5ef4d-136">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5ef4d-136">Element Information</span></span>



|   <span data-ttu-id="5ef4d-137">Elemento</span><span class="sxs-lookup"><span data-stu-id="5ef4d-137">Element</span></span>    | <span data-ttu-id="5ef4d-138">Valor</span><span class="sxs-lookup"><span data-stu-id="5ef4d-138">Value</span></span>                                                           |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="5ef4d-139">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5ef4d-139">Element type</span></span> | <span data-ttu-id="5ef4d-140">ComplexType [**TitleAreaType**](titleareatype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="5ef4d-140">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="5ef4d-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ef4d-141">Namespace</span></span>    | <span data-ttu-id="5ef4d-142">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="5ef4d-142">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="5ef4d-143">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="5ef4d-143">Schema name</span></span>  | <span data-ttu-id="5ef4d-144">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="5ef4d-144">Journal Reader</span></span>                                                  |



 

 

 



