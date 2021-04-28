---
description: Função D3DXComputeBoundingSphere (D3DX9Mesh. h) – computa uma esfera delimitadora para a malha.
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: Função D3DXComputeBoundingSphere (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dbfccb13dfe15b06de98ddba114cdc62c5f4ec05
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115814"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a><span data-ttu-id="9cb8b-103">Função D3DXComputeBoundingSphere (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="9cb8b-103">D3DXComputeBoundingSphere function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="9cb8b-104">Computa uma esfera delimitadora para a malha.</span><span class="sxs-lookup"><span data-stu-id="9cb8b-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cb8b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cb8b-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="9cb8b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cb8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cb8b-107">*pFirstPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9cb8b-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb8b-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9cb8b-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9cb8b-109">Ponteiro para a primeira posição.</span><span class="sxs-lookup"><span data-stu-id="9cb8b-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="9cb8b-110">*NumVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9cb8b-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb8b-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9cb8b-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9cb8b-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="9cb8b-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="9cb8b-113">*dwStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9cb8b-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb8b-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9cb8b-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9cb8b-115">Número de bytes entre os vetores de posição.</span><span class="sxs-lookup"><span data-stu-id="9cb8b-115">Number of bytes between position vectors.</span></span> <span data-ttu-id="9cb8b-116">Use [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)ou [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) para obter o stride do vértice.</span><span class="sxs-lookup"><span data-stu-id="9cb8b-116">Use [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md), or [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) to get the vertex stride.</span></span>

</dd> <dt>

<span data-ttu-id="9cb8b-117">*pCenter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9cb8b-117">*pCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb8b-118">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="9cb8b-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9cb8b-119">Estrutura [**D3DXVECTOR3**](d3dxvector3.md) , definindo o centro de coordenadas da esfera delimitadora retornada.</span><span class="sxs-lookup"><span data-stu-id="9cb8b-119">[**D3DXVECTOR3**](d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="9cb8b-120">*pRadius* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9cb8b-120">*pRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb8b-121">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9cb8b-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9cb8b-122">Raio da esfera delimitadora retornada.</span><span class="sxs-lookup"><span data-stu-id="9cb8b-122">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cb8b-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9cb8b-123">Return value</span></span>

<span data-ttu-id="9cb8b-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9cb8b-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9cb8b-125">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9cb8b-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9cb8b-126">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9cb8b-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cb8b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cb8b-127">Requirements</span></span>



| <span data-ttu-id="9cb8b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cb8b-128">Requirement</span></span> | <span data-ttu-id="9cb8b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="9cb8b-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cb8b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cb8b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="9cb8b-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cb8b-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9cb8b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9cb8b-132">Library</span></span><br/> | <dl> <span data-ttu-id="9cb8b-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cb8b-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9cb8b-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9cb8b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cb8b-135">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="9cb8b-135">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
