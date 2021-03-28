---
title: 'Buffer:: função GetDimensions'
description: 'Obtém o comprimento do buffer. | Buffer:: função GetDimensions'
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: c7f1ad1da7600e65d7442c1b2431535e2fdcf38c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968285"
---
# <a name="buffergetdimensions-function"></a><span data-ttu-id="bbdf0-105">Buffer:: função GetDimensions</span><span class="sxs-lookup"><span data-stu-id="bbdf0-105">Buffer::GetDimensions function</span></span>

<span data-ttu-id="bbdf0-106">Obtém o comprimento do buffer.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbdf0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbdf0-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="bbdf0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbdf0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbdf0-109">*esmaecer* \[\]</span><span class="sxs-lookup"><span data-stu-id="bbdf0-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbdf0-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="bbdf0-110">Type: **uint**</span></span>

<span data-ttu-id="bbdf0-111">O comprimento, em bytes, do buffer.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbdf0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bbdf0-112">Return value</span></span>

<span data-ttu-id="bbdf0-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbdf0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbdf0-114">Remarks</span></span>

<span data-ttu-id="bbdf0-115">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="bbdf0-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bbdf0-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="bbdf0-116">Vertex</span></span> | <span data-ttu-id="bbdf0-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="bbdf0-117">Hull</span></span> | <span data-ttu-id="bbdf0-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="bbdf0-118">Domain</span></span> | <span data-ttu-id="bbdf0-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="bbdf0-119">Geometry</span></span> | <span data-ttu-id="bbdf0-120">16x16</span><span class="sxs-lookup"><span data-stu-id="bbdf0-120">Pixel</span></span> | <span data-ttu-id="bbdf0-121">Computação</span><span class="sxs-lookup"><span data-stu-id="bbdf0-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bbdf0-122">x</span><span class="sxs-lookup"><span data-stu-id="bbdf0-122">x</span></span>      | <span data-ttu-id="bbdf0-123">x</span><span class="sxs-lookup"><span data-stu-id="bbdf0-123">x</span></span>    | <span data-ttu-id="bbdf0-124">x</span><span class="sxs-lookup"><span data-stu-id="bbdf0-124">x</span></span>      | <span data-ttu-id="bbdf0-125">x</span><span class="sxs-lookup"><span data-stu-id="bbdf0-125">x</span></span>        | <span data-ttu-id="bbdf0-126">x</span><span class="sxs-lookup"><span data-stu-id="bbdf0-126">x</span></span>     | <span data-ttu-id="bbdf0-127">x</span><span class="sxs-lookup"><span data-stu-id="bbdf0-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bbdf0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbdf0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbdf0-129">Buffer</span><span class="sxs-lookup"><span data-stu-id="bbdf0-129">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="bbdf0-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bbdf0-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




