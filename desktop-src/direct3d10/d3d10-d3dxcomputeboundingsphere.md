---
description: Função D3DXComputeBoundingSphere (D3DX10math. h) – computa uma esfera delimitadora para a malha.
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: Função D3DXComputeBoundingSphere (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0041d775b21d1af37bc51d6ec2f432e616b2abd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113294"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a><span data-ttu-id="4db84-103">Função D3DXComputeBoundingSphere (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="4db84-103">D3DXComputeBoundingSphere function (D3DX10math.h)</span></span>

<span data-ttu-id="4db84-104">Computa uma esfera delimitadora para a malha.</span><span class="sxs-lookup"><span data-stu-id="4db84-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db84-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4db84-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="4db84-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4db84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4db84-107">*pFirstPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4db84-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db84-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4db84-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4db84-109">Ponteiro para a primeira posição.</span><span class="sxs-lookup"><span data-stu-id="4db84-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="4db84-110">*NumVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4db84-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db84-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4db84-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4db84-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="4db84-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="4db84-113">*dwStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4db84-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db84-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4db84-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4db84-115">Número de bytes entre os vetores de posição.</span><span class="sxs-lookup"><span data-stu-id="4db84-115">Number of bytes between position vectors.</span></span>

</dd> <dt>

<span data-ttu-id="4db84-116">*pCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4db84-116">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db84-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4db84-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4db84-118">Estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , definindo o centro de coordenadas da esfera delimitadora retornada.</span><span class="sxs-lookup"><span data-stu-id="4db84-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="4db84-119">*pRadius* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4db84-119">*pRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db84-120">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4db84-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4db84-121">Raio da esfera delimitadora retornada.</span><span class="sxs-lookup"><span data-stu-id="4db84-121">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4db84-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4db84-122">Return value</span></span>

<span data-ttu-id="4db84-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4db84-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4db84-124">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4db84-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4db84-125">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4db84-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db84-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4db84-126">Requirements</span></span>



| <span data-ttu-id="4db84-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4db84-127">Requirement</span></span> | <span data-ttu-id="4db84-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4db84-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4db84-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4db84-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4db84-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4db84-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="4db84-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4db84-131">Library</span></span><br/> | <dl> <span data-ttu-id="4db84-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4db84-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4db84-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4db84-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db84-134">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="4db84-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
