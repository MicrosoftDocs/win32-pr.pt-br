---
description: Contém dados binários codificados para uma imagem no documento do diário, se presente.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Elemento de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8437495a4c248a8e5bc68a0f7b75a2cf7d761387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807168"
---
# <a name="image-element"></a><span data-ttu-id="5607d-103">Elemento de imagem</span><span class="sxs-lookup"><span data-stu-id="5607d-103">Image Element</span></span>

<span data-ttu-id="5607d-104">Contém dados binários codificados para uma imagem no documento do diário, se presente.</span><span class="sxs-lookup"><span data-stu-id="5607d-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="5607d-105">Definição</span><span class="sxs-lookup"><span data-stu-id="5607d-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="5607d-106">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5607d-106">Parent Elements</span></span>

[<span data-ttu-id="5607d-107">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="5607d-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="5607d-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="5607d-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="5607d-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5607d-109">Child Elements</span></span>

<span data-ttu-id="5607d-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5607d-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="5607d-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="5607d-111">Attributes</span></span>



| <span data-ttu-id="5607d-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="5607d-112">Attribute</span></span>  | <span data-ttu-id="5607d-113">Type</span><span class="sxs-lookup"><span data-stu-id="5607d-113">Type</span></span>                      | <span data-ttu-id="5607d-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5607d-114">Required</span></span> | <span data-ttu-id="5607d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5607d-115">Description</span></span>                                                                             | <span data-ttu-id="5607d-116">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5607d-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="5607d-117">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="5607d-117">**Left**</span></span>   | <span data-ttu-id="5607d-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5607d-118">**xs:integer**</span></span>            | <span data-ttu-id="5607d-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5607d-119">Required</span></span> | <span data-ttu-id="5607d-120">A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5607d-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="5607d-121">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="5607d-121">Any integer.</span></span>              |
| <span data-ttu-id="5607d-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="5607d-122">**Top**</span></span>    | <span data-ttu-id="5607d-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5607d-123">**xs:integer**</span></span>            | <span data-ttu-id="5607d-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5607d-124">Required</span></span> | <span data-ttu-id="5607d-125">A distância da origem até o ponto superior na caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5607d-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="5607d-126">Qualquer inteiro.</span><span class="sxs-lookup"><span data-stu-id="5607d-126">Any integer.</span></span>              |
| <span data-ttu-id="5607d-127">**Largura**</span><span class="sxs-lookup"><span data-stu-id="5607d-127">**Width**</span></span>  | <span data-ttu-id="5607d-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5607d-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5607d-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5607d-129">Required</span></span> | <span data-ttu-id="5607d-130">A largura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5607d-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="5607d-131">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="5607d-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="5607d-132">**Altura**</span><span class="sxs-lookup"><span data-stu-id="5607d-132">**Height**</span></span> | <span data-ttu-id="5607d-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5607d-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5607d-134">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5607d-134">Required</span></span> | <span data-ttu-id="5607d-135">A altura da caixa delimitadora para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5607d-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="5607d-136">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="5607d-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="5607d-137">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5607d-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="5607d-138">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5607d-138">Element type</span></span> | <span data-ttu-id="5607d-139">ComplexType [**ImageType**](imagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="5607d-139">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="5607d-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="5607d-140">Namespace</span></span>    | <span data-ttu-id="5607d-141">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="5607d-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="5607d-142">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="5607d-142">Schema name</span></span>  | <span data-ttu-id="5607d-143">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="5607d-143">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="5607d-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="5607d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5607d-145">**Tela de fundo**</span><span class="sxs-lookup"><span data-stu-id="5607d-145">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



