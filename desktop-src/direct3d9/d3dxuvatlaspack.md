---
description: Compactar dados de particionamento de malha em um Atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: Função D3DXUVAtlasPack (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31de326160120fe14a71841cb5f2d18e1c8d4e57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771395"
---
# <a name="d3dxuvatlaspack-function"></a><span data-ttu-id="1fc5c-103">Função D3DXUVAtlasPack</span><span class="sxs-lookup"><span data-stu-id="1fc5c-103">D3DXUVAtlasPack function</span></span>

<span data-ttu-id="1fc5c-104">Compactar dados de particionamento de malha em um Atlas.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-104">Pack mesh partitioning data into an atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc5c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fc5c-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a><span data-ttu-id="1fc5c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fc5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fc5c-107">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fc5c-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc5c-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="1fc5c-109">Ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o Atlas.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="1fc5c-110">No mínimo, a malha deve conter dados de posição e coordenadas de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="1fc5c-111">*dwWidth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fc5c-111">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc5c-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fc5c-113">Largura da textura.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-113">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="1fc5c-114">*dwHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fc5c-114">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc5c-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fc5c-116">Altura da textura.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-116">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="1fc5c-117">*fGutter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fc5c-117">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc5c-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fc5c-119">A distância mínima, em texels, entre dois gráficos no Atlas.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-119">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="1fc5c-120">A medianiz sempre é dimensionada pela largura; Portanto, se uma medianiz de 2,5 for usada em uma textura 512x512, a distância mínima entre dois gráficos será 2,5/512,0 texels.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-120">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="1fc5c-121">*dwTextureIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fc5c-121">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc5c-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fc5c-123">Índice de coordenadas de textura baseado em zero que identifica o conjunto de coordenadas de textura a ser usado.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-123">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="1fc5c-124">*pdwPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="1fc5c-124">*pdwPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="1fc5c-125">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1fc5c-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1fc5c-126">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="1fc5c-127">Ele deve ser derivado do ppPartitionResultAdjacency retornado de [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span><span class="sxs-lookup"><span data-stu-id="1fc5c-127">It should be derived from the ppPartitionResultAdjacency returned from [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span></span> <span data-ttu-id="1fc5c-128">Esse valor não pode ser **nulo**, pois o pacote precisa saber onde os gráficos foram cortados na etapa de partição para localizar as bordas de cada gráfico.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-128">This value cannot be **NULL**, because Pack needs to know where charts were cut in the partition step in order to find the edges of each chart.</span></span>

</dd> <dt>

<span data-ttu-id="1fc5c-129">*pCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fc5c-129">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc5c-130">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-130">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="1fc5c-131">Um ponteiro para uma função de retorno de chamada (consulte [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) que é útil para monitorar o progresso.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-131">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="1fc5c-132">*fCallbackFrequency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fc5c-132">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc5c-133">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fc5c-134">Especifique com que frequência o D3DX chamará o retorno de chamada; um valor padrão razoável é 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-134">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="1fc5c-135">*pUserContent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fc5c-135">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc5c-136">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-136">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fc5c-137">Um ponteiro void a ser passado de volta para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-137">A void pointer to be passed back to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="1fc5c-138">*dwOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fc5c-138">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc5c-139">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fc5c-140">Este parâmetro de opções está reservado no momento.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-140">This options parameter is currently reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1fc5c-141">*pFacePartitioning* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fc5c-141">*pFacePartitioning* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc5c-142">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-142">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="1fc5c-143">Um ponteiro para um [**ID3DXBuffer**](id3dxbuffer.md) que contém a matriz do particionamento de face final.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-143">A pointer to an [**ID3DXBuffer**](id3dxbuffer.md) containing the array of the final face-partitioning.</span></span> <span data-ttu-id="1fc5c-144">Cada elemento contém um DWORD por face.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-144">Each element contains one DWORD per face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fc5c-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fc5c-145">Return value</span></span>

<span data-ttu-id="1fc5c-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fc5c-147">Se a função for realizada com sucesso, o valor de retorno será D3D \_ OK; caso contrário, o valor será D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-147">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc5c-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc5c-148">Requirements</span></span>



| <span data-ttu-id="1fc5c-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc5c-149">Requirement</span></span> | <span data-ttu-id="1fc5c-150">Valor</span><span class="sxs-lookup"><span data-stu-id="1fc5c-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc5c-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fc5c-151">Header</span></span><br/>  | <dl> <span data-ttu-id="1fc5c-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fc5c-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1fc5c-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fc5c-153">Library</span></span><br/> | <dl> <span data-ttu-id="1fc5c-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fc5c-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1fc5c-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fc5c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc5c-156">Funções UVAtlas</span><span class="sxs-lookup"><span data-stu-id="1fc5c-156">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
