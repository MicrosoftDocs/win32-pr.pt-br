---
description: Gera um remapeamento facial otimizado para uma lista de triângulos.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: Função D3DXOptimizeFaces (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781313"
---
# <a name="d3dxoptimizefaces-function"></a><span data-ttu-id="75ea8-103">Função D3DXOptimizeFaces</span><span class="sxs-lookup"><span data-stu-id="75ea8-103">D3DXOptimizeFaces function</span></span>

<span data-ttu-id="75ea8-104">Gera um remapeamento facial otimizado para uma lista de triângulos.</span><span class="sxs-lookup"><span data-stu-id="75ea8-104">Generates an optimized face remapping for a triangle list.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ea8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75ea8-105">Syntax</span></span>


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a><span data-ttu-id="75ea8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75ea8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ea8-107">*pIndices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75ea8-107">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ea8-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75ea8-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75ea8-109">Ponteiro para índices da lista de triângulos a serem usados para ordenar vértices.</span><span class="sxs-lookup"><span data-stu-id="75ea8-109">Pointer to triangle list indices to use for ordering vertices.</span></span>

</dd> <dt>

<span data-ttu-id="75ea8-110">*NumFaces* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75ea8-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ea8-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75ea8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75ea8-112">Número de rostos na lista de triângulos.</span><span class="sxs-lookup"><span data-stu-id="75ea8-112">Number of faces in the triangle list.</span></span> <span data-ttu-id="75ea8-113">Para malhas de 16 bits, isso é limitado a 2 ^ 16-1 (65535) ou menos faces.</span><span class="sxs-lookup"><span data-stu-id="75ea8-113">For 16-bit meshes, this is limited to 2^16 - 1 (65535) or fewer faces.</span></span>

</dd> <dt>

<span data-ttu-id="75ea8-114">*NumVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75ea8-114">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ea8-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75ea8-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75ea8-116">Número de vértices referenciados pela lista de triângulos.</span><span class="sxs-lookup"><span data-stu-id="75ea8-116">Number of vertices referenced by the triangle list.</span></span>

</dd> <dt>

<span data-ttu-id="75ea8-117">*Indices32Bit* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75ea8-117">*Indices32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ea8-118">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75ea8-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75ea8-119">Sinalizador que indica o tipo de índice: **verdadeiro** se os índices forem de 32 bits (mais de 65535 índices), **falso** se os índices forem de 16 bits (65535 ou menos índices).</span><span class="sxs-lookup"><span data-stu-id="75ea8-119">Flag indicating index type: **TRUE** if indices are 32-bit (more than 65535 indices), **FALSE** if indices are 16-bit (65535 or fewer indices).</span></span>

</dd> <dt>

<span data-ttu-id="75ea8-120">*pFaceRemap* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="75ea8-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75ea8-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="75ea8-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="75ea8-122">Ponteiro para a face de malha original que foi dividida para gerar a face atual.</span><span class="sxs-lookup"><span data-stu-id="75ea8-122">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ea8-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75ea8-123">Return value</span></span>

<span data-ttu-id="75ea8-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75ea8-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75ea8-125">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75ea8-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="75ea8-126">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="75ea8-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="75ea8-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="75ea8-127">Remarks</span></span>

<span data-ttu-id="75ea8-128">O procedimento de otimização da função é funcionalmente equivalente a chamar [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) com o \_ sinalizador D3DXMESHOPT DEVICEINDEPENDENT, mas essa função faz uso mais eficiente de caches de vértice.</span><span class="sxs-lookup"><span data-stu-id="75ea8-128">This function's optimization procedure is functionally equivalent to calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) with the D3DXMESHOPT\_DEVICEINDEPENDENT flag, but this function makes more efficient use of vertex caches.</span></span>

## <a name="requirements"></a><span data-ttu-id="75ea8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75ea8-129">Requirements</span></span>



| <span data-ttu-id="75ea8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ea8-130">Requirement</span></span> | <span data-ttu-id="75ea8-131">Valor</span><span class="sxs-lookup"><span data-stu-id="75ea8-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75ea8-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75ea8-132">Header</span></span><br/>  | <dl> <span data-ttu-id="75ea8-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="75ea8-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="75ea8-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75ea8-134">Library</span></span><br/> | <dl> <span data-ttu-id="75ea8-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75ea8-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75ea8-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="75ea8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ea8-137">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="75ea8-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
