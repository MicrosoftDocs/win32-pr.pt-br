---
description: Calcule IMT por triângulo de de dados por vértice. Essa função permite que você calcule o IMT com base em qualquer valor em uma malha (cor, normal, etc.).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: Função D3DXComputeIMTFromPerVertexSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815487"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a><span data-ttu-id="cc316-104">Função D3DXComputeIMTFromPerVertexSignal</span><span class="sxs-lookup"><span data-stu-id="cc316-104">D3DXComputeIMTFromPerVertexSignal function</span></span>

<span data-ttu-id="cc316-105">Calcule IMT por triângulo de de dados por vértice.</span><span class="sxs-lookup"><span data-stu-id="cc316-105">Calculate per-triangle IMT's from from per-vertex data.</span></span> <span data-ttu-id="cc316-106">Essa função permite que você calcule o IMT com base em qualquer valor em uma malha (cor, normal, etc.).</span><span class="sxs-lookup"><span data-stu-id="cc316-106">This function allows you to calculate the IMT based off of any value in a mesh (color, normal, etc).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc316-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc316-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="cc316-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc316-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc316-109">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc316-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc316-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="cc316-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="cc316-111">Um ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o IMT.</span><span class="sxs-lookup"><span data-stu-id="cc316-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="cc316-112">*pfVertexSignal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc316-112">*pfVertexSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc316-113">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc316-113">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cc316-114">Um ponteiro para uma matriz de dados por vértice do qual IMT será computado.</span><span class="sxs-lookup"><span data-stu-id="cc316-114">A pointer to an array of per-vertex data from which IMT will be computed.</span></span> <span data-ttu-id="cc316-115">O tamanho da matriz é uSignalStride \* v, em que v é o número de vértices na malha.</span><span class="sxs-lookup"><span data-stu-id="cc316-115">The array size is uSignalStride \* v, where v is the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cc316-116">*uSignalDimension* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc316-116">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc316-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc316-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc316-118">O número de floats por vértice.</span><span class="sxs-lookup"><span data-stu-id="cc316-118">The number of floats per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="cc316-119">*uSignalStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc316-119">*uSignalStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc316-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc316-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc316-121">O número de bytes por vértice na matriz.</span><span class="sxs-lookup"><span data-stu-id="cc316-121">The number of bytes per vertex in the array.</span></span> <span data-ttu-id="cc316-122">Deve ser um múltiplo de sizeof (float)</span><span class="sxs-lookup"><span data-stu-id="cc316-122">This must be a multiple of sizeof(float)</span></span>

</dd> <dt>

<span data-ttu-id="cc316-123">*dwOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc316-123">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc316-124">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc316-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc316-125">Opções de quebra automática de textura.</span><span class="sxs-lookup"><span data-stu-id="cc316-125">Texture wrap options.</span></span> <span data-ttu-id="cc316-126">Essa é uma combinação de um ou mais [**sinalizadores D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="cc316-126">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc316-127">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="cc316-127">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="cc316-128">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="cc316-128">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="cc316-129">Um ponteiro para uma função de retorno de chamada para monitorar o progresso da computação IMT.</span><span class="sxs-lookup"><span data-stu-id="cc316-129">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="cc316-130">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="cc316-130">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="cc316-131">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc316-131">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc316-132">Um ponteiro para uma variável definida pelo usuário que é passada para a função de retorno de chamada de status.</span><span class="sxs-lookup"><span data-stu-id="cc316-132">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="cc316-133">Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="cc316-133">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="cc316-134">*ppIMTData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cc316-134">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc316-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc316-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cc316-136">Um ponteiro para o buffer (consulte [**ID3DXBuffer**](id3dxbuffer.md)) que contém a matriz IMT retornada.</span><span class="sxs-lookup"><span data-stu-id="cc316-136">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="cc316-137">Essa matriz pode ser fornecida como entrada para as [funções D3DX UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) para priorizar a alocação de espaço de textura na parametrização de textura.</span><span class="sxs-lookup"><span data-stu-id="cc316-137">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc316-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc316-138">Return value</span></span>

<span data-ttu-id="cc316-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc316-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc316-140">Se a função for realizada com sucesso, o valor de retorno será D3D \_ OK; caso contrário, o valor será D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cc316-140">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc316-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc316-141">Requirements</span></span>



| <span data-ttu-id="cc316-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc316-142">Requirement</span></span> | <span data-ttu-id="cc316-143">Valor</span><span class="sxs-lookup"><span data-stu-id="cc316-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc316-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc316-144">Header</span></span><br/>  | <dl> <span data-ttu-id="cc316-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc316-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cc316-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc316-146">Library</span></span><br/> | <dl> <span data-ttu-id="cc316-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc316-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cc316-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc316-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc316-149">Funções UVAtlas</span><span class="sxs-lookup"><span data-stu-id="cc316-149">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="cc316-150">Usando o UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cc316-150">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
