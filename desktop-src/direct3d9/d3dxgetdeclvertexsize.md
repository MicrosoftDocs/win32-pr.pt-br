---
description: Retorna o tamanho de um vértice da declaração de vértice.
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: Função D3DXGetDeclVertexSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c962064faa61dc7045b0111c5efbf1d1bea9fd40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798528"
---
# <a name="d3dxgetdeclvertexsize-function"></a><span data-ttu-id="647d8-103">Função D3DXGetDeclVertexSize</span><span class="sxs-lookup"><span data-stu-id="647d8-103">D3DXGetDeclVertexSize function</span></span>

<span data-ttu-id="647d8-104">Retorna o tamanho de um vértice da declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="647d8-104">Returns the size of a vertex from the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="647d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="647d8-105">Syntax</span></span>


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a><span data-ttu-id="647d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="647d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="647d8-107">*pDecl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="647d8-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="647d8-108">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="647d8-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="647d8-109">Um ponteiro para a declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="647d8-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="647d8-110">Consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="647d8-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="647d8-111">*Fluxo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="647d8-111">*Stream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="647d8-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="647d8-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="647d8-113">O índice de fluxo com base em zero.</span><span class="sxs-lookup"><span data-stu-id="647d8-113">The zero-based stream index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="647d8-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="647d8-114">Return value</span></span>

<span data-ttu-id="647d8-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="647d8-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="647d8-116">O tamanho da declaração de vértice, em bytes.</span><span class="sxs-lookup"><span data-stu-id="647d8-116">The vertex declaration size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="647d8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="647d8-117">Requirements</span></span>



| <span data-ttu-id="647d8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="647d8-118">Requirement</span></span> | <span data-ttu-id="647d8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="647d8-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="647d8-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="647d8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="647d8-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="647d8-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="647d8-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="647d8-122">Library</span></span><br/> | <dl> <span data-ttu-id="647d8-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="647d8-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="647d8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="647d8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="647d8-125">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="647d8-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
