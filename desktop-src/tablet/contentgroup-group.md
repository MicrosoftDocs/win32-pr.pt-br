---
description: Define um grupo que contém um conjunto de conteúdo agrupado em uma nota do diário.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Grupo de grupos de conteúdo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbbc13a3dee796646b6d61ac9ba0bde50880f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011382"
---
# <a name="contentgroup-group"></a><span data-ttu-id="13a11-103">Grupo de grupos de conteúdo</span><span class="sxs-lookup"><span data-stu-id="13a11-103">ContentGroup Group</span></span>

<span data-ttu-id="13a11-104">Define um grupo que contém um conjunto de conteúdo agrupado em uma nota do diário.</span><span class="sxs-lookup"><span data-stu-id="13a11-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="13a11-105">Definição</span><span class="sxs-lookup"><span data-stu-id="13a11-105">Definition</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="13a11-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="13a11-106">Child Elements</span></span>

[<span data-ttu-id="13a11-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="13a11-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="13a11-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="13a11-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="13a11-109">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="13a11-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="13a11-110">**Senha**</span><span class="sxs-lookup"><span data-stu-id="13a11-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="13a11-111">**Texto**</span><span class="sxs-lookup"><span data-stu-id="13a11-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="13a11-112">**Imagem**</span><span class="sxs-lookup"><span data-stu-id="13a11-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="13a11-113">**Sinalizador**</span><span class="sxs-lookup"><span data-stu-id="13a11-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="13a11-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="13a11-114">Attributes</span></span>



| <span data-ttu-id="13a11-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="13a11-115">Attribute</span></span>  | <span data-ttu-id="13a11-116">Type</span><span class="sxs-lookup"><span data-stu-id="13a11-116">Type</span></span>                      | <span data-ttu-id="13a11-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="13a11-117">Required</span></span> | <span data-ttu-id="13a11-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="13a11-118">Description</span></span>                                                                                        | <span data-ttu-id="13a11-119">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="13a11-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="13a11-120">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="13a11-120">**Left**</span></span>   | <span data-ttu-id="13a11-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="13a11-121">**xs:integer**</span></span>            | <span data-ttu-id="13a11-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="13a11-122">Required</span></span> | <span data-ttu-id="13a11-123">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="13a11-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="13a11-124">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="13a11-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="13a11-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="13a11-125">**Top**</span></span>    | <span data-ttu-id="13a11-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="13a11-126">**xs:integer**</span></span>            | <span data-ttu-id="13a11-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="13a11-127">Required</span></span> | <span data-ttu-id="13a11-128">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="13a11-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="13a11-129">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="13a11-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="13a11-130">**Largura**</span><span class="sxs-lookup"><span data-stu-id="13a11-130">**Width**</span></span>  | <span data-ttu-id="13a11-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="13a11-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="13a11-132">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="13a11-132">Required</span></span> | <span data-ttu-id="13a11-133">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="13a11-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="13a11-134">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="13a11-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="13a11-135">**Altura**</span><span class="sxs-lookup"><span data-stu-id="13a11-135">**Height**</span></span> | <span data-ttu-id="13a11-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="13a11-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="13a11-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="13a11-137">Required</span></span> | <span data-ttu-id="13a11-138">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="13a11-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="13a11-139">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="13a11-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="13a11-140">Informações do Tipo</span><span class="sxs-lookup"><span data-stu-id="13a11-140">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="13a11-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="13a11-141">Namespace</span></span>   | <span data-ttu-id="13a11-142">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="13a11-142">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="13a11-143">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="13a11-143">Schema name</span></span> | <span data-ttu-id="13a11-144">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="13a11-144">Journal Reader</span></span>                             |



 

 

 




