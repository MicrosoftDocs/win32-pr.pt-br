---
description: Especifica as propriedades do material.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: Estrutura D3DMATERIAL9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370969"
---
# <a name="d3dmaterial9-structure"></a><span data-ttu-id="56eef-103">Estrutura D3DMATERIAL9</span><span class="sxs-lookup"><span data-stu-id="56eef-103">D3DMATERIAL9 structure</span></span>

<span data-ttu-id="56eef-104">Especifica as propriedades do material.</span><span class="sxs-lookup"><span data-stu-id="56eef-104">Specifies material properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="56eef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56eef-105">Syntax</span></span>


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a><span data-ttu-id="56eef-106">Membros</span><span class="sxs-lookup"><span data-stu-id="56eef-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="56eef-107">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="56eef-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="56eef-108">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="56eef-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56eef-109">Valor que especifica a cor difusa do material.</span><span class="sxs-lookup"><span data-stu-id="56eef-109">Value specifying the diffuse color of the material.</span></span> <span data-ttu-id="56eef-110">Consulte [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="56eef-110">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="56eef-111">**Ambiente**</span><span class="sxs-lookup"><span data-stu-id="56eef-111">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="56eef-112">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="56eef-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56eef-113">Valor que especifica a cor do ambiente do material.</span><span class="sxs-lookup"><span data-stu-id="56eef-113">Value specifying the ambient color of the material.</span></span> <span data-ttu-id="56eef-114">Consulte [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="56eef-114">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="56eef-115">**Especular**</span><span class="sxs-lookup"><span data-stu-id="56eef-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="56eef-116">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="56eef-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56eef-117">Valor que especifica a cor especular do material.</span><span class="sxs-lookup"><span data-stu-id="56eef-117">Value specifying the specular color of the material.</span></span> <span data-ttu-id="56eef-118">Consulte [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="56eef-118">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="56eef-119">**Emissiva**</span><span class="sxs-lookup"><span data-stu-id="56eef-119">**Emissive**</span></span>
</dt> <dd>

<span data-ttu-id="56eef-120">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="56eef-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56eef-121">Valor que especifica a cor emissiva do material.</span><span class="sxs-lookup"><span data-stu-id="56eef-121">Value specifying the emissive color of the material.</span></span> <span data-ttu-id="56eef-122">Consulte [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="56eef-122">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="56eef-123">**Alimentar**</span><span class="sxs-lookup"><span data-stu-id="56eef-123">**Power**</span></span>
</dt> <dd>

<span data-ttu-id="56eef-124">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="56eef-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="56eef-125">Valor de ponto flutuante especificando a nitidez dos realces especulares.</span><span class="sxs-lookup"><span data-stu-id="56eef-125">Floating-point value specifying the sharpness of specular highlights.</span></span> <span data-ttu-id="56eef-126">Quanto maior o valor, mais nítido o realce.</span><span class="sxs-lookup"><span data-stu-id="56eef-126">The higher the value, the sharper the highlight.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56eef-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="56eef-127">Remarks</span></span>

<span data-ttu-id="56eef-128">Para desativar os realces especulares, defina D3DRS \_ SPECULARENABLE como **false**, usando [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="56eef-128">To turn off specular highlights, set D3DRS\_SPECULARENABLE to **FALSE**, using [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span> <span data-ttu-id="56eef-129">Essa é a opção mais rápida porque nenhum realce especular será calculado.</span><span class="sxs-lookup"><span data-stu-id="56eef-129">This is the fastest option because no specular highlights will be calculated.</span></span>

<span data-ttu-id="56eef-130">Para obter mais informações sobre como usar o mecanismo de iluminação para calcular a iluminação especular, consulte [Iluminação especular (Direct3D 9)](specular-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="56eef-130">For more information about using the lighting engine to calculate specular lighting, see [Specular Lighting (Direct3D 9)](specular-lighting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56eef-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56eef-131">Requirements</span></span>



| <span data-ttu-id="56eef-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="56eef-132">Requirement</span></span> | <span data-ttu-id="56eef-133">Valor</span><span class="sxs-lookup"><span data-stu-id="56eef-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56eef-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56eef-134">Header</span></span><br/> | <dl> <span data-ttu-id="56eef-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="56eef-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56eef-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="56eef-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56eef-137">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="56eef-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="56eef-138">**IDirect3DDevice9:: GetMaterial**</span><span class="sxs-lookup"><span data-stu-id="56eef-138">**IDirect3DDevice9::GetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[<span data-ttu-id="56eef-139">**IDirect3DDevice9:: SetMaterial**</span><span class="sxs-lookup"><span data-stu-id="56eef-139">**IDirect3DDevice9::SetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
