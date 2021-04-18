---
title: 'Função Texture1D:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função Texture1D:: GetDimensions'
ms.assetid: eb8fc02f-01c8-44b9-9d7e-faf59660c287
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
ms.openlocfilehash: fdd9b79a1cc1fa2a5a8db3e0db7a7163878b066b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506412"
---
# <a name="texture1dgetdimensions-function"></a><span data-ttu-id="39661-105">Função Texture1D:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="39661-105">Texture1D::GetDimensions function</span></span>

<span data-ttu-id="39661-106">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="39661-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="39661-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39661-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="39661-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39661-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39661-109">*MipLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39661-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39661-110">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39661-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39661-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="39661-111">Optional.</span></span> <span data-ttu-id="39661-112">Nível de mipmap (deve ser especificado se *NumberOfLevels* for usado).</span><span class="sxs-lookup"><span data-stu-id="39661-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="39661-113">*Largura* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="39661-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39661-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39661-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39661-115">A largura do recurso, em texels.</span><span class="sxs-lookup"><span data-stu-id="39661-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="39661-116">*NumberOfLevels* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="39661-116">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39661-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39661-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39661-118">O número de níveis de mipmap (também requer *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="39661-118">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39661-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39661-119">Return value</span></span>

<span data-ttu-id="39661-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="39661-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39661-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="39661-121">Remarks</span></span>

<span data-ttu-id="39661-122">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="39661-122">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float NumberOfLevels);

void GetDimensions(out float Width);
```



<span data-ttu-id="39661-123">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="39661-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="39661-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="39661-124">Vertex</span></span> | <span data-ttu-id="39661-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="39661-125">Hull</span></span> | <span data-ttu-id="39661-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="39661-126">Domain</span></span> | <span data-ttu-id="39661-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="39661-127">Geometry</span></span> | <span data-ttu-id="39661-128">16x16</span><span class="sxs-lookup"><span data-stu-id="39661-128">Pixel</span></span> | <span data-ttu-id="39661-129">Computação</span><span class="sxs-lookup"><span data-stu-id="39661-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="39661-130">x</span><span class="sxs-lookup"><span data-stu-id="39661-130">x</span></span>     | <span data-ttu-id="39661-131">x</span><span class="sxs-lookup"><span data-stu-id="39661-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="39661-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="39661-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39661-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="39661-133">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="39661-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="39661-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
