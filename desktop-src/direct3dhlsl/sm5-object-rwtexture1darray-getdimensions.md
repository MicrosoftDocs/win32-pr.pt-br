---
title: 'Função RWTexture1DArray:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função RWTexture1DArray:: GetDimensions'
ms.assetid: 64f2757e-c03c-4f72-b081-1c57656d6e95
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
ms.openlocfilehash: d31d04ccf62b42fede209589a5e4a6760a3091d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172762"
---
# <a name="rwtexture1darraygetdimensions-function"></a><span data-ttu-id="04c65-105">Função RWTexture1DArray:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="04c65-105">RWTexture1DArray::GetDimensions function</span></span>

<span data-ttu-id="04c65-106">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="04c65-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="04c65-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04c65-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="04c65-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04c65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04c65-109">*Largura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04c65-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04c65-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="04c65-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="04c65-111">A largura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="04c65-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="04c65-112">*Elementos* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04c65-112">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04c65-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="04c65-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="04c65-114">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="04c65-114">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04c65-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04c65-115">Return value</span></span>

<span data-ttu-id="04c65-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="04c65-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04c65-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="04c65-117">Remarks</span></span>

<span data-ttu-id="04c65-118">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="04c65-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(out float Width,
  out UINT Elements);
```



<span data-ttu-id="04c65-119">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="04c65-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="04c65-120">Vértice</span><span class="sxs-lookup"><span data-stu-id="04c65-120">Vertex</span></span> | <span data-ttu-id="04c65-121">Envoltória</span><span class="sxs-lookup"><span data-stu-id="04c65-121">Hull</span></span> | <span data-ttu-id="04c65-122">Domínio</span><span class="sxs-lookup"><span data-stu-id="04c65-122">Domain</span></span> | <span data-ttu-id="04c65-123">Geometria</span><span class="sxs-lookup"><span data-stu-id="04c65-123">Geometry</span></span> | <span data-ttu-id="04c65-124">16x16</span><span class="sxs-lookup"><span data-stu-id="04c65-124">Pixel</span></span> | <span data-ttu-id="04c65-125">Computação</span><span class="sxs-lookup"><span data-stu-id="04c65-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="04c65-126">x</span><span class="sxs-lookup"><span data-stu-id="04c65-126">x</span></span>     | <span data-ttu-id="04c65-127">x</span><span class="sxs-lookup"><span data-stu-id="04c65-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="04c65-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="04c65-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04c65-129">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="04c65-129">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="04c65-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="04c65-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
