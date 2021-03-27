---
title: 'Função RWTexture3D:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função RWTexture3D:: GetDimensions'
ms.assetid: ba70b955-1e80-4f27-84f1-fc9d26a1f1ab
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
ms.openlocfilehash: 499ab493851257030921e9d55f4873eef8726915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298242"
---
# <a name="rwtexture3dgetdimensions-function"></a><span data-ttu-id="bdb0b-105">Função RWTexture3D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="bdb0b-105">RWTexture3D::GetDimensions function</span></span>

<span data-ttu-id="bdb0b-106">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="bdb0b-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb0b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdb0b-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Depth
);
```

## <a name="parameters"></a><span data-ttu-id="bdb0b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdb0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb0b-109">*Largura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bdb0b-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdb0b-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bdb0b-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bdb0b-111">A largura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="bdb0b-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="bdb0b-112">*Altura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bdb0b-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdb0b-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bdb0b-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bdb0b-114">A altura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="bdb0b-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="bdb0b-115">*Profundidade* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bdb0b-115">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdb0b-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bdb0b-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bdb0b-117">A profundidade do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="bdb0b-117">The resource depth, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb0b-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bdb0b-118">Return value</span></span>

<span data-ttu-id="bdb0b-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bdb0b-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdb0b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdb0b-120">Remarks</span></span>

<span data-ttu-id="bdb0b-121">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="bdb0b-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="bdb0b-122">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="bdb0b-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bdb0b-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="bdb0b-123">Vertex</span></span> | <span data-ttu-id="bdb0b-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="bdb0b-124">Hull</span></span> | <span data-ttu-id="bdb0b-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="bdb0b-125">Domain</span></span> | <span data-ttu-id="bdb0b-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="bdb0b-126">Geometry</span></span> | <span data-ttu-id="bdb0b-127">16x16</span><span class="sxs-lookup"><span data-stu-id="bdb0b-127">Pixel</span></span> | <span data-ttu-id="bdb0b-128">Computação</span><span class="sxs-lookup"><span data-stu-id="bdb0b-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="bdb0b-129">x</span><span class="sxs-lookup"><span data-stu-id="bdb0b-129">x</span></span>     | <span data-ttu-id="bdb0b-130">x</span><span class="sxs-lookup"><span data-stu-id="bdb0b-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bdb0b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdb0b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb0b-132">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="bdb0b-132">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="bdb0b-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bdb0b-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
