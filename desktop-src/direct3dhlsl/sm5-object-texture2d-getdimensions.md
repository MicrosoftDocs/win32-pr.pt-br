---
title: 'Função Texture2D:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função Texture2D:: GetDimensions'
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989220"
---
# <a name="texture2dgetdimensions-function"></a><span data-ttu-id="ac5ac-105">Função Texture2D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="ac5ac-105">Texture2D::GetDimensions function</span></span>

<span data-ttu-id="ac5ac-106">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac5ac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac5ac-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="ac5ac-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac5ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac5ac-109">*MipLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac5ac-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5ac-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ac5ac-110">Type: **uint**</span></span>

<span data-ttu-id="ac5ac-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-111">Optional.</span></span> <span data-ttu-id="ac5ac-112">O nível de mipmap (deve ser especificado se *NumberOfLevels* for usado).</span><span class="sxs-lookup"><span data-stu-id="ac5ac-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="ac5ac-113">*Largura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ac5ac-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5ac-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ac5ac-114">Type: **uint**</span></span>

<span data-ttu-id="ac5ac-115">A largura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="ac5ac-116">*Altura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ac5ac-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5ac-117">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ac5ac-117">Type: **uint**</span></span>

<span data-ttu-id="ac5ac-118">A altura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="ac5ac-119">*NumberOfLevels* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ac5ac-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5ac-120">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ac5ac-120">Type: **uint**</span></span>

<span data-ttu-id="ac5ac-121">O número de níveis de mipmap (também requer *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="ac5ac-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac5ac-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac5ac-122">Return value</span></span>

<span data-ttu-id="ac5ac-123">Nothing</span><span class="sxs-lookup"><span data-stu-id="ac5ac-123">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="ac5ac-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac5ac-124">Remarks</span></span>

<span data-ttu-id="ac5ac-125">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="ac5ac-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="ac5ac-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ac5ac-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ac5ac-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="ac5ac-127">Vertex</span></span> | <span data-ttu-id="ac5ac-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="ac5ac-128">Hull</span></span> | <span data-ttu-id="ac5ac-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="ac5ac-129">Domain</span></span> | <span data-ttu-id="ac5ac-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="ac5ac-130">Geometry</span></span> | <span data-ttu-id="ac5ac-131">16x16</span><span class="sxs-lookup"><span data-stu-id="ac5ac-131">Pixel</span></span> | <span data-ttu-id="ac5ac-132">Computação</span><span class="sxs-lookup"><span data-stu-id="ac5ac-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ac5ac-133">x</span><span class="sxs-lookup"><span data-stu-id="ac5ac-133">x</span></span>     | <span data-ttu-id="ac5ac-134">x</span><span class="sxs-lookup"><span data-stu-id="ac5ac-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ac5ac-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac5ac-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac5ac-136">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ac5ac-136">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="ac5ac-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ac5ac-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




