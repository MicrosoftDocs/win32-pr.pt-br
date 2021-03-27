---
title: 'Função Texture2DMSArray:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função Texture2DMSArray:: GetDimensions'
ms.assetid: 86d54e0d-f168-479f-b2af-f021b8994741
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
ms.openlocfilehash: e22a225178c2fa965ea842b8c86692d09b87168f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298393"
---
# <a name="texture2dmsarraygetdimensions-function"></a><span data-ttu-id="e0e8e-105">Função Texture2DMSArray:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="e0e8e-105">Texture2DMSArray::GetDimensions function</span></span>

<span data-ttu-id="e0e8e-106">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="e0e8e-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e8e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0e8e-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="e0e8e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0e8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0e8e-109">*Largura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e0e8e-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0e8e-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0e8e-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e0e8e-111">A largura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="e0e8e-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e0e8e-112">*Altura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e0e8e-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0e8e-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0e8e-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e0e8e-114">A altura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="e0e8e-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e0e8e-115">*Elementos* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e0e8e-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0e8e-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0e8e-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e0e8e-117">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="e0e8e-117">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="e0e8e-118">*NumberOfSamples* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e0e8e-118">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0e8e-119">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0e8e-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e0e8e-120">O número de locais de exemplo.</span><span class="sxs-lookup"><span data-stu-id="e0e8e-120">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0e8e-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0e8e-121">Return value</span></span>

<span data-ttu-id="e0e8e-122">Nothing</span><span class="sxs-lookup"><span data-stu-id="e0e8e-122">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="e0e8e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0e8e-123">Remarks</span></span>

<span data-ttu-id="e0e8e-124">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="e0e8e-124">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float Elements,
  out float NumberOfSamples);
```



<span data-ttu-id="e0e8e-125">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e0e8e-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e0e8e-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="e0e8e-126">Vertex</span></span> | <span data-ttu-id="e0e8e-127">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e0e8e-127">Hull</span></span> | <span data-ttu-id="e0e8e-128">Domínio</span><span class="sxs-lookup"><span data-stu-id="e0e8e-128">Domain</span></span> | <span data-ttu-id="e0e8e-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="e0e8e-129">Geometry</span></span> | <span data-ttu-id="e0e8e-130">16x16</span><span class="sxs-lookup"><span data-stu-id="e0e8e-130">Pixel</span></span> | <span data-ttu-id="e0e8e-131">Computação</span><span class="sxs-lookup"><span data-stu-id="e0e8e-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e0e8e-132">x</span><span class="sxs-lookup"><span data-stu-id="e0e8e-132">x</span></span>     | <span data-ttu-id="e0e8e-133">x</span><span class="sxs-lookup"><span data-stu-id="e0e8e-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e0e8e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0e8e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e8e-135">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e0e8e-135">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="e0e8e-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e0e8e-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
