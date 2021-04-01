---
description: Define um grupo de atributos que é usado por uma variedade de elementos em um arquivo XML de diário. Ele contém atributos usados para definir os limites (esquerda, superior, altura e largura) de um elemento no documento.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Grupo de atributos BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646551"
---
# <a name="boundstype-attribute-group"></a><span data-ttu-id="cc20b-104">Grupo de atributos BoundsType</span><span class="sxs-lookup"><span data-stu-id="cc20b-104">BoundsType Attribute Group</span></span>

<span data-ttu-id="cc20b-105">Define um grupo de atributos que é usado por uma variedade de elementos em um arquivo XML de diário.</span><span class="sxs-lookup"><span data-stu-id="cc20b-105">Defines an attribute group that is used by a variety of elements in a Journal XML file.</span></span> <span data-ttu-id="cc20b-106">Ele contém atributos usados para definir os limites (esquerda, superior, altura e largura) de um elemento no documento.</span><span class="sxs-lookup"><span data-stu-id="cc20b-106">It contains attributes used to define the bounds (left, top, height, and width) of an element in the document.</span></span>

## <a name="definition"></a><span data-ttu-id="cc20b-107">Definição</span><span class="sxs-lookup"><span data-stu-id="cc20b-107">Definition</span></span>

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a><span data-ttu-id="cc20b-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cc20b-108">Child Elements</span></span>

<span data-ttu-id="cc20b-109">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="cc20b-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="cc20b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc20b-110">Attributes</span></span>



| <span data-ttu-id="cc20b-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="cc20b-111">Attribute</span></span>  | <span data-ttu-id="cc20b-112">Type</span><span class="sxs-lookup"><span data-stu-id="cc20b-112">Type</span></span>                      | <span data-ttu-id="cc20b-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc20b-113">Required</span></span> | <span data-ttu-id="cc20b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc20b-114">Description</span></span>                                                                                        | <span data-ttu-id="cc20b-115">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="cc20b-115">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="cc20b-116">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="cc20b-116">**Left**</span></span>   | <span data-ttu-id="cc20b-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="cc20b-117">**xs:integer**</span></span>            | <span data-ttu-id="cc20b-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc20b-118">Required</span></span> | <span data-ttu-id="cc20b-119">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="cc20b-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="cc20b-120">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="cc20b-120">Any integer.</span></span><br/>              |
| <span data-ttu-id="cc20b-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="cc20b-121">**Top**</span></span>    | <span data-ttu-id="cc20b-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="cc20b-122">**xs:integer**</span></span>            | <span data-ttu-id="cc20b-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc20b-123">Required</span></span> | <span data-ttu-id="cc20b-124">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="cc20b-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="cc20b-125">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="cc20b-125">Any integer.</span></span><br/>              |
| <span data-ttu-id="cc20b-126">**Largura**</span><span class="sxs-lookup"><span data-stu-id="cc20b-126">**Width**</span></span>  | <span data-ttu-id="cc20b-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="cc20b-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="cc20b-128">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc20b-128">Required</span></span> | <span data-ttu-id="cc20b-129">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="cc20b-129">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="cc20b-130">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="cc20b-130">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="cc20b-131">**Altura**</span><span class="sxs-lookup"><span data-stu-id="cc20b-131">**Height**</span></span> | <span data-ttu-id="cc20b-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="cc20b-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="cc20b-133">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc20b-133">Required</span></span> | <span data-ttu-id="cc20b-134">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="cc20b-134">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="cc20b-135">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="cc20b-135">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="cc20b-136">Informações do Tipo</span><span class="sxs-lookup"><span data-stu-id="cc20b-136">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="cc20b-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc20b-137">Namespace</span></span>   | <span data-ttu-id="cc20b-138">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="cc20b-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="cc20b-139">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="cc20b-139">Schema name</span></span> | <span data-ttu-id="cc20b-140">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="cc20b-140">Journal Reader</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="cc20b-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc20b-141">Remarks</span></span>

<span data-ttu-id="cc20b-142">**Left** e **Top** podem ser negativos porque a origem é definida pelas margens, não pela página.</span><span class="sxs-lookup"><span data-stu-id="cc20b-142">**Left** and **Top** can be negative because the origin is defined by the margins, not the page.</span></span>

 

 




