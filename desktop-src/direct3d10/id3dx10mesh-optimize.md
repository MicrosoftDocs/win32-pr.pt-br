---
description: Gera uma nova malha com faces e vértices reordenados para otimizar o desempenho do desenho.
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'Método ID3DX10Mesh:: Optimize (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e3c416b28cefe1a3f7fb487567afac4c99057478
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298704"
---
# <a name="id3dx10meshoptimize-method"></a><span data-ttu-id="9ab46-103">Método ID3DX10Mesh:: Optimize</span><span class="sxs-lookup"><span data-stu-id="9ab46-103">ID3DX10Mesh::Optimize method</span></span>

<span data-ttu-id="9ab46-104">Gera uma nova malha com faces e vértices reordenados para otimizar o desempenho do desenho.</span><span class="sxs-lookup"><span data-stu-id="9ab46-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ab46-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ab46-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="9ab46-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ab46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab46-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9ab46-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab46-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ab46-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ab46-109">Especifica o tipo de otimização a ser executado.</span><span class="sxs-lookup"><span data-stu-id="9ab46-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="9ab46-110">Esse parâmetro pode ser definido como uma combinação de um ou mais sinalizadores de D3DXMESHOPT e D3DXMESH (exceto D3DXMESH \_ 32 bits, D3DXMESH \_ IB \_ WriteOnly e D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="9ab46-110">This parameter can be set to a combination of one or more flags from D3DXMESHOPT and D3DXMESH (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="9ab46-111">*pFaceRemap* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ab46-111">*pFaceRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab46-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ab46-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9ab46-113">Uma matriz de UINTs, uma por face, que identifica a face de malha original que corresponde a cada face na malha otimizada.</span><span class="sxs-lookup"><span data-stu-id="9ab46-113">An array of UINTs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="9ab46-114">Se o valor fornecido para esse argumento for **nulo**, os dados de remapeamento facial não serão retornados.</span><span class="sxs-lookup"><span data-stu-id="9ab46-114">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="9ab46-115">*ppVertexRemap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9ab46-115">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab46-116">Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="9ab46-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="9ab46-117">Endereço de um ponteiro para uma [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), que contém um DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos.</span><span class="sxs-lookup"><span data-stu-id="9ab46-117">Address of a pointer to an [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="9ab46-118">Esse remapeamento será útil se você precisar alterar dados externos com base no novo mapeamento de vértice.</span><span class="sxs-lookup"><span data-stu-id="9ab46-118">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ab46-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ab46-119">Return value</span></span>

<span data-ttu-id="9ab46-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9ab46-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9ab46-121">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9ab46-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ab46-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ab46-122">Remarks</span></span>

<span data-ttu-id="9ab46-123">Esse método gera uma nova malha.</span><span class="sxs-lookup"><span data-stu-id="9ab46-123">This method generates a new mesh.</span></span> <span data-ttu-id="9ab46-124">Antes de executar Optimize, um aplicativo deve gerar um buffer de adjacência chamando [**ID3DX10Mesh:: GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span><span class="sxs-lookup"><span data-stu-id="9ab46-124">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span></span> <span data-ttu-id="9ab46-125">O buffer de adjacência contém dados de adjacência, como uma lista de bordas e as faces que são adjacentes entre si.</span><span class="sxs-lookup"><span data-stu-id="9ab46-125">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="9ab46-126">Esse método é muito semelhante ao método [**ID3DX10Mesh:: CloneMesh**](id3dx10mesh-clonemesh.md) , exceto pelo fato de que ele pode executar a otimização ao gerar o novo clone da malha.</span><span class="sxs-lookup"><span data-stu-id="9ab46-126">This method is very similar to the [**ID3DX10Mesh::CloneMesh**](id3dx10mesh-clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="9ab46-127">A malha de saída herda todos os parâmetros de criação da malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="9ab46-127">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab46-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ab46-128">Requirements</span></span>



| <span data-ttu-id="9ab46-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ab46-129">Requirement</span></span> | <span data-ttu-id="9ab46-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9ab46-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab46-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ab46-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9ab46-132"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ab46-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ab46-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ab46-133">Library</span></span><br/> | <dl> <span data-ttu-id="9ab46-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ab46-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ab46-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ab46-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab46-136">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="9ab46-136">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="9ab46-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="9ab46-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
