---
description: Define um grupo que contém um conjunto de conteúdo agrupado em uma nota de Diário.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Grupo ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432608"
---
# <a name="contentgroup-group"></a><span data-ttu-id="7dccd-103">Grupo ContentGroup</span><span class="sxs-lookup"><span data-stu-id="7dccd-103">ContentGroup Group</span></span>

<span data-ttu-id="7dccd-104">Define um grupo que contém um conjunto de conteúdo agrupado em uma nota de Diário.</span><span class="sxs-lookup"><span data-stu-id="7dccd-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="7dccd-105">Definição</span><span class="sxs-lookup"><span data-stu-id="7dccd-105">Definition</span></span>

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="7dccd-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7dccd-106">Child Elements</span></span>

[<span data-ttu-id="7dccd-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="7dccd-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="7dccd-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="7dccd-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="7dccd-109">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="7dccd-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="7dccd-110">**Desenho**</span><span class="sxs-lookup"><span data-stu-id="7dccd-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="7dccd-111">**Text**</span><span class="sxs-lookup"><span data-stu-id="7dccd-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="7dccd-112">**Imagem**</span><span class="sxs-lookup"><span data-stu-id="7dccd-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="7dccd-113">**Bandeira**</span><span class="sxs-lookup"><span data-stu-id="7dccd-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="7dccd-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="7dccd-114">Attributes</span></span>



| <span data-ttu-id="7dccd-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="7dccd-115">Attribute</span></span>  | <span data-ttu-id="7dccd-116">Type</span><span class="sxs-lookup"><span data-stu-id="7dccd-116">Type</span></span>                      | <span data-ttu-id="7dccd-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7dccd-117">Required</span></span> | <span data-ttu-id="7dccd-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7dccd-118">Description</span></span>                                                                                        | <span data-ttu-id="7dccd-119">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="7dccd-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="7dccd-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="7dccd-120">**Left**</span></span>   | <span data-ttu-id="7dccd-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="7dccd-121">**xs:integer**</span></span>            | <span data-ttu-id="7dccd-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7dccd-122">Required</span></span> | <span data-ttu-id="7dccd-123">A distância da origem até o ponto mais à esquerda na caixa delimitante do elemento.</span><span class="sxs-lookup"><span data-stu-id="7dccd-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="7dccd-124">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="7dccd-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="7dccd-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="7dccd-125">**Top**</span></span>    | <span data-ttu-id="7dccd-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="7dccd-126">**xs:integer**</span></span>            | <span data-ttu-id="7dccd-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7dccd-127">Required</span></span> | <span data-ttu-id="7dccd-128">A distância da origem até o ponto mais alto na caixa delimitada do elemento.</span><span class="sxs-lookup"><span data-stu-id="7dccd-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="7dccd-129">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="7dccd-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="7dccd-130">**Largura**</span><span class="sxs-lookup"><span data-stu-id="7dccd-130">**Width**</span></span>  | <span data-ttu-id="7dccd-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="7dccd-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="7dccd-132">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7dccd-132">Required</span></span> | <span data-ttu-id="7dccd-133">A largura da caixa delimitada para o elemento.</span><span class="sxs-lookup"><span data-stu-id="7dccd-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="7dccd-134">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="7dccd-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="7dccd-135">**Altura**</span><span class="sxs-lookup"><span data-stu-id="7dccd-135">**Height**</span></span> | <span data-ttu-id="7dccd-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="7dccd-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="7dccd-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7dccd-137">Required</span></span> | <span data-ttu-id="7dccd-138">A altura da caixa delimitada para o elemento.</span><span class="sxs-lookup"><span data-stu-id="7dccd-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="7dccd-139">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="7dccd-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="7dccd-140">Informações do Tipo</span><span class="sxs-lookup"><span data-stu-id="7dccd-140">Type Information</span></span>



|  <span data-ttu-id="7dccd-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="7dccd-141">Element</span></span>     | <span data-ttu-id="7dccd-142">Valor</span><span class="sxs-lookup"><span data-stu-id="7dccd-142">Value</span></span>                                                     |
|-------------|--------------------------------------------|
| <span data-ttu-id="7dccd-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="7dccd-143">Namespace</span></span>   | <span data-ttu-id="7dccd-144">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="7dccd-144">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="7dccd-145">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="7dccd-145">Schema name</span></span> | <span data-ttu-id="7dccd-146">Leitor de Diário</span><span class="sxs-lookup"><span data-stu-id="7dccd-146">Journal Reader</span></span>                             |



 

 

 




