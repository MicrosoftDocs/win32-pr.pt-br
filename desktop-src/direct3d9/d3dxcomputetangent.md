---
description: Computa os vetores tangentes das coordenadas de textura dadas no estágio de textura. Fornecido para dar suporte a aplicativos herdados. Use D3DXComputeTangentFrameEx para obter resultados melhores.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: Função D3DXComputeTangent (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812289"
---
# <a name="d3dxcomputetangent-function"></a><span data-ttu-id="cd6a3-105">Função D3DXComputeTangent</span><span class="sxs-lookup"><span data-stu-id="cd6a3-105">D3DXComputeTangent function</span></span>

<span data-ttu-id="cd6a3-106">Computa os vetores tangentes das coordenadas de textura dadas no estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-106">Computes the tangent vectors for the texture coordinates given in the texture stage.</span></span> <span data-ttu-id="cd6a3-107">Fornecido para dar suporte a aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-107">Provided to support legacy applications.</span></span> <span data-ttu-id="cd6a3-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) para obter resultados melhores.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd6a3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd6a3-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="cd6a3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd6a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd6a3-111">*Malha* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd6a3-111">*Mesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6a3-112">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="cd6a3-113">Ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) que representa a malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represent the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cd6a3-114">*TexStageIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd6a3-114">*TexStageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6a3-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd6a3-116">Índice que representa o estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-116">Index that represents the texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="cd6a3-117">*TangentIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd6a3-117">*TangentIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6a3-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd6a3-119">Índice que fornece o índice de uso para os dados da tangente.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-119">Index that provides the usage index for the tangent data.</span></span> <span data-ttu-id="cd6a3-120">A declaração de vértice implica o uso; Esse índice modifica o uso com o índice de uso.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-120">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="cd6a3-121">Para obter mais informações sobre uma declaração de vértice, consulte [declaração de vértice (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="cd6a3-121">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd6a3-122">*BinormIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd6a3-122">*BinormIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6a3-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd6a3-124">Índice que fornece o índice de uso para os dados binormal.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-124">Index that provides the usage index for the binormal data.</span></span> <span data-ttu-id="cd6a3-125">A declaração de vértice implica o uso; Esse índice modifica o uso com o índice de uso.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-125">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="cd6a3-126">Para obter mais informações sobre uma declaração de vértice, consulte [declaração de vértice (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="cd6a3-126">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd6a3-127">*Encapsular* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd6a3-127">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6a3-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd6a3-129">Defina esse valor como 0 para sem quebra automática ou para 1 para quebra automática nas direções você e V.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-129">Set this value to 0 for no wrapping, or to 1 for wrapping in the U and V directions.</span></span>

</dd> <dt>

<span data-ttu-id="cd6a3-130">*pAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd6a3-130">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6a3-131">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd6a3-131">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cd6a3-132">Ponteiro para uma matriz de três DWORDs por face a ser preenchida com índices de face adjacentes.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-132">Pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="cd6a3-133">O número de bytes nessa matriz deve ser pelo menos (3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).</span><span class="sxs-lookup"><span data-stu-id="cd6a3-133">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd6a3-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd6a3-134">Return value</span></span>

<span data-ttu-id="cd6a3-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd6a3-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd6a3-136">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-136">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cd6a3-137">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd6a3-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd6a3-138">Remarks</span></span>

<span data-ttu-id="cd6a3-139">Se a declaração de vértice de malha especificar campos tangentes ou binormal, o **D3DXComputeTangent** atualizará todos os dados tangentes ou binormals fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-139">If the mesh vertex declaration specifies tangent or binormal fields, **D3DXComputeTangent** will update any user-supplied tangent or binormal data.</span></span> <span data-ttu-id="cd6a3-140">Como alternativa, defina TangentIndex como [D3DX como \_ padrão](other-d3dx-constants.md) para não atualizar os dados tangentes fornecidos pelo usuário ou defina BinormIndex como D3DX como \_ padrão para não atualizar os dados binormal fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-140">Alternatively, set TangentIndex to [D3DX\_DEFAULT](other-d3dx-constants.md) to not update the user-supplied tangent data, or set BinormIndex to D3DX\_DEFAULT to not update the user-supplied binormal data.</span></span> <span data-ttu-id="cd6a3-141">TexStageIndex não pode ser definido como D3DX \_ padrão.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-141">TexStageIndex cannot be set to D3DX\_DEFAULT.</span></span>

<span data-ttu-id="cd6a3-142">**D3DXComputeTangent** depende da declaração de vértice de malha que contém o campo binormal (BinormIndex), o campo tangente (TangentIndex) ou ambos.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-142">**D3DXComputeTangent** depends on the mesh vertex declaration containing either the binormal field (BinormIndex), the tangent field (TangentIndex), or both.</span></span> <span data-ttu-id="cd6a3-143">Se ambos estiverem ausentes, essa função falhará.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-143">If both are missing, this function will fail.</span></span>

<span data-ttu-id="cd6a3-144">Essa função simplesmente chama [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) com os seguintes parâmetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="cd6a3-144">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="cd6a3-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd6a3-145">Requirements</span></span>



| <span data-ttu-id="cd6a3-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd6a3-146">Requirement</span></span> | <span data-ttu-id="cd6a3-147">Valor</span><span class="sxs-lookup"><span data-stu-id="cd6a3-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6a3-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd6a3-148">Header</span></span><br/>  | <dl> <span data-ttu-id="cd6a3-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd6a3-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cd6a3-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd6a3-150">Library</span></span><br/> | <dl> <span data-ttu-id="cd6a3-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd6a3-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd6a3-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd6a3-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd6a3-153">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="cd6a3-153">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
