---
title: 'Função RWTexture2D:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função RWTexture2D:: GetDimensions'
ms.assetid: bc55622d-fbff-4aeb-aceb-4eb2cfc7ac28
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
ms.openlocfilehash: 19a6711e8f04afdb2f5ec66ff33c8aaf1d59b40c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104091928"
---
# <a name="rwtexture2dgetdimensions-function"></a><span data-ttu-id="3f7fa-105">Função RWTexture2D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="3f7fa-105">RWTexture2D::GetDimensions function</span></span>

<span data-ttu-id="3f7fa-106">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="3f7fa-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f7fa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f7fa-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height
);
```

## <a name="parameters"></a><span data-ttu-id="3f7fa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f7fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f7fa-109">*Largura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3f7fa-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f7fa-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3f7fa-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3f7fa-111">A largura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="3f7fa-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="3f7fa-112">*Altura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3f7fa-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f7fa-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3f7fa-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3f7fa-114">A altura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="3f7fa-114">The resource height, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f7fa-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f7fa-115">Return value</span></span>

<span data-ttu-id="3f7fa-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3f7fa-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f7fa-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f7fa-117">Remarks</span></span>

<span data-ttu-id="3f7fa-118">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="3f7fa-118">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="3f7fa-119">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3f7fa-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3f7fa-120">Vértice</span><span class="sxs-lookup"><span data-stu-id="3f7fa-120">Vertex</span></span> | <span data-ttu-id="3f7fa-121">Envoltória</span><span class="sxs-lookup"><span data-stu-id="3f7fa-121">Hull</span></span> | <span data-ttu-id="3f7fa-122">Domínio</span><span class="sxs-lookup"><span data-stu-id="3f7fa-122">Domain</span></span> | <span data-ttu-id="3f7fa-123">Geometria</span><span class="sxs-lookup"><span data-stu-id="3f7fa-123">Geometry</span></span> | <span data-ttu-id="3f7fa-124">16x16</span><span class="sxs-lookup"><span data-stu-id="3f7fa-124">Pixel</span></span> | <span data-ttu-id="3f7fa-125">Computação</span><span class="sxs-lookup"><span data-stu-id="3f7fa-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3f7fa-126">x</span><span class="sxs-lookup"><span data-stu-id="3f7fa-126">x</span></span>     | <span data-ttu-id="3f7fa-127">x</span><span class="sxs-lookup"><span data-stu-id="3f7fa-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3f7fa-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f7fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f7fa-129">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="3f7fa-129">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="3f7fa-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3f7fa-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
