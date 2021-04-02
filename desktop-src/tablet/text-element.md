---
description: Contém informações de texto da nota do diário.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922645"
---
# <a name="text-element"></a><span data-ttu-id="b0163-103">Elemento Text</span><span class="sxs-lookup"><span data-stu-id="b0163-103">Text Element</span></span>

<span data-ttu-id="b0163-104">Contém informações de texto da nota do diário.</span><span class="sxs-lookup"><span data-stu-id="b0163-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="b0163-105">Definição</span><span class="sxs-lookup"><span data-stu-id="b0163-105">Definition</span></span>

<span data-ttu-id="b0163-106">Quando usado com o [**conteúdo**](content-element--journal-reader.md):</span><span class="sxs-lookup"><span data-stu-id="b0163-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="b0163-107">Ou, quando usado com [**TitleInfo**](titleinfo-element.md) e [**GroupNode**](groupnode-element.md):</span><span class="sxs-lookup"><span data-stu-id="b0163-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="b0163-108">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b0163-108">Parent Elements</span></span>

[<span data-ttu-id="b0163-109">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="b0163-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="b0163-110">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="b0163-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="b0163-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="b0163-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="b0163-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b0163-112">Child Elements</span></span>

<span data-ttu-id="b0163-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b0163-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="b0163-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="b0163-114">Attributes</span></span>

<span data-ttu-id="b0163-115">Não há atributos quando usados com [**TitleInfo**](titleinfo-element.md) e [**GroupNode**](groupnode-element.md).</span><span class="sxs-lookup"><span data-stu-id="b0163-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="b0163-116">Quando usado com [**conteúdo**](content-element--journal-reader.md), os atributos são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="b0163-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="b0163-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="b0163-117">Attribute</span></span>  | <span data-ttu-id="b0163-118">Type</span><span class="sxs-lookup"><span data-stu-id="b0163-118">Type</span></span>                      | <span data-ttu-id="b0163-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b0163-119">Required</span></span> | <span data-ttu-id="b0163-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0163-120">Description</span></span>                                                                             | <span data-ttu-id="b0163-121">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="b0163-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="b0163-122">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="b0163-122">**Left**</span></span>   | <span data-ttu-id="b0163-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="b0163-123">**xs:integer**</span></span>            | <span data-ttu-id="b0163-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b0163-124">Required</span></span> | <span data-ttu-id="b0163-125">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="b0163-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="b0163-126">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="b0163-126">Any integer.</span></span>              |
| <span data-ttu-id="b0163-127">**Top**</span><span class="sxs-lookup"><span data-stu-id="b0163-127">**Top**</span></span>    | <span data-ttu-id="b0163-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="b0163-128">**xs:integer**</span></span>            | <span data-ttu-id="b0163-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b0163-129">Required</span></span> | <span data-ttu-id="b0163-130">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="b0163-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="b0163-131">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="b0163-131">Any integer.</span></span>              |
| <span data-ttu-id="b0163-132">**Largura**</span><span class="sxs-lookup"><span data-stu-id="b0163-132">**Width**</span></span>  | <span data-ttu-id="b0163-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="b0163-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="b0163-134">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b0163-134">Required</span></span> | <span data-ttu-id="b0163-135">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="b0163-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="b0163-136">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="b0163-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="b0163-137">**Altura**</span><span class="sxs-lookup"><span data-stu-id="b0163-137">**Height**</span></span> | <span data-ttu-id="b0163-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="b0163-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="b0163-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b0163-139">Required</span></span> | <span data-ttu-id="b0163-140">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="b0163-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="b0163-141">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="b0163-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="b0163-142">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b0163-142">Element Information</span></span>



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0163-143">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b0163-143">Element type</span></span> | <span data-ttu-id="b0163-144">[**Tipo**](texttype-complex-type.md) complexType (com o elemento Content) ou **xs: String** (com elementos [**GroupNode**](groupnode-element.md) e [**TitleInfo**](titleinfo-element.md) )</span><span class="sxs-lookup"><span data-stu-id="b0163-144">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="b0163-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0163-145">Namespace</span></span>    | <span data-ttu-id="b0163-146">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="b0163-146">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="b0163-147">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="b0163-147">Schema name</span></span>  | <span data-ttu-id="b0163-148">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="b0163-148">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




