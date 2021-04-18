---
description: Contém um parágrafo.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Elemento Paragraph (Windows.ui.xaml.documents. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: bfe3752541bb54571e9802f557e83dcc7632f845
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771763"
---
# <a name="paragraph-element"></a><span data-ttu-id="01ffa-103">Elemento Paragraph</span><span class="sxs-lookup"><span data-stu-id="01ffa-103">Paragraph Element</span></span>

<span data-ttu-id="01ffa-104">Contém um parágrafo.</span><span class="sxs-lookup"><span data-stu-id="01ffa-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="01ffa-105">Definição</span><span class="sxs-lookup"><span data-stu-id="01ffa-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="01ffa-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="01ffa-106">Parent Elements</span></span>

[<span data-ttu-id="01ffa-107">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="01ffa-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="01ffa-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="01ffa-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="01ffa-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="01ffa-109">Child Elements</span></span>

[<span data-ttu-id="01ffa-110">**Linha**</span><span class="sxs-lookup"><span data-stu-id="01ffa-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="01ffa-111">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="01ffa-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="01ffa-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="01ffa-112">Attributes</span></span>



| <span data-ttu-id="01ffa-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="01ffa-113">Attribute</span></span>       | <span data-ttu-id="01ffa-114">Type</span><span class="sxs-lookup"><span data-stu-id="01ffa-114">Type</span></span>                      | <span data-ttu-id="01ffa-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="01ffa-115">Required</span></span> | <span data-ttu-id="01ffa-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="01ffa-116">Description</span></span>                                                                             | <span data-ttu-id="01ffa-117">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="01ffa-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="01ffa-118">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="01ffa-118">**Left**</span></span>        | <span data-ttu-id="01ffa-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="01ffa-119">**xs:integer**</span></span>            | <span data-ttu-id="01ffa-120">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="01ffa-120">Required</span></span> | <span data-ttu-id="01ffa-121">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="01ffa-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="01ffa-122">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="01ffa-122">Any integer.</span></span>              |
| <span data-ttu-id="01ffa-123">**Top**</span><span class="sxs-lookup"><span data-stu-id="01ffa-123">**Top**</span></span>         | <span data-ttu-id="01ffa-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="01ffa-124">**xs:integer**</span></span>            | <span data-ttu-id="01ffa-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="01ffa-125">Required</span></span> | <span data-ttu-id="01ffa-126">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="01ffa-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="01ffa-127">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="01ffa-127">Any integer.</span></span>              |
| <span data-ttu-id="01ffa-128">**Largura**</span><span class="sxs-lookup"><span data-stu-id="01ffa-128">**Width**</span></span>       | <span data-ttu-id="01ffa-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="01ffa-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="01ffa-130">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="01ffa-130">Required</span></span> | <span data-ttu-id="01ffa-131">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="01ffa-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="01ffa-132">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="01ffa-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="01ffa-133">**Altura**</span><span class="sxs-lookup"><span data-stu-id="01ffa-133">**Height**</span></span>      | <span data-ttu-id="01ffa-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="01ffa-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="01ffa-135">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="01ffa-135">Required</span></span> | <span data-ttu-id="01ffa-136">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="01ffa-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="01ffa-137">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="01ffa-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="01ffa-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="01ffa-138">**BlockNumber**</span></span> | <span data-ttu-id="01ffa-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="01ffa-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="01ffa-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="01ffa-140">Required</span></span> | <span data-ttu-id="01ffa-141">Número do bloco.</span><span class="sxs-lookup"><span data-stu-id="01ffa-141">Block number.</span></span>                                                                           | <span data-ttu-id="01ffa-142">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="01ffa-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="01ffa-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="01ffa-143">**LineNumber**</span></span>  | <span data-ttu-id="01ffa-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="01ffa-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="01ffa-145">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="01ffa-145">Required</span></span> | <span data-ttu-id="01ffa-146">A linha na qual o parágrafo começa.</span><span class="sxs-lookup"><span data-stu-id="01ffa-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="01ffa-147">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="01ffa-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="01ffa-148">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="01ffa-148">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="01ffa-149">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="01ffa-149">Element type</span></span> | <span data-ttu-id="01ffa-150">ComplexType de [**paragraphtype**](paragraphtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="01ffa-150">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="01ffa-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="01ffa-151">Namespace</span></span>    | <span data-ttu-id="01ffa-152">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="01ffa-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="01ffa-153">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="01ffa-153">Schema name</span></span>  | <span data-ttu-id="01ffa-154">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="01ffa-154">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="01ffa-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01ffa-155">Requirements</span></span>



| <span data-ttu-id="01ffa-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="01ffa-156">Requirement</span></span> | <span data-ttu-id="01ffa-157">Valor</span><span class="sxs-lookup"><span data-stu-id="01ffa-157">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01ffa-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01ffa-158">Header</span></span><br/> | <dl> <span data-ttu-id="01ffa-159"><dt>Windows.ui.xaml.documents. h</dt></span><span class="sxs-lookup"><span data-stu-id="01ffa-159"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




