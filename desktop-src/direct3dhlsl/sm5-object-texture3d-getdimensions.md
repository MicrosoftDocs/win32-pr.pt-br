---
title: 'Função Texture3D:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função Texture3D:: GetDimensions'
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
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
ms.openlocfilehash: 7a700e0ff065e5f4758241ee0c8252965209a21f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989255"
---
# <a name="texture3dgetdimensions-function"></a><span data-ttu-id="a5421-105">Função Texture3D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="a5421-105">Texture3D::GetDimensions function</span></span>

<span data-ttu-id="a5421-106">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="a5421-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5421-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5421-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="a5421-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5421-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5421-109">*MipLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5421-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5421-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5421-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a5421-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a5421-111">Optional.</span></span> <span data-ttu-id="a5421-112">Nível de mipmap (deve ser especificado se *NumberOfLevels* for usado).</span><span class="sxs-lookup"><span data-stu-id="a5421-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="a5421-113">*Largura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a5421-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5421-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5421-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a5421-115">A largura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="a5421-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="a5421-116">*Altura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a5421-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5421-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5421-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a5421-118">A altura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="a5421-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="a5421-119">*Profundidade* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a5421-119">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5421-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5421-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a5421-121">A profundidade do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="a5421-121">The resource depth, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="a5421-122">*NumberOfLevels* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a5421-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5421-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5421-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a5421-124">O número de níveis de mipmap (também requer *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="a5421-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5421-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5421-125">Return value</span></span>

<span data-ttu-id="a5421-126">Nothing</span><span class="sxs-lookup"><span data-stu-id="a5421-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="a5421-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5421-127">Remarks</span></span>

<span data-ttu-id="a5421-128">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="a5421-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="a5421-129">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a5421-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a5421-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="a5421-130">Vertex</span></span> | <span data-ttu-id="a5421-131">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a5421-131">Hull</span></span> | <span data-ttu-id="a5421-132">Domínio</span><span class="sxs-lookup"><span data-stu-id="a5421-132">Domain</span></span> | <span data-ttu-id="a5421-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="a5421-133">Geometry</span></span> | <span data-ttu-id="a5421-134">16x16</span><span class="sxs-lookup"><span data-stu-id="a5421-134">Pixel</span></span> | <span data-ttu-id="a5421-135">Computação</span><span class="sxs-lookup"><span data-stu-id="a5421-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a5421-136">x</span><span class="sxs-lookup"><span data-stu-id="a5421-136">x</span></span>     | <span data-ttu-id="a5421-137">x</span><span class="sxs-lookup"><span data-stu-id="a5421-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a5421-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5421-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5421-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a5421-139">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="a5421-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a5421-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
