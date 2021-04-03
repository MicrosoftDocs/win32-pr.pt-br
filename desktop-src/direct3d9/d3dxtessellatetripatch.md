---
description: Tessellates um patch de superfície de ordem superior triangular em uma malha de triângulo.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: Função D3DXTessellateTriPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61d5a426f9fe3331b85c4a881219319622283820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663995"
---
# <a name="d3dxtessellatetripatch-function"></a><span data-ttu-id="026a8-103">Função D3DXTessellateTriPatch</span><span class="sxs-lookup"><span data-stu-id="026a8-103">D3DXTessellateTriPatch function</span></span>

<span data-ttu-id="026a8-104">Tessellates um patch de superfície de ordem superior triangular em uma malha de triângulo.</span><span class="sxs-lookup"><span data-stu-id="026a8-104">Tessellates a triangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="026a8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="026a8-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="026a8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="026a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="026a8-107">*pVB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="026a8-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="026a8-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="026a8-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="026a8-109">O buffer de vértices que contém os dados do patch.</span><span class="sxs-lookup"><span data-stu-id="026a8-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="026a8-110">*pNumSegs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="026a8-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="026a8-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="026a8-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="026a8-112">Ponteiro para uma matriz de três valores de ponto flutuante que identificam o número de segmentos nos quais cada borda do patch de triângulo deve ser dividida quando mosaico.</span><span class="sxs-lookup"><span data-stu-id="026a8-112">Pointer to an array of three floating-point values that identify the number of segments into which each edge of the triangle patch should be divided when tessellated.</span></span> <span data-ttu-id="026a8-113">Consulte [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="026a8-113">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="026a8-114">*pInDecl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="026a8-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="026a8-115">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="026a8-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="026a8-116">Estrutura de declaração de vértice que define os dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="026a8-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="026a8-117">Consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="026a8-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="026a8-118">*pTriPatchInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="026a8-118">*pTriPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="026a8-119">Tipo: **const [**D3TRIPATCH \_ info**](d3dtripatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="026a8-119">Type: **const [**D3TRIPATCH\_INFO**](d3dtripatch-info.md)\***</span></span>

<span data-ttu-id="026a8-120">Descreve um patch de triângulo.</span><span class="sxs-lookup"><span data-stu-id="026a8-120">Describes a triangle patch.</span></span> <span data-ttu-id="026a8-121">Consulte [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="026a8-121">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="026a8-122">*pMesh* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="026a8-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="026a8-123">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="026a8-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="026a8-124">Ponteiro para a malha criada.</span><span class="sxs-lookup"><span data-stu-id="026a8-124">Pointer to the created mesh.</span></span> <span data-ttu-id="026a8-125">Consulte [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="026a8-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="026a8-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="026a8-126">Return value</span></span>

<span data-ttu-id="026a8-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="026a8-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="026a8-128">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="026a8-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="026a8-129">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="026a8-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="026a8-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="026a8-130">Remarks</span></span>

<span data-ttu-id="026a8-131">Use [**D3DXTriPatchSize**](d3dxtripatchsize.md) para obter o número de vértices de saída e os índices necessários para a função de mosaico.</span><span class="sxs-lookup"><span data-stu-id="026a8-131">Use [**D3DXTriPatchSize**](d3dxtripatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="026a8-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="026a8-132">Requirements</span></span>



| <span data-ttu-id="026a8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="026a8-133">Requirement</span></span> | <span data-ttu-id="026a8-134">Valor</span><span class="sxs-lookup"><span data-stu-id="026a8-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="026a8-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="026a8-135">Header</span></span><br/>  | <dl> <span data-ttu-id="026a8-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="026a8-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="026a8-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="026a8-137">Library</span></span><br/> | <dl> <span data-ttu-id="026a8-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="026a8-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="026a8-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="026a8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="026a8-140">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="026a8-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="026a8-141">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="026a8-141">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
