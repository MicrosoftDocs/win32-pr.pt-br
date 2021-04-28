---
description: Função D3DXSHPRTCompSplitMeshSC – usada com resultados compactados da versão de vértice do simulador de transferência radiante (PRT) precomputado.
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Função D3DXSHPRTCompSplitMeshSC (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e51a86ec9b12992d49364d3a7c614751dacafac3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093894"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a><span data-ttu-id="0cce8-103">Função D3DXSHPRTCompSplitMeshSC</span><span class="sxs-lookup"><span data-stu-id="0cce8-103">D3DXSHPRTCompSplitMeshSC function</span></span>

<span data-ttu-id="0cce8-104">Usado com resultados compactados da versão de vértice do simulador de transferência radiante (PRT) de computação.</span><span class="sxs-lookup"><span data-stu-id="0cce8-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="0cce8-105">Depois que [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) tiver sido chamado, essa função poderá ser usada para dividir a malha em um grupo de faces/vértices por supercluster.</span><span class="sxs-lookup"><span data-stu-id="0cce8-105">After [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) has been called, this function can be used to split the mesh into a group of faces/vertices per super cluster.</span></span> <span data-ttu-id="0cce8-106">Cada super cluster contém todas as faces que contêm qualquer vértice classificado em um de seus clusters.</span><span class="sxs-lookup"><span data-stu-id="0cce8-106">Each super cluster contains all of the faces that contain any vertex classified in one of its clusters.</span></span> <span data-ttu-id="0cce8-107">Todos os vértices conectados a esse conjunto de faces também estão incluídos na matriz retornada ppVertStatus indicando se o vértice pertence ou não ao Super cluster.</span><span class="sxs-lookup"><span data-stu-id="0cce8-107">All of the vertices connected to this set of faces are also included with the returned array ppVertStatus indicating whether or not the vertex belongs to the super cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cce8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cce8-108">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a><span data-ttu-id="0cce8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cce8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cce8-110">*pClusterIDs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-110">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cce8-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0cce8-112">*NumVertices* IDs de cluster (extraídas de um buffer compactado).</span><span class="sxs-lookup"><span data-stu-id="0cce8-112">*NumVertices* cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-113">*NumVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-113">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cce8-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cce8-115">Número de vértices na malha original.</span><span class="sxs-lookup"><span data-stu-id="0cce8-115">Number of vertices in original mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-116">*NumCs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-116">*NumCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cce8-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cce8-118">Número de clusters (parâmetro de entrada para compactação).</span><span class="sxs-lookup"><span data-stu-id="0cce8-118">Number of clusters (input parameter to compression.)</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-119">*pSClusterIDs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-119">*pSClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cce8-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0cce8-121">Matriz de tamanho *NumCs* que conterá as IDs de supercluster.</span><span class="sxs-lookup"><span data-stu-id="0cce8-121">Array of size *NumCs* that will contain super cluster IDs.</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-122">*NumSCs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-122">*NumSCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cce8-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cce8-124">Número de superclusters alocados em [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span><span class="sxs-lookup"><span data-stu-id="0cce8-124">Number of super clusters allocated in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-125">*pInputIB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-125">*pInputIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-126">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cce8-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cce8-127">Buffer de índice bruto para malha.</span><span class="sxs-lookup"><span data-stu-id="0cce8-127">Raw index buffer for mesh.</span></span> <span data-ttu-id="0cce8-128">O formato depende de *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="0cce8-128">The format depends on *InputIBIs32Bit*.</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-129">*InputIBIs32Bit* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-129">*InputIBIs32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-130">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cce8-130">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cce8-131">Se for **true**, o buffer de índice será definido como 32 bit; caso contrário, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0cce8-131">If **TRUE**, the index buffer is set to 32 bit; otherwise, 16 bit.</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-132">*NumFaces* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-132">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-133">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cce8-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cce8-134">Número de rostos na malha original (*pInputIB* é 3 vezes esse comprimento.)</span><span class="sxs-lookup"><span data-stu-id="0cce8-134">Number of faces in the original mesh (*pInputIB* is 3 times this length.)</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-135">*ppIBData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-135">*ppIBData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cce8-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0cce8-137">Buffer de índice bruto que conterá as faces divididas resultantes.</span><span class="sxs-lookup"><span data-stu-id="0cce8-137">Raw index buffer that will contain the resulting split faces.</span></span> <span data-ttu-id="0cce8-138">Formato determinado por *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="0cce8-138">Format determined by *InputIBIs32Bit*.</span></span> <span data-ttu-id="0cce8-139">Alocada por função.</span><span class="sxs-lookup"><span data-stu-id="0cce8-139">Allocated by function.</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-140">*pIBDataLength* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-140">*pIBDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-141">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cce8-141">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0cce8-142">Comprimento de *ppIBData*, atribuído na função.</span><span class="sxs-lookup"><span data-stu-id="0cce8-142">Length of *ppIBData*, assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-143">*OutputIBIs32Bit* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-143">*OutputIBIs32Bit* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-144">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cce8-144">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cce8-145">Se **for true**, alocará uma matriz de inteiros sem sinal; caso contrário, o aloca uma matriz curta não assinada.</span><span class="sxs-lookup"><span data-stu-id="0cce8-145">If **TRUE**, allocates an unsigned integer array; otherwise, allocates an unsigned short array.</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-146">*ppFaceRemap* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-146">*ppFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-147">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cce8-147">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0cce8-148">Mapeamento de cada face em *ppIBData* para faces originais.</span><span class="sxs-lookup"><span data-stu-id="0cce8-148">Mapping of each face in *ppIBData* to original faces.</span></span> <span data-ttu-id="0cce8-149">O comprimento é \* *pIBDataLength*/3.</span><span class="sxs-lookup"><span data-stu-id="0cce8-149">Length is \**pIBDataLength*/3.</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-150">*ppVertData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-150">*ppVertData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-151">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cce8-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0cce8-152">Nova estrutura de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="0cce8-152">New vertex data structure.</span></span> <span data-ttu-id="0cce8-153">Tamanho de *pVertDataLength*.</span><span class="sxs-lookup"><span data-stu-id="0cce8-153">Size of *pVertDataLength*.</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-154">*pVertDataLength* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-154">*pVertDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-155">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cce8-155">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0cce8-156">Número de novos vértices na malha dividida.</span><span class="sxs-lookup"><span data-stu-id="0cce8-156">Number of new vertices in split mesh.</span></span> <span data-ttu-id="0cce8-157">Atribuído na função.</span><span class="sxs-lookup"><span data-stu-id="0cce8-157">Assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-158">*pSCClusterList* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-158">*pSCClusterList* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-159">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cce8-159">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0cce8-160">Matriz de comprimento *NumCs* quais índices *PSCData* (campos *pClusterIDs* \* ) para cada supercluster, contém clusters classificados por supercluster.</span><span class="sxs-lookup"><span data-stu-id="0cce8-160">Array of length *NumCs* which *pSCData* indexes into (*pClusterIDs*\* fields) for each supercluster, contains clusters sorted by supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="0cce8-161">*pSCData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0cce8-161">*pSCData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cce8-162">Tipo: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cce8-162">Type: **[**D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span></span>

<span data-ttu-id="0cce8-163">Estrutura por supercluster.</span><span class="sxs-lookup"><span data-stu-id="0cce8-163">Structure per super cluster.</span></span> <span data-ttu-id="0cce8-164">Contém índices em *ppIBData*, *pSCClusterList* e *ppVertData*.</span><span class="sxs-lookup"><span data-stu-id="0cce8-164">Contains indices into *ppIBData*, *pSCClusterList*, and *ppVertData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cce8-165">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0cce8-165">Return value</span></span>

<span data-ttu-id="0cce8-166">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0cce8-166">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0cce8-167">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0cce8-167">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0cce8-168">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0cce8-168">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cce8-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cce8-169">Requirements</span></span>



| <span data-ttu-id="0cce8-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cce8-170">Requirement</span></span> | <span data-ttu-id="0cce8-171">Valor</span><span class="sxs-lookup"><span data-stu-id="0cce8-171">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cce8-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0cce8-172">Header</span></span><br/>  | <dl> <span data-ttu-id="0cce8-173"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cce8-173"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0cce8-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cce8-174">Library</span></span><br/> | <dl> <span data-ttu-id="0cce8-175"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cce8-175"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0cce8-176">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0cce8-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cce8-177">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="0cce8-177">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
