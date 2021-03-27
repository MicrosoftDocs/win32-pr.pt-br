---
title: 'Função Texture2DMS:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função Texture2DMS:: GetDimensions'
ms.assetid: badf4127-2498-4c2e-acc7-20507488fc6b
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
ms.openlocfilehash: f720a10ac73f48ce1f27c5676d706a75178aa8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930375"
---
# <a name="texture2dmsgetdimensions-function"></a><span data-ttu-id="1801c-105">Função Texture2DMS:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="1801c-105">Texture2DMS::GetDimensions function</span></span>

<span data-ttu-id="1801c-106">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="1801c-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="1801c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1801c-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="1801c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1801c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1801c-109">*Largura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1801c-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1801c-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1801c-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1801c-111">A largura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="1801c-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="1801c-112">*Altura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1801c-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1801c-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1801c-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1801c-114">A altura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="1801c-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="1801c-115">*NumberOfSamples* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1801c-115">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1801c-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1801c-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1801c-117">O número de locais de exemplo.</span><span class="sxs-lookup"><span data-stu-id="1801c-117">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1801c-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1801c-118">Return value</span></span>

<span data-ttu-id="1801c-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1801c-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1801c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1801c-120">Remarks</span></span>

<span data-ttu-id="1801c-121">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="1801c-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float NumberOfSamples);
```



<span data-ttu-id="1801c-122">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="1801c-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1801c-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="1801c-123">Vertex</span></span> | <span data-ttu-id="1801c-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="1801c-124">Hull</span></span> | <span data-ttu-id="1801c-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="1801c-125">Domain</span></span> | <span data-ttu-id="1801c-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="1801c-126">Geometry</span></span> | <span data-ttu-id="1801c-127">16x16</span><span class="sxs-lookup"><span data-stu-id="1801c-127">Pixel</span></span> | <span data-ttu-id="1801c-128">Computação</span><span class="sxs-lookup"><span data-stu-id="1801c-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1801c-129">x</span><span class="sxs-lookup"><span data-stu-id="1801c-129">x</span></span>     | <span data-ttu-id="1801c-130">x</span><span class="sxs-lookup"><span data-stu-id="1801c-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1801c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1801c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1801c-132">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="1801c-132">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="1801c-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1801c-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
