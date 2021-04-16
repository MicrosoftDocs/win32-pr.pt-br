---
description: Calcula o IMT por triângulo de um sinal especificado pelo aplicativo personalizado que varia na superfície da malha (geralmente com uma frequência maior do que os dados de vértice). O sinal é avaliado por meio de uma função de retorno de chamada especificada pelo usuário.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: Função D3DXComputeIMTFromSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 979304a350c226a9406e62896bb84492d8046e74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765028"
---
# <a name="d3dxcomputeimtfromsignal-function"></a><span data-ttu-id="b200f-104">Função D3DXComputeIMTFromSignal</span><span class="sxs-lookup"><span data-stu-id="b200f-104">D3DXComputeIMTFromSignal function</span></span>

<span data-ttu-id="b200f-105">Calcula o IMT por triângulo de um sinal especificado pelo aplicativo personalizado que varia na superfície da malha (geralmente com uma frequência maior do que os dados de vértice).</span><span class="sxs-lookup"><span data-stu-id="b200f-105">Calculates per-triangle IMT's from a custom application-specified signal that varies over the surface of the mesh (generally at a higher frequency than vertex data).</span></span> <span data-ttu-id="b200f-106">O sinal é avaliado por meio de uma função de retorno de chamada especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b200f-106">The signal is evaluated via a user-specified callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b200f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b200f-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="b200f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b200f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b200f-109">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b200f-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b200f-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="b200f-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="b200f-111">Um ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o IMT.</span><span class="sxs-lookup"><span data-stu-id="b200f-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="b200f-112">*dwTextureIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b200f-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b200f-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b200f-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b200f-114">Índice de coordenadas de textura baseado em zero que identifica o conjunto de coordenadas de textura a ser usado.</span><span class="sxs-lookup"><span data-stu-id="b200f-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="b200f-115">*uSignalDimension* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b200f-115">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b200f-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b200f-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b200f-117">O número de componentes em cada ponto de dados no sinal.</span><span class="sxs-lookup"><span data-stu-id="b200f-117">The number of components in each data point in the signal.</span></span>

</dd> <dt>

<span data-ttu-id="b200f-118">*fMaxUVDistance* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b200f-118">*fMaxUVDistance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b200f-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b200f-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b200f-120">A distância máxima entre os vértices; o algoritmo continua subdividindo até que a distância entre todos os vértices seja menor ou igual a fMaxUVDistance.</span><span class="sxs-lookup"><span data-stu-id="b200f-120">The maximum distance between vertices; the algorithm continues subdividing until the distance between all vertices is less than or equal to fMaxUVDistance.</span></span>

</dd> <dt>

<span data-ttu-id="b200f-121">*dwOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b200f-121">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b200f-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b200f-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b200f-123">Opções de quebra automática de textura.</span><span class="sxs-lookup"><span data-stu-id="b200f-123">Texture wrap options.</span></span> <span data-ttu-id="b200f-124">Essa é uma combinação de um ou mais [**sinalizadores D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b200f-124">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b200f-125">*pSignalCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b200f-125">*pSignalCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b200f-126">Tipo: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span><span class="sxs-lookup"><span data-stu-id="b200f-126">Type: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span></span>

<span data-ttu-id="b200f-127">Um ponteiro para uma função de avaliador fornecida pelo usuário, que será usado para calcular o valor de sinal em coordenadas U, x arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="b200f-127">A pointer to a user-provided evaluator function, which will be used to compute the signal value at arbitrary U,V coordinates.</span></span> <span data-ttu-id="b200f-128">A função segue o protótipo de [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span><span class="sxs-lookup"><span data-stu-id="b200f-128">The function follows the prototype of [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span></span>

</dd> <dt>

<span data-ttu-id="b200f-129">*pUserData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b200f-129">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b200f-130">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="b200f-130">Type: **VOID\***</span></span>

<span data-ttu-id="b200f-131">Um ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada de sinal.</span><span class="sxs-lookup"><span data-stu-id="b200f-131">A pointer to a user-defined value which is passed to the signal callback function.</span></span> <span data-ttu-id="b200f-132">Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b200f-132">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="b200f-133">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="b200f-133">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="b200f-134">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="b200f-134">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="b200f-135">Um ponteiro para uma função de retorno de chamada para monitorar o progresso da computação IMT.</span><span class="sxs-lookup"><span data-stu-id="b200f-135">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="b200f-136">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="b200f-136">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="b200f-137">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b200f-137">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b200f-138">Um ponteiro para uma variável definida pelo usuário que é passada para a função de retorno de chamada de status.</span><span class="sxs-lookup"><span data-stu-id="b200f-138">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="b200f-139">Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b200f-139">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="b200f-140">*ppIMTData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b200f-140">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b200f-141">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b200f-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b200f-142">Um ponteiro para o buffer (consulte [**ID3DXBuffer**](id3dxbuffer.md)) que contém a matriz IMT retornada.</span><span class="sxs-lookup"><span data-stu-id="b200f-142">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="b200f-143">Essa matriz pode ser fornecida como entrada para as [funções D3DX UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) para priorizar a alocação de espaço de textura na parametrização de textura.</span><span class="sxs-lookup"><span data-stu-id="b200f-143">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b200f-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b200f-144">Return value</span></span>

<span data-ttu-id="b200f-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b200f-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b200f-146">Se a função for realizada com sucesso, o valor de retorno será D3D \_ OK; caso contrário, o valor será D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b200f-146">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b200f-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="b200f-147">Remarks</span></span>

<span data-ttu-id="b200f-148">Essa função requer que a malha de entrada contenha um mapeamento de textura de sinal para malha (as coordenadas de IE. Texture).</span><span class="sxs-lookup"><span data-stu-id="b200f-148">This function requires that the input mesh contain a signal-to-mesh texture mapping (ie. texture coordinates).</span></span> <span data-ttu-id="b200f-149">Ele permite que o usuário defina um sinal arbitrariamente sobre a superfície da malha.</span><span class="sxs-lookup"><span data-stu-id="b200f-149">It allows the user to define a signal arbitrarily over the surface of the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="b200f-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b200f-150">Requirements</span></span>



| <span data-ttu-id="b200f-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="b200f-151">Requirement</span></span> | <span data-ttu-id="b200f-152">Valor</span><span class="sxs-lookup"><span data-stu-id="b200f-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b200f-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b200f-153">Header</span></span><br/>  | <dl> <span data-ttu-id="b200f-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b200f-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b200f-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b200f-155">Library</span></span><br/> | <dl> <span data-ttu-id="b200f-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b200f-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b200f-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="b200f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b200f-158">Funções UVAtlas</span><span class="sxs-lookup"><span data-stu-id="b200f-158">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="b200f-159">Usando o UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b200f-159">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
