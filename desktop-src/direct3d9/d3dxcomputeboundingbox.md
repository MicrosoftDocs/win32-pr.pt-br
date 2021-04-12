---
description: Computa uma caixa delimitadora orientada a eixo de coordenadas.
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: Função D3DXComputeBoundingBox (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df0376428153cfc02e499c9e26226cce81154023
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173043"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a><span data-ttu-id="0f61a-103">Função D3DXComputeBoundingBox (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="0f61a-103">D3DXComputeBoundingBox function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="0f61a-104">Computa uma caixa delimitadora orientada a eixo de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="0f61a-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f61a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f61a-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="0f61a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f61a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f61a-107">*pFirstPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f61a-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f61a-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0f61a-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0f61a-109">Ponteiro para a primeira posição.</span><span class="sxs-lookup"><span data-stu-id="0f61a-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="0f61a-110">*NumVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f61a-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f61a-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f61a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f61a-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="0f61a-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="0f61a-113">*dwStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f61a-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f61a-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f61a-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f61a-115">Contagem ou número de bytes entre vértices.</span><span class="sxs-lookup"><span data-stu-id="0f61a-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="0f61a-116">*pMin* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f61a-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f61a-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f61a-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0f61a-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , descrevendo o canto inferior esquerdo retornado da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="0f61a-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span> <span data-ttu-id="0f61a-119">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="0f61a-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0f61a-120">*pMax* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f61a-120">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f61a-121">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f61a-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0f61a-122">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , descrevendo o canto superior direito retornado da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="0f61a-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span> <span data-ttu-id="0f61a-123">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="0f61a-123">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f61a-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f61a-124">Return value</span></span>

<span data-ttu-id="0f61a-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f61a-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f61a-126">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0f61a-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0f61a-127">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0f61a-127">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f61a-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f61a-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0f61a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f61a-129">Requirements</span></span>



| <span data-ttu-id="0f61a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f61a-130">Requirement</span></span> | <span data-ttu-id="0f61a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0f61a-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f61a-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f61a-132">Header</span></span><br/>  | <dl> <span data-ttu-id="0f61a-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f61a-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0f61a-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f61a-134">Library</span></span><br/> | <dl> <span data-ttu-id="0f61a-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f61a-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0f61a-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f61a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f61a-137">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="0f61a-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
