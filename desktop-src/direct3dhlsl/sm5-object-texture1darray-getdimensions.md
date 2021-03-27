---
title: 'Função Texture1DArray:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função Texture1DArray:: GetDimensions'
ms.assetid: a15f1808-296d-43ac-80c0-5cbec0bcb801
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
ms.openlocfilehash: 46cc7e93fc01e14ff34091da4549308730d7cd7c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663910"
---
# <a name="texture1darraygetdimensions-function"></a><span data-ttu-id="8558d-105">Função Texture1DArray:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="8558d-105">Texture1DArray::GetDimensions function</span></span>

<span data-ttu-id="8558d-106">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="8558d-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="8558d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8558d-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="8558d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8558d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8558d-109">*MipLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8558d-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8558d-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8558d-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8558d-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8558d-111">Optional.</span></span> <span data-ttu-id="8558d-112">Nível de mipmap (deve ser especificado se *NumberOfLevels* for usado).</span><span class="sxs-lookup"><span data-stu-id="8558d-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="8558d-113">*Largura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8558d-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8558d-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8558d-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8558d-115">A largura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="8558d-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="8558d-116">*Elementos* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8558d-116">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8558d-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8558d-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8558d-118">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="8558d-118">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="8558d-119">*NumberOfLevels* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8558d-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8558d-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8558d-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8558d-121">O número de níveis de mipmap (também requer *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="8558d-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8558d-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8558d-122">Return value</span></span>

<span data-ttu-id="8558d-123">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8558d-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8558d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="8558d-124">Remarks</span></span>

<span data-ttu-id="8558d-125">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="8558d-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out UINT Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="8558d-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8558d-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8558d-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="8558d-127">Vertex</span></span> | <span data-ttu-id="8558d-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="8558d-128">Hull</span></span> | <span data-ttu-id="8558d-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="8558d-129">Domain</span></span> | <span data-ttu-id="8558d-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="8558d-130">Geometry</span></span> | <span data-ttu-id="8558d-131">16x16</span><span class="sxs-lookup"><span data-stu-id="8558d-131">Pixel</span></span> | <span data-ttu-id="8558d-132">Computação</span><span class="sxs-lookup"><span data-stu-id="8558d-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8558d-133">x</span><span class="sxs-lookup"><span data-stu-id="8558d-133">x</span></span>     | <span data-ttu-id="8558d-134">x</span><span class="sxs-lookup"><span data-stu-id="8558d-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8558d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="8558d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8558d-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8558d-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="8558d-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8558d-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
