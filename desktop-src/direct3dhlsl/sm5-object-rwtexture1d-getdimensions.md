---
title: 'Função RWTexture1D:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função RWTexture1D:: GetDimensions'
ms.assetid: 1bbd53ed-9396-4e8e-b2f3-3bd85f6e1a90
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
ms.openlocfilehash: b65f0113ecf2c91786e45c35f5e8e832744bc952
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968282"
---
# <a name="rwtexture1dgetdimensions-function"></a><span data-ttu-id="04983-105">Função RWTexture1D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="04983-105">RWTexture1D::GetDimensions function</span></span>

<span data-ttu-id="04983-106">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="04983-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="04983-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04983-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width
);
```

## <a name="parameters"></a><span data-ttu-id="04983-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04983-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04983-109">*Largura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04983-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04983-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="04983-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="04983-111">A largura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="04983-111">The resource width, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04983-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04983-112">Return value</span></span>

<span data-ttu-id="04983-113">Nothing</span><span class="sxs-lookup"><span data-stu-id="04983-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="04983-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="04983-114">Remarks</span></span>

<span data-ttu-id="04983-115">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="04983-115">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width);

void GetDimensions(out float Width);
```



<span data-ttu-id="04983-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="04983-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="04983-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="04983-117">Vertex</span></span> | <span data-ttu-id="04983-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="04983-118">Hull</span></span> | <span data-ttu-id="04983-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="04983-119">Domain</span></span> | <span data-ttu-id="04983-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="04983-120">Geometry</span></span> | <span data-ttu-id="04983-121">16x16</span><span class="sxs-lookup"><span data-stu-id="04983-121">Pixel</span></span> | <span data-ttu-id="04983-122">Computação</span><span class="sxs-lookup"><span data-stu-id="04983-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="04983-123">x</span><span class="sxs-lookup"><span data-stu-id="04983-123">x</span></span>     | <span data-ttu-id="04983-124">x</span><span class="sxs-lookup"><span data-stu-id="04983-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="04983-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="04983-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04983-126">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="04983-126">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="04983-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="04983-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
