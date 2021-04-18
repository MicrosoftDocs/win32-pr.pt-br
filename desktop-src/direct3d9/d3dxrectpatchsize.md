---
description: Obtém o tamanho do patch do retângulo.
ms.assetid: d25373ef-789d-4515-83da-7049f040c9a4
title: Função D3DXRectPatchSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRectPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5770e05493164db9da75fb38fa1e41594bfae8f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760423"
---
# <a name="d3dxrectpatchsize-function"></a><span data-ttu-id="b4440-103">Função D3DXRectPatchSize</span><span class="sxs-lookup"><span data-stu-id="b4440-103">D3DXRectPatchSize function</span></span>

<span data-ttu-id="b4440-104">Obtém o tamanho do patch do retângulo.</span><span class="sxs-lookup"><span data-stu-id="b4440-104">Gets the size of the rectangle patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4440-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4440-105">Syntax</span></span>


```C++
HRESULT D3DXRectPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pwdVertices
);
```



## <a name="parameters"></a><span data-ttu-id="b4440-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4440-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4440-107">*pfNumSegs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4440-107">*pfNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4440-108">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b4440-108">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4440-109">Número de segmentos por borda para incluí.</span><span class="sxs-lookup"><span data-stu-id="b4440-109">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="b4440-110">*pdwTriangles* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b4440-110">*pdwTriangles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4440-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4440-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4440-112">Ponteiro para um DWORD que contém o número de triângulos no patch.</span><span class="sxs-lookup"><span data-stu-id="b4440-112">Pointer to a DWORD that contains the number of triangles in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="b4440-113">*pwdVertices* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b4440-113">*pwdVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4440-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4440-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4440-115">Ponteiro para um DWORD que contém o número de vértices no patch.</span><span class="sxs-lookup"><span data-stu-id="b4440-115">Pointer to a DWORD that contains the number of vertices in the patch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4440-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4440-116">Return value</span></span>

<span data-ttu-id="b4440-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4440-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4440-118">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b4440-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b4440-119">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b4440-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4440-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4440-120">Requirements</span></span>



| <span data-ttu-id="b4440-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4440-121">Requirement</span></span> | <span data-ttu-id="b4440-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b4440-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4440-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4440-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b4440-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4440-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b4440-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4440-125">Library</span></span><br/> | <dl> <span data-ttu-id="b4440-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4440-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b4440-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4440-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4440-128">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="b4440-128">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="b4440-129">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="b4440-129">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
