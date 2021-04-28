---
description: Função D3DXComputeBoundingBox (D3DX10math. h) – computa uma caixa delimitadora orientada a eixo de coordenadas.
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: Função D3DXComputeBoundingBox (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a12e7e302fb36ffb8856e6402f110e01bb2afb2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103524"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a><span data-ttu-id="fd998-103">Função D3DXComputeBoundingBox (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="fd998-103">D3DXComputeBoundingBox function (D3DX10math.h)</span></span>

<span data-ttu-id="fd998-104">Computa uma caixa delimitadora orientada a eixo de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="fd998-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd998-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd998-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="fd998-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd998-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd998-107">*pFirstPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd998-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd998-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd998-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fd998-109">Ponteiro para a primeira posição.</span><span class="sxs-lookup"><span data-stu-id="fd998-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="fd998-110">*NumVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd998-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd998-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd998-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd998-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="fd998-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="fd998-113">*dwStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd998-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd998-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd998-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd998-115">Contagem ou número de bytes entre vértices.</span><span class="sxs-lookup"><span data-stu-id="fd998-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="fd998-116">*pMin* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fd998-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd998-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd998-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fd998-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , descrevendo o canto inferior esquerdo retornado da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="fd998-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span>

</dd> <dt>

<span data-ttu-id="fd998-119">*pMax* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fd998-119">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd998-120">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd998-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fd998-121">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , descrevendo o canto superior direito retornado da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="fd998-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd998-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fd998-122">Return value</span></span>

<span data-ttu-id="fd998-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd998-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd998-124">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fd998-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fd998-125">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fd998-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd998-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd998-126">Requirements</span></span>



| <span data-ttu-id="fd998-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd998-127">Requirement</span></span> | <span data-ttu-id="fd998-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fd998-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd998-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd998-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fd998-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd998-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="fd998-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd998-131">Library</span></span><br/> | <dl> <span data-ttu-id="fd998-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd998-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd998-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fd998-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd998-134">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="fd998-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
