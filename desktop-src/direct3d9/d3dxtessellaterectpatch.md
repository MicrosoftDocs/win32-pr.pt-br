---
description: Tessellates um patch de superfície de ordem superior retangular em uma malha de triangulares.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: Função D3DXTessellateRectPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172981"
---
# <a name="d3dxtessellaterectpatch-function"></a><span data-ttu-id="554f3-103">Função D3DXTessellateRectPatch</span><span class="sxs-lookup"><span data-stu-id="554f3-103">D3DXTessellateRectPatch function</span></span>

<span data-ttu-id="554f3-104">Tessellates um patch de superfície de ordem superior retangular em uma malha de triangulares.</span><span class="sxs-lookup"><span data-stu-id="554f3-104">Tessellates a rectangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="554f3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="554f3-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="554f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="554f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="554f3-107">*pVB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="554f3-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="554f3-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="554f3-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="554f3-109">O buffer de vértices que contém os dados do patch.</span><span class="sxs-lookup"><span data-stu-id="554f3-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="554f3-110">*pNumSegs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="554f3-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="554f3-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="554f3-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="554f3-112">Ponteiro para uma matriz de quatro valores de ponto flutuante que identificam o número de segmentos nos quais cada borda do patch de retângulo deve ser dividida quando mosaico.</span><span class="sxs-lookup"><span data-stu-id="554f3-112">Pointer to an array of four floating-point values that identify the number of segments into which each edge of the rectangle patch should be divided when tessellated.</span></span> <span data-ttu-id="554f3-113">Consulte [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="554f3-113">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="554f3-114">*pInDecl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="554f3-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="554f3-115">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="554f3-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="554f3-116">Estrutura de declaração de vértice que define os dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="554f3-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="554f3-117">Consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="554f3-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="554f3-118">*pRectPatchInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="554f3-118">*pRectPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="554f3-119">Tipo: **const [**D3DRECTPATCH \_ info**](d3drectpatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="554f3-119">Type: **const [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md)\***</span></span>

<span data-ttu-id="554f3-120">Descreve um patch retangular.</span><span class="sxs-lookup"><span data-stu-id="554f3-120">Describes a rectangular patch.</span></span> <span data-ttu-id="554f3-121">Consulte [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="554f3-121">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="554f3-122">*pMesh* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="554f3-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="554f3-123">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="554f3-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="554f3-124">Ponteiro para a malha criada.</span><span class="sxs-lookup"><span data-stu-id="554f3-124">Pointer to the created mesh.</span></span> <span data-ttu-id="554f3-125">Consulte [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="554f3-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="554f3-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="554f3-126">Return value</span></span>

<span data-ttu-id="554f3-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="554f3-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="554f3-128">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="554f3-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="554f3-129">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="554f3-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="554f3-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="554f3-130">Remarks</span></span>

<span data-ttu-id="554f3-131">Use [**D3DXRectPatchSize**](d3dxrectpatchsize.md) para obter o número de vértices de saída e os índices necessários para a função de mosaico.</span><span class="sxs-lookup"><span data-stu-id="554f3-131">Use [**D3DXRectPatchSize**](d3dxrectpatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="554f3-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="554f3-132">Requirements</span></span>



| <span data-ttu-id="554f3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="554f3-133">Requirement</span></span> | <span data-ttu-id="554f3-134">Valor</span><span class="sxs-lookup"><span data-stu-id="554f3-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="554f3-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="554f3-135">Header</span></span><br/>  | <dl> <span data-ttu-id="554f3-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="554f3-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="554f3-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="554f3-137">Library</span></span><br/> | <dl> <span data-ttu-id="554f3-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="554f3-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="554f3-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="554f3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="554f3-140">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="554f3-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="554f3-141">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="554f3-141">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
