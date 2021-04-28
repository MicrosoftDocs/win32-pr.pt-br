---
description: Função D3DXSHPRTCompSuperCluster – usada com resultados compactados da versão de vértice do simulador de transferência radiante (PRT) precomputado.
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: Função D3DXSHPRTCompSuperCluster (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c22c8a3a14fd8af3e9104889b421068c7ff1457
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117854"
---
# <a name="d3dxshprtcompsupercluster-function"></a><span data-ttu-id="c28cc-103">Função D3DXSHPRTCompSuperCluster</span><span class="sxs-lookup"><span data-stu-id="c28cc-103">D3DXSHPRTCompSuperCluster function</span></span>

<span data-ttu-id="c28cc-104">Usado com resultados compactados da versão de vértice do simulador de transferência radiante (PRT) de computação.</span><span class="sxs-lookup"><span data-stu-id="c28cc-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="c28cc-105">Gera "superclusters", que são grupos de clusters que podem ser desenhados na mesma chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="c28cc-105">Generates "superclusters," which are groups of clusters that can be drawn in the same draw call.</span></span> <span data-ttu-id="c28cc-106">Um algoritmo de ávido que minimiza o superempate é usado para agrupar os clusters.</span><span class="sxs-lookup"><span data-stu-id="c28cc-106">A greedy algorithm that minimizes overdraw is used to group the clusters.</span></span>

## <a name="syntax"></a><span data-ttu-id="c28cc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c28cc-107">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a><span data-ttu-id="c28cc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c28cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c28cc-109">*pClusterIDs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c28cc-109">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c28cc-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c28cc-110">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c28cc-111">Ponteiro para as IDs de cluster NumVerts (extraídas de um buffer compactado).</span><span class="sxs-lookup"><span data-stu-id="c28cc-111">Pointer to a NumVerts cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="c28cc-112">*pScene* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c28cc-112">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c28cc-113">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="c28cc-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="c28cc-114">Ponteiro para uma malha que representa a cena composta passada para o simulador.</span><span class="sxs-lookup"><span data-stu-id="c28cc-114">Pointer to a mesh that represents composite scene passed to the simulator.</span></span> <span data-ttu-id="c28cc-115">Consulte [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="c28cc-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="c28cc-116">*MaxNumClusters* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c28cc-116">*MaxNumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c28cc-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c28cc-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c28cc-118">Número máximo de clusters alocados por super cluster.</span><span class="sxs-lookup"><span data-stu-id="c28cc-118">Maximum number of clusters allocated per super cluster.</span></span>

</dd> <dt>

<span data-ttu-id="c28cc-119">*NumClusters* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c28cc-119">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c28cc-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c28cc-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c28cc-121">Número de clusters computados no simulador.</span><span class="sxs-lookup"><span data-stu-id="c28cc-121">Number of clusters computed in the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="c28cc-122">*pSClusterIDs* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c28cc-122">*pSClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c28cc-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c28cc-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c28cc-124">Ponteiro para uma matriz de comprimento *NumClusters*.</span><span class="sxs-lookup"><span data-stu-id="c28cc-124">Pointer to an array of length *NumClusters*.</span></span> <span data-ttu-id="c28cc-125">Contém o índice do super cluster ao qual o cluster correspondente foi atribuído.</span><span class="sxs-lookup"><span data-stu-id="c28cc-125">Contains the index of the super cluster to which the corresponding cluster was assigned.</span></span>

</dd> <dt>

<span data-ttu-id="c28cc-126">*pNumSCs* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c28cc-126">*pNumSCs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c28cc-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c28cc-127">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c28cc-128">Número de superclusters alocados.</span><span class="sxs-lookup"><span data-stu-id="c28cc-128">Number of super clusters allocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c28cc-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c28cc-129">Return value</span></span>

<span data-ttu-id="c28cc-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c28cc-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c28cc-131">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c28cc-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c28cc-132">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c28cc-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c28cc-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c28cc-133">Requirements</span></span>



| <span data-ttu-id="c28cc-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c28cc-134">Requirement</span></span> | <span data-ttu-id="c28cc-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c28cc-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c28cc-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c28cc-136">Header</span></span><br/>  | <dl> <span data-ttu-id="c28cc-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c28cc-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c28cc-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c28cc-138">Library</span></span><br/> | <dl> <span data-ttu-id="c28cc-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c28cc-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c28cc-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c28cc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c28cc-141">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="c28cc-141">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
