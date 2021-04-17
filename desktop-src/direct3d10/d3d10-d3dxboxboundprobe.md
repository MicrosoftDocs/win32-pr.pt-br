---
description: A função D3DXBoxBoundProbe (D3DX10math. h) determina se um raio intersecciona o volume da caixa delimitadora de uma caixa.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: Função D3DXBoxBoundProbe (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187815"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a><span data-ttu-id="9d3ee-103">Função D3DXBoxBoundProbe (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="9d3ee-103">D3DXBoxBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="9d3ee-104">Determina se um raio intersecciona o volume da caixa delimitadora de uma caixa.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d3ee-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="9d3ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d3ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d3ee-107">*pMin* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d3ee-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d3ee-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d3ee-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9d3ee-109">Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que descreve o canto inferior esquerdo da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="9d3ee-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9d3ee-111">*pMax* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d3ee-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d3ee-112">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d3ee-112">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9d3ee-113">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , descrevendo o canto superior direito da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-113">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="9d3ee-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9d3ee-115">*pRayPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d3ee-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d3ee-116">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d3ee-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9d3ee-117">Ponteiro para uma estrutura D3DXVECTOR3, especificando a coordenada de origem do raio.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-117">Pointer to a D3DXVECTOR3 structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="9d3ee-118">*pRayDirection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d3ee-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d3ee-119">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d3ee-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9d3ee-120">Ponteiro para uma estrutura D3DXVECTOR3, especificando a direção do raio.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-120">Pointer to a D3DXVECTOR3 structure, specifying the direction of the ray.</span></span> <span data-ttu-id="9d3ee-121">Esse vetor não deve ser (0, 0, 0), mas não precisa ser normalizado.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d3ee-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d3ee-122">Return value</span></span>

<span data-ttu-id="9d3ee-123">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d3ee-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9d3ee-124">Retornará **true** se Ray Interseccionar o volume da caixa delimitadora da caixa.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="9d3ee-125">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d3ee-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d3ee-126">Remarks</span></span>

<span data-ttu-id="9d3ee-127">**D3DXBoxBoundProbe** determina se o raio intersecciona o volume da caixa delimitadora da caixa, não apenas a superfície da caixa.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-127">**D3DXBoxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="9d3ee-128">Os valores passados para **D3DXBoxBoundProbe** são xmin, xMax, ymin, ymax, zmin e Zmax.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-128">The values passed to **D3DXBoxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="9d3ee-129">Portanto, o seguinte define os cantos da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-129">Thus, the following defines the corners of the bounding box.</span></span>


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



<span data-ttu-id="9d3ee-130">A profundidade da caixa delimitadora na direção z é Zmax-zmin, na direção y, ymax-ymin e, na direção x, é xmax-xmin.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="9d3ee-131">Por exemplo, com os seguintes vetores mínimo e máximo, min (-1,-1,-1) e Max (1, 1, 1), a caixa delimitadora é definida da maneira a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a><span data-ttu-id="9d3ee-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d3ee-132">Requirements</span></span>



| <span data-ttu-id="9d3ee-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d3ee-133">Requirement</span></span> | <span data-ttu-id="9d3ee-134">Valor</span><span class="sxs-lookup"><span data-stu-id="9d3ee-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d3ee-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d3ee-135">Header</span></span>  | <span data-ttu-id="9d3ee-136">D3DX10math. h</span><span class="sxs-lookup"><span data-stu-id="9d3ee-136">D3DX10math.h</span></span> |
| <span data-ttu-id="9d3ee-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d3ee-137">Library</span></span> | <span data-ttu-id="9d3ee-138">D3DX10. lib</span><span class="sxs-lookup"><span data-stu-id="9d3ee-138">D3DX10.lib</span></span>  |



## <a name="see-also"></a><span data-ttu-id="9d3ee-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d3ee-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d3ee-140">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="9d3ee-140">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
