---
description: Calcule os IMT por triângulo de dados por Texel. Essa função é semelhante a D3DXComputeIMTFromTexture, mas usa uma matriz float para passar os dados e pode calcular valores bidimensionais mais altos que 4.
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: Função D3DXComputeIMTFromPerTexelSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3db71fbc931f7bdb3e73c8d949a163607e66c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762217"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a><span data-ttu-id="a850f-104">Função D3DXComputeIMTFromPerTexelSignal</span><span class="sxs-lookup"><span data-stu-id="a850f-104">D3DXComputeIMTFromPerTexelSignal function</span></span>

<span data-ttu-id="a850f-105">Calcule os IMT por triângulo de dados por Texel.</span><span class="sxs-lookup"><span data-stu-id="a850f-105">Calculate per-triangle IMT's from per-texel data.</span></span> <span data-ttu-id="a850f-106">Essa função é semelhante a [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), mas usa uma matriz float para passar os dados e pode calcular valores bidimensionais mais altos que 4.</span><span class="sxs-lookup"><span data-stu-id="a850f-106">This function is similar to [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), but it uses a float array to pass in the data, and it can calculate higher dimensional values than 4.</span></span>

## <a name="syntax"></a><span data-ttu-id="a850f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a850f-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="a850f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a850f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a850f-109">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a850f-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a850f-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a850f-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="a850f-111">Um ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o IMT.</span><span class="sxs-lookup"><span data-stu-id="a850f-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="a850f-112">*dwTextureIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a850f-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a850f-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a850f-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a850f-114">Índice de coordenadas de textura baseado em zero que identifica o conjunto de coordenadas de textura a ser usado.</span><span class="sxs-lookup"><span data-stu-id="a850f-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="a850f-115">*pfTexelSignal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a850f-115">*pfTexelSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a850f-116">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a850f-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a850f-117">Um ponteiro para uma matriz de texels de entrada da qual IMT será computado.</span><span class="sxs-lookup"><span data-stu-id="a850f-117">A pointer to an array of input texels from which IMT will be computed.</span></span> <span data-ttu-id="a850f-118">O tamanho da matriz é uWidth \* uHeight \* uComponents.</span><span class="sxs-lookup"><span data-stu-id="a850f-118">The array size is uWidth\*uHeight\*uComponents.</span></span>

</dd> <dt>

<span data-ttu-id="a850f-119">*uWidth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a850f-119">*uWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a850f-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a850f-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a850f-121">Largura da textura em pixels.</span><span class="sxs-lookup"><span data-stu-id="a850f-121">Texture width in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a850f-122">*uHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a850f-122">*uHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a850f-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a850f-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a850f-124">Altura da textura em pixels.</span><span class="sxs-lookup"><span data-stu-id="a850f-124">Texture height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a850f-125">*uSignalDimension* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a850f-125">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a850f-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a850f-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a850f-127">O número de floats por componente em cada elemento da matriz de sinais.</span><span class="sxs-lookup"><span data-stu-id="a850f-127">The number of floats per-component in each element of the signal array.</span></span>

</dd> <dt>

<span data-ttu-id="a850f-128">*uComponents* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a850f-128">*uComponents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a850f-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a850f-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a850f-130">O número de componentes em cada Texel.</span><span class="sxs-lookup"><span data-stu-id="a850f-130">The number of components in each texel.</span></span>

</dd> <dt>

<span data-ttu-id="a850f-131">*dwOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a850f-131">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a850f-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a850f-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a850f-133">Opções de quebra automática de textura.</span><span class="sxs-lookup"><span data-stu-id="a850f-133">Texture wrap options.</span></span> <span data-ttu-id="a850f-134">Essa é uma combinação de um ou mais [**sinalizadores D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a850f-134">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a850f-135">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="a850f-135">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="a850f-136">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="a850f-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="a850f-137">Um ponteiro para uma função de retorno de chamada para monitorar o progresso da computação IMT.</span><span class="sxs-lookup"><span data-stu-id="a850f-137">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="a850f-138">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="a850f-138">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="a850f-139">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a850f-139">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a850f-140">Um ponteiro para uma variável definida pelo usuário que é passada para a função de retorno de chamada de status.</span><span class="sxs-lookup"><span data-stu-id="a850f-140">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="a850f-141">Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a850f-141">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="a850f-142">*ppIMTData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a850f-142">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a850f-143">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a850f-143">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a850f-144">Um ponteiro para o buffer (consulte [**ID3DXBuffer**](id3dxbuffer.md)) que contém a matriz IMT retornada.</span><span class="sxs-lookup"><span data-stu-id="a850f-144">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="a850f-145">Essa matriz pode ser fornecida como entrada para as [funções D3DX UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) para priorizar a alocação de espaço de textura na parametrização de textura.</span><span class="sxs-lookup"><span data-stu-id="a850f-145">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a850f-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a850f-146">Return value</span></span>

<span data-ttu-id="a850f-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a850f-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a850f-148">Se a função for realizada com sucesso, o valor de retorno será D3D \_ OK; caso contrário, o valor será D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a850f-148">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a850f-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a850f-149">Requirements</span></span>



| <span data-ttu-id="a850f-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="a850f-150">Requirement</span></span> | <span data-ttu-id="a850f-151">Valor</span><span class="sxs-lookup"><span data-stu-id="a850f-151">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a850f-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a850f-152">Header</span></span><br/>  | <dl> <span data-ttu-id="a850f-153"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a850f-153"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a850f-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a850f-154">Library</span></span><br/> | <dl> <span data-ttu-id="a850f-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a850f-155"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a850f-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="a850f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a850f-157">Funções UVAtlas</span><span class="sxs-lookup"><span data-stu-id="a850f-157">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="a850f-158">Usando o UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a850f-158">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
