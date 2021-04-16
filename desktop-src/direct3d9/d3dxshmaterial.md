---
description: Características de material de PRT (transferência de radiante computacional) de harmônica esférica (SH).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: Estrutura D3DXSHMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105808346"
---
# <a name="d3dxshmaterial-structure"></a><span data-ttu-id="363a5-103">Estrutura D3DXSHMATERIAL</span><span class="sxs-lookup"><span data-stu-id="363a5-103">D3DXSHMATERIAL structure</span></span>

<span data-ttu-id="363a5-104">Características de material de PRT (transferência de radiante computacional) de harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="363a5-104">Spherical harmonic (SH) precomputed radiance transfer (PRT) material characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="363a5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="363a5-105">Syntax</span></span>


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a><span data-ttu-id="363a5-106">Membros</span><span class="sxs-lookup"><span data-stu-id="363a5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="363a5-107">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="363a5-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="363a5-108">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="363a5-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="363a5-109">Albedo difuso da superfície.</span><span class="sxs-lookup"><span data-stu-id="363a5-109">Diffuse albedo of the surface.</span></span> <span data-ttu-id="363a5-110">Esse valor será ignorado se o objeto for um espelho.</span><span class="sxs-lookup"><span data-stu-id="363a5-110">This value is ignored if the object is a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="363a5-111">**bMirror**</span><span class="sxs-lookup"><span data-stu-id="363a5-111">**bMirror**</span></span>
</dt> <dd>

<span data-ttu-id="363a5-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="363a5-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="363a5-113">Deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="363a5-113">Must be set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="363a5-114">**bSubSurf**</span><span class="sxs-lookup"><span data-stu-id="363a5-114">**bSubSurf**</span></span>
</dt> <dd>

<span data-ttu-id="363a5-115">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="363a5-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="363a5-116">Defina como **true** para habilitar a dispersão de subsuperfície; qualquer objeto que faça a dispersão da subsuperfície não pode ser um espelho.</span><span class="sxs-lookup"><span data-stu-id="363a5-116">Set to **TRUE** to enable subsurface scattering; any object that does subsurface scattering cannot be a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="363a5-117">**RelativeIndexOfRefraction**</span><span class="sxs-lookup"><span data-stu-id="363a5-117">**RelativeIndexOfRefraction**</span></span>
</dt> <dd>

<span data-ttu-id="363a5-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="363a5-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="363a5-119">O índice relativo de refração é a proporção entre dois índices absolutos de refração.</span><span class="sxs-lookup"><span data-stu-id="363a5-119">Relative index of refraction is the ratio between two absolute indexes of refraction.</span></span> <span data-ttu-id="363a5-120">Um índice de refração é a proporção do seno do ângulo de incidência para o seno do ângulo de refração.</span><span class="sxs-lookup"><span data-stu-id="363a5-120">An index of refraction is the ratio of the sine of the angle of incidence to the sine of the angle of refraction.</span></span>

</dd> <dt>

<span data-ttu-id="363a5-121">**Absorção**</span><span class="sxs-lookup"><span data-stu-id="363a5-121">**Absorption**</span></span>
</dt> <dd>

<span data-ttu-id="363a5-122">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="363a5-122">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="363a5-123">O coeficiente de absorção é um parâmetro para a equação de renderização de volume usado para modelar a propagação clara em uma mídia participante.</span><span class="sxs-lookup"><span data-stu-id="363a5-123">The absorption coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> <dt>

<span data-ttu-id="363a5-124">**ReducedScattering**</span><span class="sxs-lookup"><span data-stu-id="363a5-124">**ReducedScattering**</span></span>
</dt> <dd>

<span data-ttu-id="363a5-125">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="363a5-125">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="363a5-126">O coeficiente de dispersão reduzida é um parâmetro para a equação de renderização de volume usado para modelar a propagação clara em uma mídia de participação.</span><span class="sxs-lookup"><span data-stu-id="363a5-126">The reduced scattering coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="363a5-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="363a5-127">Remarks</span></span>

<span data-ttu-id="363a5-128">As cenas não Spectrals usam o canal vermelho dos materiais em vez do valor de luminância.</span><span class="sxs-lookup"><span data-stu-id="363a5-128">Non-spectral scenes use the red channel from the materials instead of the luminance value.</span></span>

<span data-ttu-id="363a5-129">Para obter mais informações sobre o PRT, consulte:</span><span class="sxs-lookup"><span data-stu-id="363a5-129">For more information about PRT see:</span></span>

-   <span data-ttu-id="363a5-130">Jensen, Henrik Wann, et al. SIGGRAPH procedimentos: um modelo prático para transporte de luz de subsuperfície, 2001.</span><span class="sxs-lookup"><span data-stu-id="363a5-130">Jensen, Henrik Wann, et al. Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001.</span></span>

## <a name="requirements"></a><span data-ttu-id="363a5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="363a5-131">Requirements</span></span>



| <span data-ttu-id="363a5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="363a5-132">Requirement</span></span> | <span data-ttu-id="363a5-133">Valor</span><span class="sxs-lookup"><span data-stu-id="363a5-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="363a5-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="363a5-134">Header</span></span><br/> | <dl> <span data-ttu-id="363a5-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="363a5-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="363a5-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="363a5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363a5-137">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="363a5-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
