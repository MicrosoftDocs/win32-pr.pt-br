---
description: Determina se um raio intersecciona o volume da caixa delimitadora de uma caixa.
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
ms.openlocfilehash: 545036d9564ec20d59c983ffe2d5447659442ba1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787777"
---
# <a name="d3dxboxboundprobe-function"></a><span data-ttu-id="d0d99-103">Função D3DXBoxBoundProbe</span><span class="sxs-lookup"><span data-stu-id="d0d99-103">D3DXBoxBoundProbe function</span></span>

<span data-ttu-id="d0d99-104">Determina se um raio intersecciona o volume da caixa delimitadora de uma caixa.</span><span class="sxs-lookup"><span data-stu-id="d0d99-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0d99-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0d99-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="d0d99-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0d99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0d99-107">*pMin* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0d99-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d99-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d0d99-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d0d99-109">Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que descreve o canto inferior esquerdo da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="d0d99-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="d0d99-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="d0d99-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d0d99-111">*pMax* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0d99-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d99-112">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d0d99-112">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d0d99-113">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , descrevendo o canto superior direito da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="d0d99-113">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="d0d99-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="d0d99-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d0d99-115">*pRayPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0d99-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d99-116">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d0d99-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d0d99-117">Ponteiro para uma estrutura D3DXVECTOR3, especificando a coordenada de origem do raio.</span><span class="sxs-lookup"><span data-stu-id="d0d99-117">Pointer to a D3DXVECTOR3 structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="d0d99-118">*pRayDirection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0d99-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d99-119">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d0d99-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d0d99-120">Ponteiro para uma estrutura D3DXVECTOR3, especificando a direção do raio.</span><span class="sxs-lookup"><span data-stu-id="d0d99-120">Pointer to a D3DXVECTOR3 structure, specifying the direction of the ray.</span></span> <span data-ttu-id="d0d99-121">Esse vetor não deve ser (0, 0, 0), mas não precisa ser normalizado.</span><span class="sxs-lookup"><span data-stu-id="d0d99-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0d99-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0d99-122">Return value</span></span>

<span data-ttu-id="d0d99-123">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0d99-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0d99-124">Retornará **true** se Ray Interseccionar o volume da caixa delimitadora da caixa.</span><span class="sxs-lookup"><span data-stu-id="d0d99-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="d0d99-125">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="d0d99-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0d99-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0d99-126">Remarks</span></span>

<span data-ttu-id="d0d99-127">**D3DXBoxBoundProbe** determina se o raio intersecciona o volume da caixa delimitadora da caixa, não apenas a superfície da caixa.</span><span class="sxs-lookup"><span data-stu-id="d0d99-127">**D3DXBoxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="d0d99-128">Os valores passados para **D3DXBoxBoundProbe** são xmin, xMax, ymin, ymax, zmin e Zmax.</span><span class="sxs-lookup"><span data-stu-id="d0d99-128">The values passed to **D3DXBoxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="d0d99-129">Portanto, o seguinte define os cantos da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="d0d99-129">Thus, the following defines the corners of the bounding box.</span></span>


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



<span data-ttu-id="d0d99-130">A profundidade da caixa delimitadora na direção z é Zmax-zmin, na direção y, ymax-ymin e, na direção x, é xmax-xmin.</span><span class="sxs-lookup"><span data-stu-id="d0d99-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="d0d99-131">Por exemplo, com os seguintes vetores mínimo e máximo, min (-1,-1,-1) e Max (1, 1, 1), a caixa delimitadora é definida da maneira a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0d99-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d0d99-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0d99-132">Requirements</span></span>



| <span data-ttu-id="d0d99-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0d99-133">Requirement</span></span> | <span data-ttu-id="d0d99-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d0d99-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0d99-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0d99-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d0d99-136"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0d99-136"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="d0d99-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0d99-137">Library</span></span><br/> | <dl> <span data-ttu-id="d0d99-138"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0d99-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d0d99-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0d99-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0d99-140">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="d0d99-140">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
