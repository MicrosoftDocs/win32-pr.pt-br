---
description: Contém informações de localização e limite para o título da nota, se presente.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Elemento TitleArea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c009d817af9679edda618dd0262c7cbb85a612ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922744"
---
# <a name="titlearea-element"></a><span data-ttu-id="aa53c-103">Elemento TitleArea</span><span class="sxs-lookup"><span data-stu-id="aa53c-103">TitleArea Element</span></span>

<span data-ttu-id="aa53c-104">Contém informações de localização e limite para o título da nota, se presente.</span><span class="sxs-lookup"><span data-stu-id="aa53c-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="aa53c-105">Definição</span><span class="sxs-lookup"><span data-stu-id="aa53c-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="aa53c-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="aa53c-106">Parent Elements</span></span>

[<span data-ttu-id="aa53c-107">**Título**</span><span class="sxs-lookup"><span data-stu-id="aa53c-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="aa53c-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="aa53c-108">Child Elements</span></span>

<span data-ttu-id="aa53c-109">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="aa53c-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="aa53c-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="aa53c-110">Attributes</span></span>



| <span data-ttu-id="aa53c-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="aa53c-111">Attribute</span></span>  | <span data-ttu-id="aa53c-112">Type</span><span class="sxs-lookup"><span data-stu-id="aa53c-112">Type</span></span>                      | <span data-ttu-id="aa53c-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aa53c-113">Required</span></span> | <span data-ttu-id="aa53c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa53c-114">Description</span></span>                                                                             | <span data-ttu-id="aa53c-115">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="aa53c-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="aa53c-116">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="aa53c-116">**Left**</span></span>   | <span data-ttu-id="aa53c-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="aa53c-117">**xs:integer**</span></span>            | <span data-ttu-id="aa53c-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aa53c-118">Required</span></span> | <span data-ttu-id="aa53c-119">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="aa53c-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="aa53c-120">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="aa53c-120">Any integer.</span></span>              |
| <span data-ttu-id="aa53c-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="aa53c-121">**Top**</span></span>    | <span data-ttu-id="aa53c-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="aa53c-122">**xs:integer**</span></span>            | <span data-ttu-id="aa53c-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aa53c-123">Required</span></span> | <span data-ttu-id="aa53c-124">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="aa53c-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="aa53c-125">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="aa53c-125">Any integer.</span></span>              |
| <span data-ttu-id="aa53c-126">**Largura**</span><span class="sxs-lookup"><span data-stu-id="aa53c-126">**Width**</span></span>  | <span data-ttu-id="aa53c-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="aa53c-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="aa53c-128">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aa53c-128">Required</span></span> | <span data-ttu-id="aa53c-129">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="aa53c-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="aa53c-130">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="aa53c-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="aa53c-131">**Altura**</span><span class="sxs-lookup"><span data-stu-id="aa53c-131">**Height**</span></span> | <span data-ttu-id="aa53c-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="aa53c-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="aa53c-133">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aa53c-133">Required</span></span> | <span data-ttu-id="aa53c-134">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="aa53c-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="aa53c-135">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="aa53c-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="aa53c-136">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="aa53c-136">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="aa53c-137">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="aa53c-137">Element type</span></span> | <span data-ttu-id="aa53c-138">ComplexType [**TitleAreaType**](titleareatype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="aa53c-138">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="aa53c-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa53c-139">Namespace</span></span>    | <span data-ttu-id="aa53c-140">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="aa53c-140">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="aa53c-141">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="aa53c-141">Schema name</span></span>  | <span data-ttu-id="aa53c-142">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="aa53c-142">Journal Reader</span></span>                                                  |



 

 

 



