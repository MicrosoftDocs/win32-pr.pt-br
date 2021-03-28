---
title: 'Função Texture2DMSArray:: GetSamplePosition'
description: 'Obtém a posição do exemplo especificado. | Função Texture2DMSArray:: GetSamplePosition'
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
keywords:
- HLSL da função GetSamplePosition
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172868"
---
# <a name="texture2dmsarraygetsampleposition-function"></a><span data-ttu-id="9cce6-105">Função Texture2DMSArray:: GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="9cce6-105">Texture2DMSArray::GetSamplePosition function</span></span>

<span data-ttu-id="9cce6-106">Obtém a posição do exemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="9cce6-106">Gets the position of the specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cce6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cce6-107">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="9cce6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cce6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cce6-109">*sampleindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9cce6-109">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cce6-110">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9cce6-110">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9cce6-111">O índice de base zero de um local de exemplo.</span><span class="sxs-lookup"><span data-stu-id="9cce6-111">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cce6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cce6-112">Return value</span></span>

<span data-ttu-id="9cce6-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="9cce6-113">Type: **float2**</span></span>

<span data-ttu-id="9cce6-114">Um local de exemplo.</span><span class="sxs-lookup"><span data-stu-id="9cce6-114">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cce6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cce6-115">Remarks</span></span>

<span data-ttu-id="9cce6-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="9cce6-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9cce6-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="9cce6-117">Vertex</span></span> | <span data-ttu-id="9cce6-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9cce6-118">Hull</span></span> | <span data-ttu-id="9cce6-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="9cce6-119">Domain</span></span> | <span data-ttu-id="9cce6-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="9cce6-120">Geometry</span></span> | <span data-ttu-id="9cce6-121">16x16</span><span class="sxs-lookup"><span data-stu-id="9cce6-121">Pixel</span></span> | <span data-ttu-id="9cce6-122">Computação</span><span class="sxs-lookup"><span data-stu-id="9cce6-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9cce6-123">x</span><span class="sxs-lookup"><span data-stu-id="9cce6-123">x</span></span>      | <span data-ttu-id="9cce6-124">x</span><span class="sxs-lookup"><span data-stu-id="9cce6-124">x</span></span>    | <span data-ttu-id="9cce6-125">x</span><span class="sxs-lookup"><span data-stu-id="9cce6-125">x</span></span>      | <span data-ttu-id="9cce6-126">x</span><span class="sxs-lookup"><span data-stu-id="9cce6-126">x</span></span>        | <span data-ttu-id="9cce6-127">x</span><span class="sxs-lookup"><span data-stu-id="9cce6-127">x</span></span>     | <span data-ttu-id="9cce6-128">x</span><span class="sxs-lookup"><span data-stu-id="9cce6-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9cce6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cce6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cce6-130">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="9cce6-130">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="9cce6-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9cce6-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
