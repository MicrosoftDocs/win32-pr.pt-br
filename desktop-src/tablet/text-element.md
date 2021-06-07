---
description: Contém informações de texto da nota Diário.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570f613a06f9fe814bfb1acbdbdba040dbc1119f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432308"
---
# <a name="text-element"></a><span data-ttu-id="0e47f-103">Elemento Text</span><span class="sxs-lookup"><span data-stu-id="0e47f-103">Text Element</span></span>

<span data-ttu-id="0e47f-104">Contém informações de texto da nota Diário.</span><span class="sxs-lookup"><span data-stu-id="0e47f-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="0e47f-105">Definição</span><span class="sxs-lookup"><span data-stu-id="0e47f-105">Definition</span></span>

<span data-ttu-id="0e47f-106">Quando usado com [**Content**](content-element--journal-reader.md):</span><span class="sxs-lookup"><span data-stu-id="0e47f-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="0e47f-107">Ou, quando usado com [**TitleInfo**](titleinfo-element.md) e [**GroupNode:**](groupnode-element.md)</span><span class="sxs-lookup"><span data-stu-id="0e47f-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="0e47f-108">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0e47f-108">Parent Elements</span></span>

[<span data-ttu-id="0e47f-109">**Conteúdo**</span><span class="sxs-lookup"><span data-stu-id="0e47f-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="0e47f-110">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="0e47f-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="0e47f-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="0e47f-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="0e47f-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0e47f-112">Child Elements</span></span>

<span data-ttu-id="0e47f-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0e47f-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="0e47f-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e47f-114">Attributes</span></span>

<span data-ttu-id="0e47f-115">Não há atributos quando usados com [**TitleInfo**](titleinfo-element.md) e [**GroupNode.**](groupnode-element.md)</span><span class="sxs-lookup"><span data-stu-id="0e47f-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="0e47f-116">Quando usado com [**Content**](content-element--journal-reader.md), os atributos são os a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e47f-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="0e47f-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="0e47f-117">Attribute</span></span>  | <span data-ttu-id="0e47f-118">Type</span><span class="sxs-lookup"><span data-stu-id="0e47f-118">Type</span></span>                      | <span data-ttu-id="0e47f-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0e47f-119">Required</span></span> | <span data-ttu-id="0e47f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e47f-120">Description</span></span>                                                                             | <span data-ttu-id="0e47f-121">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0e47f-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="0e47f-122">**Left**</span><span class="sxs-lookup"><span data-stu-id="0e47f-122">**Left**</span></span>   | <span data-ttu-id="0e47f-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="0e47f-123">**xs:integer**</span></span>            | <span data-ttu-id="0e47f-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0e47f-124">Required</span></span> | <span data-ttu-id="0e47f-125">A distância da origem até o ponto mais à esquerda na caixa delimitante do elemento.</span><span class="sxs-lookup"><span data-stu-id="0e47f-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="0e47f-126">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="0e47f-126">Any integer.</span></span>              |
| <span data-ttu-id="0e47f-127">**Top**</span><span class="sxs-lookup"><span data-stu-id="0e47f-127">**Top**</span></span>    | <span data-ttu-id="0e47f-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="0e47f-128">**xs:integer**</span></span>            | <span data-ttu-id="0e47f-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0e47f-129">Required</span></span> | <span data-ttu-id="0e47f-130">A distância da origem até o ponto mais alto na caixa delimitada do elemento.</span><span class="sxs-lookup"><span data-stu-id="0e47f-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="0e47f-131">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="0e47f-131">Any integer.</span></span>              |
| <span data-ttu-id="0e47f-132">**Largura**</span><span class="sxs-lookup"><span data-stu-id="0e47f-132">**Width**</span></span>  | <span data-ttu-id="0e47f-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0e47f-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0e47f-134">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0e47f-134">Required</span></span> | <span data-ttu-id="0e47f-135">A largura da caixa delimitada para o elemento.</span><span class="sxs-lookup"><span data-stu-id="0e47f-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="0e47f-136">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="0e47f-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="0e47f-137">**Altura**</span><span class="sxs-lookup"><span data-stu-id="0e47f-137">**Height**</span></span> | <span data-ttu-id="0e47f-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0e47f-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0e47f-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0e47f-139">Required</span></span> | <span data-ttu-id="0e47f-140">A altura da caixa delimitada para o elemento.</span><span class="sxs-lookup"><span data-stu-id="0e47f-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="0e47f-141">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="0e47f-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="0e47f-142">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0e47f-142">Element Information</span></span>



|   <span data-ttu-id="0e47f-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="0e47f-143">Element</span></span>           |   <span data-ttu-id="0e47f-144">Valor</span><span class="sxs-lookup"><span data-stu-id="0e47f-144">Value</span></span>                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e47f-145">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0e47f-145">Element type</span></span> | <span data-ttu-id="0e47f-146">[**ComplexType TextType**](texttype-complex-type.md) (com o elemento Content) **ou xs:string** (com [**elementos GroupNode**](groupnode-element.md) e [**TitleInfo)**](titleinfo-element.md)</span><span class="sxs-lookup"><span data-stu-id="0e47f-146">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="0e47f-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e47f-147">Namespace</span></span>    | <span data-ttu-id="0e47f-148">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="0e47f-148">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="0e47f-149">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="0e47f-149">Schema name</span></span>  | <span data-ttu-id="0e47f-150">Leitor de Diário</span><span class="sxs-lookup"><span data-stu-id="0e47f-150">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




