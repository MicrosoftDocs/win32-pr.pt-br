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
ms.openlocfilehash: d6c3791812f3ac1191f1959150bd5ac7059c54fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105753202"
---
# <a name="directml-constants"></a><span data-ttu-id="189cc-104">Constantes DirectML</span><span class="sxs-lookup"><span data-stu-id="189cc-104">DirectML constants</span></span>

<span data-ttu-id="189cc-105">As constantes a seguir são declaradas em `DirectML.h` .</span><span class="sxs-lookup"><span data-stu-id="189cc-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="189cc-106">Constante</span><span class="sxs-lookup"><span data-stu-id="189cc-106">Constant</span></span> | <span data-ttu-id="189cc-107">Valor</span><span class="sxs-lookup"><span data-stu-id="189cc-107">Value</span></span> | <span data-ttu-id="189cc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="189cc-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="189cc-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="189cc-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="189cc-110">5</span><span class="sxs-lookup"><span data-stu-id="189cc-110">5</span></span> | <span data-ttu-id="189cc-111">Os dezenases de DirectML dão suporte a um máximo de 5 dimensões para DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="189cc-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="189cc-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="189cc-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="189cc-113">8</span><span class="sxs-lookup"><span data-stu-id="189cc-113">8</span></span> | <span data-ttu-id="189cc-114">Os dezenases de DirectML dão suporte a um máximo de 8 dimensões para DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="189cc-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="189cc-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="189cc-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="189cc-116">256</span><span class="sxs-lookup"><span data-stu-id="189cc-116">256</span></span> | <span data-ttu-id="189cc-117">Os buffers temporários e persistentes devem ter um endereço base alinhado a 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="189cc-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="189cc-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="189cc-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="189cc-119">256</span><span class="sxs-lookup"><span data-stu-id="189cc-119">256</span></span> | <span data-ttu-id="189cc-120">Os buffers temporários e persistentes devem ter um endereço base alinhado a 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="189cc-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="189cc-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="189cc-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="189cc-122">16</span><span class="sxs-lookup"><span data-stu-id="189cc-122">16</span></span> | <span data-ttu-id="189cc-123">Os tempos de buffer têm um requisito mínimo de alinhamento de endereço base de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="189cc-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="189cc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="189cc-124">Requirements</span></span>

| <span data-ttu-id="189cc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="189cc-125">Requirement</span></span> | <span data-ttu-id="189cc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="189cc-126">Value</span></span> |
|-|-|
| <span data-ttu-id="189cc-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="189cc-127">Header</span></span> | <span data-ttu-id="189cc-128">D3D12. h</span><span class="sxs-lookup"><span data-stu-id="189cc-128">D3D12.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="189cc-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="189cc-129">See also</span></span>

* [<span data-ttu-id="189cc-130">Referência do DirectML</span><span class="sxs-lookup"><span data-stu-id="189cc-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="189cc-131">Referência de núcleo</span><span class="sxs-lookup"><span data-stu-id="189cc-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="189cc-132">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="189cc-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
