---
title: Constantes DirectML
description: As constantes a seguir são declaradas em `DirectML.h` .
keywords:
- Constantes
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: ad4ff8c409f79a03cb4021974fe374498926c3e2
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803412"
---
# <a name="directml-constants"></a><span data-ttu-id="e7ace-104">Constantes DirectML</span><span class="sxs-lookup"><span data-stu-id="e7ace-104">DirectML constants</span></span>

<span data-ttu-id="e7ace-105">As constantes a seguir são declaradas em `DirectML.h` .</span><span class="sxs-lookup"><span data-stu-id="e7ace-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="e7ace-106">Constante</span><span class="sxs-lookup"><span data-stu-id="e7ace-106">Constant</span></span> | <span data-ttu-id="e7ace-107">Valor</span><span class="sxs-lookup"><span data-stu-id="e7ace-107">Value</span></span> | <span data-ttu-id="e7ace-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7ace-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="e7ace-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="e7ace-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="e7ace-110">5</span><span class="sxs-lookup"><span data-stu-id="e7ace-110">5</span></span> | <span data-ttu-id="e7ace-111">Os dezenases de DirectML dão suporte a um máximo de 5 dimensões para DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="e7ace-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="e7ace-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="e7ace-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="e7ace-113">8</span><span class="sxs-lookup"><span data-stu-id="e7ace-113">8</span></span> | <span data-ttu-id="e7ace-114">Os dezenases de DirectML dão suporte a um máximo de 8 dimensões para DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="e7ace-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="e7ace-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="e7ace-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="e7ace-116">256</span><span class="sxs-lookup"><span data-stu-id="e7ace-116">256</span></span> | <span data-ttu-id="e7ace-117">Os buffers temporários e persistentes devem ter um endereço base alinhado a 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="e7ace-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="e7ace-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="e7ace-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="e7ace-119">256</span><span class="sxs-lookup"><span data-stu-id="e7ace-119">256</span></span> | <span data-ttu-id="e7ace-120">Os buffers temporários e persistentes devem ter um endereço base alinhado a 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="e7ace-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="e7ace-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="e7ace-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="e7ace-122">16</span><span class="sxs-lookup"><span data-stu-id="e7ace-122">16</span></span> | <span data-ttu-id="e7ace-123">Os tempos de buffer têm um requisito mínimo de alinhamento de endereço base de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="e7ace-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="e7ace-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7ace-124">Requirements</span></span>

| <span data-ttu-id="e7ace-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7ace-125">Requirement</span></span> | <span data-ttu-id="e7ace-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e7ace-126">Value</span></span> |
|-|-|
| <span data-ttu-id="e7ace-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7ace-127">Header</span></span> | <span data-ttu-id="e7ace-128">DirectML. h</span><span class="sxs-lookup"><span data-stu-id="e7ace-128">DirectML.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="e7ace-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7ace-129">See also</span></span>

* [<span data-ttu-id="e7ace-130">Referência do DirectML</span><span class="sxs-lookup"><span data-stu-id="e7ace-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="e7ace-131">Referência de núcleo</span><span class="sxs-lookup"><span data-stu-id="e7ace-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="e7ace-132">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e7ace-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
