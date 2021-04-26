---
description: Especifica um tipo a ser incluído de um arquivo XSD.
ms.assetid: dd3894a8-1848-4ae0-ba6c-42ac4fe36ff3
title: elemento typeUri
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9ef0a2482354fcfd962a7e41a7c2b94b54f5cb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998683"
---
# <a name="typeuri-element"></a><span data-ttu-id="cfacd-103">elemento typeUri</span><span class="sxs-lookup"><span data-stu-id="cfacd-103">typeUri element</span></span>

<span data-ttu-id="cfacd-104">Especifica um tipo a ser incluído de um arquivo XSD.</span><span class="sxs-lookup"><span data-stu-id="cfacd-104">Specifies a type to include from an XSD file.</span></span>

## <a name="usage"></a><span data-ttu-id="cfacd-105">Uso</span><span class="sxs-lookup"><span data-stu-id="cfacd-105">Usage</span></span>

``` syntax
<typeUri
  type = "character_string"
  uri = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="cfacd-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="cfacd-106">Attributes</span></span>



| <span data-ttu-id="cfacd-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="cfacd-107">Attribute</span></span>           | <span data-ttu-id="cfacd-108">Type</span><span class="sxs-lookup"><span data-stu-id="cfacd-108">Type</span></span>                         | <span data-ttu-id="cfacd-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cfacd-109">Required</span></span>       | <span data-ttu-id="cfacd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="cfacd-110">Description</span></span>                                                            |
|---------------------|------------------------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="cfacd-111">**tipo**</span><span class="sxs-lookup"><span data-stu-id="cfacd-111">**type**</span></span><br/> | <span data-ttu-id="cfacd-112">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="cfacd-112">character\_string</span></span><br/> | <span data-ttu-id="cfacd-113">Sim</span><span class="sxs-lookup"><span data-stu-id="cfacd-113">Yes</span></span><br/> | <span data-ttu-id="cfacd-114">O nome do tipo.</span><span class="sxs-lookup"><span data-stu-id="cfacd-114">The name of the type.</span></span><br/> <br/>                           |
| <span data-ttu-id="cfacd-115">**uri**</span><span class="sxs-lookup"><span data-stu-id="cfacd-115">**uri**</span></span><br/>  | <span data-ttu-id="cfacd-116">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="cfacd-116">character\_string</span></span><br/> | <span data-ttu-id="cfacd-117">Sim</span><span class="sxs-lookup"><span data-stu-id="cfacd-117">Yes</span></span><br/> | <span data-ttu-id="cfacd-118">O namespace do tipo.</span><span class="sxs-lookup"><span data-stu-id="cfacd-118">The namespace of the type.</span></span> <span data-ttu-id="cfacd-119">Deve ser um URI válido.</span><span class="sxs-lookup"><span data-stu-id="cfacd-119">Must be a valid URI.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="cfacd-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cfacd-120">Child elements</span></span>

<span data-ttu-id="cfacd-121">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="cfacd-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="cfacd-122">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="cfacd-122">Parent elements</span></span>



| <span data-ttu-id="cfacd-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="cfacd-123">Element</span></span>                       | <span data-ttu-id="cfacd-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="cfacd-124">Description</span></span>                                                                       |
|-------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="cfacd-125">**XSD**</span><span class="sxs-lookup"><span data-stu-id="cfacd-125">**xsd**</span></span>](xsd.md)<br/> | <span data-ttu-id="cfacd-126">Especifica um arquivo XSD para processar informações de contrato.</span><span class="sxs-lookup"><span data-stu-id="cfacd-126">Specifies an XSD file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="cfacd-127">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="cfacd-127">Element information</span></span>



| <span data-ttu-id="cfacd-128">Label</span><span class="sxs-lookup"><span data-stu-id="cfacd-128">Label</span></span> | <span data-ttu-id="cfacd-129">Valor</span><span class="sxs-lookup"><span data-stu-id="cfacd-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="cfacd-130">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfacd-130">Minimum supported system</span></span><br/> | <span data-ttu-id="cfacd-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfacd-131">Windows Vista</span></span> |
| <span data-ttu-id="cfacd-132">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="cfacd-132">Can be empty</span></span>                        | <span data-ttu-id="cfacd-133">Sim</span><span class="sxs-lookup"><span data-stu-id="cfacd-133">Yes</span></span>           |



 

 




