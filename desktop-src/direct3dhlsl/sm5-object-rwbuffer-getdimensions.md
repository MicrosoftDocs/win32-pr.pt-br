---
title: 'Função RWBuffer:: GetDimensions'
description: 'Obtém o comprimento do buffer. | Função RWBuffer:: GetDimensions'
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
keywords:
- Função GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 98e419d3e77a27f211f0e063573caffcd6c61ce8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989234"
---
# <a name="rwbuffergetdimensions-function"></a><span data-ttu-id="60e41-105">Função RWBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="60e41-105">RWBuffer::GetDimensions function</span></span>

<span data-ttu-id="60e41-106">Obtém o comprimento do buffer.</span><span class="sxs-lookup"><span data-stu-id="60e41-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e41-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60e41-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="60e41-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60e41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60e41-109">*esmaecer* \[\]</span><span class="sxs-lookup"><span data-stu-id="60e41-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60e41-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="60e41-110">Type: **uint**</span></span>

<span data-ttu-id="60e41-111">O comprimento, em bytes, do buffer.</span><span class="sxs-lookup"><span data-stu-id="60e41-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60e41-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60e41-112">Return value</span></span>

<span data-ttu-id="60e41-113">Nothing</span><span class="sxs-lookup"><span data-stu-id="60e41-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="60e41-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="60e41-114">Remarks</span></span>

<span data-ttu-id="60e41-115">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="60e41-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="60e41-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="60e41-116">Vertex</span></span> | <span data-ttu-id="60e41-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="60e41-117">Hull</span></span> | <span data-ttu-id="60e41-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="60e41-118">Domain</span></span> | <span data-ttu-id="60e41-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="60e41-119">Geometry</span></span> | <span data-ttu-id="60e41-120">16x16</span><span class="sxs-lookup"><span data-stu-id="60e41-120">Pixel</span></span> | <span data-ttu-id="60e41-121">Computação</span><span class="sxs-lookup"><span data-stu-id="60e41-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="60e41-122">x</span><span class="sxs-lookup"><span data-stu-id="60e41-122">x</span></span>     | <span data-ttu-id="60e41-123">x</span><span class="sxs-lookup"><span data-stu-id="60e41-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="60e41-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="60e41-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e41-125">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="60e41-125">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="60e41-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="60e41-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




