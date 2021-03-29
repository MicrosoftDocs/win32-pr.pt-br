---
title: 'Função Texture2DArray:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função Texture2DArray:: GetDimensions'
ms.assetid: 0f6d88b3-195d-4f8c-ac31-ac90129a233e
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
ms.openlocfilehash: b3a78bd12f6924c85d4d395c3cdf73443ae51478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968280"
---
# <a name="texture2darraygetdimensions-function"></a><span data-ttu-id="43ab5-105">Função Texture2DArray:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="43ab5-105">Texture2DArray::GetDimensions function</span></span>

<span data-ttu-id="43ab5-106">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="43ab5-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ab5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43ab5-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="43ab5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43ab5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ab5-109">*MipLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43ab5-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ab5-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43ab5-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="43ab5-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="43ab5-111">Optional.</span></span> <span data-ttu-id="43ab5-112">O nível de mipmap (deve ser especificado se *NumberOfLevels* for usado).</span><span class="sxs-lookup"><span data-stu-id="43ab5-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="43ab5-113">*Largura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="43ab5-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43ab5-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43ab5-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="43ab5-115">A largura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="43ab5-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="43ab5-116">*Altura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="43ab5-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43ab5-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43ab5-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="43ab5-118">A altura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="43ab5-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="43ab5-119">*Elementos* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="43ab5-119">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43ab5-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43ab5-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="43ab5-121">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="43ab5-121">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="43ab5-122">*NumberOfLevels* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="43ab5-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43ab5-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43ab5-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="43ab5-124">O número de níveis de mipmap (também requer *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="43ab5-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43ab5-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43ab5-125">Return value</span></span>

<span data-ttu-id="43ab5-126">Nothing</span><span class="sxs-lookup"><span data-stu-id="43ab5-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="43ab5-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="43ab5-127">Remarks</span></span>

<span data-ttu-id="43ab5-128">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="43ab5-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out float Height,
  out float Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="43ab5-129">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="43ab5-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="43ab5-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="43ab5-130">Vertex</span></span> | <span data-ttu-id="43ab5-131">Envoltória</span><span class="sxs-lookup"><span data-stu-id="43ab5-131">Hull</span></span> | <span data-ttu-id="43ab5-132">Domínio</span><span class="sxs-lookup"><span data-stu-id="43ab5-132">Domain</span></span> | <span data-ttu-id="43ab5-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="43ab5-133">Geometry</span></span> | <span data-ttu-id="43ab5-134">16x16</span><span class="sxs-lookup"><span data-stu-id="43ab5-134">Pixel</span></span> | <span data-ttu-id="43ab5-135">Computação</span><span class="sxs-lookup"><span data-stu-id="43ab5-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="43ab5-136">x</span><span class="sxs-lookup"><span data-stu-id="43ab5-136">x</span></span>     | <span data-ttu-id="43ab5-137">x</span><span class="sxs-lookup"><span data-stu-id="43ab5-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="43ab5-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="43ab5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ab5-139">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="43ab5-139">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="43ab5-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="43ab5-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
