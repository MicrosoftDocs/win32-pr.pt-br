---
title: 'Função Texture2DMS:: GetSamplePosition'
description: Retorna a posição de exemplo do índice de exemplo fornecido.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
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
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499223"
---
# <a name="texture2dmsgetsampleposition-function"></a><span data-ttu-id="69b21-104">Função Texture2DMS:: GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="69b21-104">Texture2DMS::GetSamplePosition function</span></span>

<span data-ttu-id="69b21-105">Retorna a posição de exemplo do índice de exemplo fornecido.</span><span class="sxs-lookup"><span data-stu-id="69b21-105">Returns the sample position for the sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b21-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69b21-106">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="69b21-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69b21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b21-108">*sampleindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69b21-108">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b21-109">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="69b21-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="69b21-110">O índice de base zero de um local de exemplo.</span><span class="sxs-lookup"><span data-stu-id="69b21-110">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b21-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69b21-111">Return value</span></span>

<span data-ttu-id="69b21-112">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="69b21-112">Type: **float2**</span></span>

<span data-ttu-id="69b21-113">Um local de exemplo.</span><span class="sxs-lookup"><span data-stu-id="69b21-113">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="69b21-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="69b21-114">Remarks</span></span>

<span data-ttu-id="69b21-115">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="69b21-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="69b21-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="69b21-116">Vertex</span></span> | <span data-ttu-id="69b21-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="69b21-117">Hull</span></span> | <span data-ttu-id="69b21-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="69b21-118">Domain</span></span> | <span data-ttu-id="69b21-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="69b21-119">Geometry</span></span> | <span data-ttu-id="69b21-120">16x16</span><span class="sxs-lookup"><span data-stu-id="69b21-120">Pixel</span></span> | <span data-ttu-id="69b21-121">Computação</span><span class="sxs-lookup"><span data-stu-id="69b21-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="69b21-122">x</span><span class="sxs-lookup"><span data-stu-id="69b21-122">x</span></span>      | <span data-ttu-id="69b21-123">x</span><span class="sxs-lookup"><span data-stu-id="69b21-123">x</span></span>    | <span data-ttu-id="69b21-124">x</span><span class="sxs-lookup"><span data-stu-id="69b21-124">x</span></span>      | <span data-ttu-id="69b21-125">x</span><span class="sxs-lookup"><span data-stu-id="69b21-125">x</span></span>        | <span data-ttu-id="69b21-126">x</span><span class="sxs-lookup"><span data-stu-id="69b21-126">x</span></span>     | <span data-ttu-id="69b21-127">x</span><span class="sxs-lookup"><span data-stu-id="69b21-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="69b21-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="69b21-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b21-129">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="69b21-129">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="69b21-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="69b21-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
