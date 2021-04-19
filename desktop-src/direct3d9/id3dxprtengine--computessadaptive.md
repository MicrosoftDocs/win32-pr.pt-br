---
description: 'Computa um vetor de transferência que mapeia o radiante de origem para sair do radiante resultante da dispersão de subsuperfície, usando a amostragem adaptável e as propriedades de material definidas por ID3DXPRTEngine:: SetMeshMaterials.'
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'Método ID3DXPRTEngine:: ComputeSSAdaptive (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793654"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a><span data-ttu-id="98388-103">Método ID3DXPRTEngine:: ComputeSSAdaptive</span><span class="sxs-lookup"><span data-stu-id="98388-103">ID3DXPRTEngine::ComputeSSAdaptive method</span></span>

<span data-ttu-id="98388-104">Computa um vetor de transferência que mapeia o radiante de origem para sair do radiante resultante da dispersão de subsuperfície, usando a amostragem adaptável e as propriedades de material definidas por [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span><span class="sxs-lookup"><span data-stu-id="98388-104">Computes a transfer vector that maps source radiance to exit radiance resulting from subsurface scattering, using adaptive sampling and material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="98388-105">O método gera novos vértices e rostos na malha para aproximar com mais precisão o sinal de radiante de transferência (PRT) precomputado.</span><span class="sxs-lookup"><span data-stu-id="98388-105">The method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="98388-106">Esse método pode ser usado somente para materiais definidos por vértice em um objeto de malha.</span><span class="sxs-lookup"><span data-stu-id="98388-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="98388-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98388-107">Syntax</span></span>


```C++
HRESULT ComputeSSAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="98388-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98388-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98388-109">*pDataIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98388-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98388-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="98388-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="98388-111">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa o objeto 3D do salto claro anterior.</span><span class="sxs-lookup"><span data-stu-id="98388-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="98388-112">Esse buffer de entrada deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="98388-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="98388-113">*AdaptiveThresh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98388-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98388-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98388-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98388-115">Limite no vetor de PRT a ser usado para subdividir vértices de malha e rostos.</span><span class="sxs-lookup"><span data-stu-id="98388-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="98388-116">Se for menor que 1e-6F, um valor padrão de 1e-6F será especificado.</span><span class="sxs-lookup"><span data-stu-id="98388-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="98388-117">*MinEdgeLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98388-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98388-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98388-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98388-119">Comprimento mínimo de borda facial que será gerado na amostragem adaptável.</span><span class="sxs-lookup"><span data-stu-id="98388-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="98388-120">Se o método determinar que o valor é muito pequeno, um valor dependente de modelo será especificado.</span><span class="sxs-lookup"><span data-stu-id="98388-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span>

</dd> <dt>

<span data-ttu-id="98388-121">*MaxSubdiv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98388-121">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98388-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98388-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98388-123">Nível máximo de subdivisão de uma face que será usada na amostragem adaptável.</span><span class="sxs-lookup"><span data-stu-id="98388-123">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="98388-124">Se for zero, um valor padrão de 4 será especificado.</span><span class="sxs-lookup"><span data-stu-id="98388-124">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="98388-125">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="98388-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98388-126">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="98388-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="98388-127">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que modela um único salto da luz dispersa de subsuperfície.</span><span class="sxs-lookup"><span data-stu-id="98388-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="98388-128">Esse buffer de saída deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="98388-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="98388-129">*pDataTotal* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="98388-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98388-130">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="98388-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="98388-131">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que é a soma em execução de todas as saídas de pDataOut anteriores.</span><span class="sxs-lookup"><span data-stu-id="98388-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="98388-132">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="98388-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98388-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98388-133">Return value</span></span>

<span data-ttu-id="98388-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="98388-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="98388-135">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="98388-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="98388-136">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="98388-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="98388-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="98388-137">Remarks</span></span>

<span data-ttu-id="98388-138">Para modelar a dispersão de subsuperfície, chame esse método para cada salto leve depois que um método [**ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="98388-138">To model subsurface scattering, call this method for each light bounce after an [**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) method is called.</span></span>

<span data-ttu-id="98388-139">A saída desse método não inclui albedo, e apenas a luz de entrada é integrada ao simulador.</span><span class="sxs-lookup"><span data-stu-id="98388-139">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="98388-140">Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que a radiante de origem, gerando assim resultados mais precisos da compactação.</span><span class="sxs-lookup"><span data-stu-id="98388-140">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="98388-141">Chame [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vetor de PRT pelo albedo.</span><span class="sxs-lookup"><span data-stu-id="98388-141">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="98388-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98388-142">Requirements</span></span>



| <span data-ttu-id="98388-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="98388-143">Requirement</span></span> | <span data-ttu-id="98388-144">Valor</span><span class="sxs-lookup"><span data-stu-id="98388-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98388-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98388-145">Header</span></span><br/>  | <dl> <span data-ttu-id="98388-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="98388-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="98388-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98388-147">Library</span></span><br/> | <dl> <span data-ttu-id="98388-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98388-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="98388-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="98388-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98388-150">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="98388-150">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="98388-151">**ID3DXPRTEngine::ComputeBounce**</span><span class="sxs-lookup"><span data-stu-id="98388-151">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> <dt>

[<span data-ttu-id="98388-152">**ID3DXPRTEngine:: computar**</span><span class="sxs-lookup"><span data-stu-id="98388-152">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 
