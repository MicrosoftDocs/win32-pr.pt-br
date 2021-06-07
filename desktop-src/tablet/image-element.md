---
description: Contém dados binários codificados para uma imagem no documento do diário, se presente.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Elemento de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9dd3b37a39ce45ee0294f46922fbab376523b64
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432578"
---
# <a name="image-element"></a><span data-ttu-id="c6ffe-103">Elemento de imagem</span><span class="sxs-lookup"><span data-stu-id="c6ffe-103">Image Element</span></span>

<span data-ttu-id="c6ffe-104">Contém dados binários codificados para uma imagem no documento do diário, se presente.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="c6ffe-105">Definição</span><span class="sxs-lookup"><span data-stu-id="c6ffe-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="c6ffe-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c6ffe-106">Parent Elements</span></span>

[<span data-ttu-id="c6ffe-107">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="c6ffe-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="c6ffe-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c6ffe-109">Child Elements</span></span>

<span data-ttu-id="c6ffe-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="c6ffe-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="c6ffe-111">Attributes</span></span>



| <span data-ttu-id="c6ffe-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="c6ffe-112">Attribute</span></span>  | <span data-ttu-id="c6ffe-113">Type</span><span class="sxs-lookup"><span data-stu-id="c6ffe-113">Type</span></span>                      | <span data-ttu-id="c6ffe-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c6ffe-114">Required</span></span> | <span data-ttu-id="c6ffe-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6ffe-115">Description</span></span>                                                                             | <span data-ttu-id="c6ffe-116">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="c6ffe-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="c6ffe-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-117">**Left**</span></span>   | <span data-ttu-id="c6ffe-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-118">**xs:integer**</span></span>            | <span data-ttu-id="c6ffe-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c6ffe-119">Required</span></span> | <span data-ttu-id="c6ffe-120">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="c6ffe-121">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-121">Any integer.</span></span>              |
| <span data-ttu-id="c6ffe-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-122">**Top**</span></span>    | <span data-ttu-id="c6ffe-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-123">**xs:integer**</span></span>            | <span data-ttu-id="c6ffe-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c6ffe-124">Required</span></span> | <span data-ttu-id="c6ffe-125">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="c6ffe-126">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-126">Any integer.</span></span>              |
| <span data-ttu-id="c6ffe-127">**Largura**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-127">**Width**</span></span>  | <span data-ttu-id="c6ffe-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="c6ffe-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c6ffe-129">Required</span></span> | <span data-ttu-id="c6ffe-130">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="c6ffe-131">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="c6ffe-132">**Altura**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-132">**Height**</span></span> | <span data-ttu-id="c6ffe-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="c6ffe-134">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c6ffe-134">Required</span></span> | <span data-ttu-id="c6ffe-135">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="c6ffe-136">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="c6ffe-137">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c6ffe-137">Element Information</span></span>



|  <span data-ttu-id="c6ffe-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="c6ffe-138">Element</span></span>     | <span data-ttu-id="c6ffe-139">Valor</span><span class="sxs-lookup"><span data-stu-id="c6ffe-139">Value</span></span>                                                     |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="c6ffe-140">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c6ffe-140">Element type</span></span> | <span data-ttu-id="c6ffe-141">ComplexType [**ImageType**](imagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="c6ffe-141">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="c6ffe-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6ffe-142">Namespace</span></span>    | <span data-ttu-id="c6ffe-143">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="c6ffe-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="c6ffe-144">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="c6ffe-144">Schema name</span></span>  | <span data-ttu-id="c6ffe-145">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="c6ffe-145">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="c6ffe-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6ffe-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ffe-147">**Segundo plano**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-147">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



