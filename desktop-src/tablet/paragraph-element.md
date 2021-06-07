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
ms.openlocfilehash: 2f246294c80814ec809c0a1ca035fcb4741c30c5
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432228"
---
# <a name="paragraph-element"></a><span data-ttu-id="a7f4f-103">Elemento Paragraph</span><span class="sxs-lookup"><span data-stu-id="a7f4f-103">Paragraph Element</span></span>

<span data-ttu-id="a7f4f-104">Contém um parágrafo.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="a7f4f-105">Definição</span><span class="sxs-lookup"><span data-stu-id="a7f4f-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="a7f4f-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a7f4f-106">Parent Elements</span></span>

[<span data-ttu-id="a7f4f-107">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="a7f4f-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="a7f4f-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a7f4f-109">Child Elements</span></span>

[<span data-ttu-id="a7f4f-110">**Descritos**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="a7f4f-111">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="a7f4f-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="a7f4f-112">Attributes</span></span>



| <span data-ttu-id="a7f4f-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="a7f4f-113">Attribute</span></span>       | <span data-ttu-id="a7f4f-114">Type</span><span class="sxs-lookup"><span data-stu-id="a7f4f-114">Type</span></span>                      | <span data-ttu-id="a7f4f-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a7f4f-115">Required</span></span> | <span data-ttu-id="a7f4f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7f4f-116">Description</span></span>                                                                             | <span data-ttu-id="a7f4f-117">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="a7f4f-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="a7f4f-118">**Left**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-118">**Left**</span></span>        | <span data-ttu-id="a7f4f-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-119">**xs:integer**</span></span>            | <span data-ttu-id="a7f4f-120">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a7f4f-120">Required</span></span> | <span data-ttu-id="a7f4f-121">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="a7f4f-122">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-122">Any integer.</span></span>              |
| <span data-ttu-id="a7f4f-123">**Top**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-123">**Top**</span></span>         | <span data-ttu-id="a7f4f-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-124">**xs:integer**</span></span>            | <span data-ttu-id="a7f4f-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a7f4f-125">Required</span></span> | <span data-ttu-id="a7f4f-126">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="a7f4f-127">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-127">Any integer.</span></span>              |
| <span data-ttu-id="a7f4f-128">**Largura**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-128">**Width**</span></span>       | <span data-ttu-id="a7f4f-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a7f4f-130">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a7f4f-130">Required</span></span> | <span data-ttu-id="a7f4f-131">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="a7f4f-132">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="a7f4f-133">**Altura**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-133">**Height**</span></span>      | <span data-ttu-id="a7f4f-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a7f4f-135">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a7f4f-135">Required</span></span> | <span data-ttu-id="a7f4f-136">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="a7f4f-137">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="a7f4f-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-138">**BlockNumber**</span></span> | <span data-ttu-id="a7f4f-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a7f4f-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a7f4f-140">Required</span></span> | <span data-ttu-id="a7f4f-141">Número do bloco.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-141">Block number.</span></span>                                                                           | <span data-ttu-id="a7f4f-142">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="a7f4f-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-143">**LineNumber**</span></span>  | <span data-ttu-id="a7f4f-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a7f4f-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a7f4f-145">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a7f4f-145">Required</span></span> | <span data-ttu-id="a7f4f-146">A linha na qual o parágrafo começa.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="a7f4f-147">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="a7f4f-148">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a7f4f-148">Element Information</span></span>



|  <span data-ttu-id="a7f4f-149">Elemento</span><span class="sxs-lookup"><span data-stu-id="a7f4f-149">Element</span></span>     | <span data-ttu-id="a7f4f-150">Valor</span><span class="sxs-lookup"><span data-stu-id="a7f4f-150">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="a7f4f-151">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a7f4f-151">Element type</span></span> | <span data-ttu-id="a7f4f-152">ComplexType de [**paragraphtype**](paragraphtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="a7f4f-152">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="a7f4f-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7f4f-153">Namespace</span></span>    | <span data-ttu-id="a7f4f-154">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="a7f4f-154">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="a7f4f-155">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="a7f4f-155">Schema name</span></span>  | <span data-ttu-id="a7f4f-156">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="a7f4f-156">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="a7f4f-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7f4f-157">Requirements</span></span>



| <span data-ttu-id="a7f4f-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7f4f-158">Requirement</span></span> | <span data-ttu-id="a7f4f-159">Valor</span><span class="sxs-lookup"><span data-stu-id="a7f4f-159">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f4f-160">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7f4f-160">Header</span></span><br/> | <dl> <span data-ttu-id="a7f4f-161"><dt>Windows.ui.xaml.documents. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7f4f-161"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




