---
description: 'Computa o radiante de origem resultante da dispersão de subsuperfície, usando as propriedades de material definidas por ID3DXPRTEngine:: SetMeshMaterials. Esse método pode ser usado somente para materiais definidos por vértice em um objeto de malha.'
ms.assetid: cdf0d9c1-70e3-44d5-b97a-0521e6739daf
title: 'Método ID3DXPRTEngine:: computate (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSS
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 89a69be6cc946ff6695d234b8bfb82532385526e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298862"
---
# <a name="id3dxprtenginecomputess-method"></a><span data-ttu-id="7b353-104">Método ID3DXPRTEngine:: computar</span><span class="sxs-lookup"><span data-stu-id="7b353-104">ID3DXPRTEngine::ComputeSS method</span></span>

<span data-ttu-id="7b353-105">Computa o radiante de origem resultante da dispersão de subsuperfície, usando as propriedades de material definidas por [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span><span class="sxs-lookup"><span data-stu-id="7b353-105">Computes the source radiance resulting from subsurface scattering, using material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="7b353-106">Esse método pode ser usado somente para materiais definidos por vértice em um objeto de malha.</span><span class="sxs-lookup"><span data-stu-id="7b353-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b353-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b353-107">Syntax</span></span>


```C++
HRESULT ComputeSS(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="7b353-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b353-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b353-109">*pDataIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b353-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b353-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="7b353-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="7b353-111">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa o objeto 3D do salto claro anterior.</span><span class="sxs-lookup"><span data-stu-id="7b353-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="7b353-112">Esse buffer de entrada deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="7b353-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="7b353-113">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7b353-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b353-114">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="7b353-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="7b353-115">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que modela um único salto da luz dispersa de subsuperfície.</span><span class="sxs-lookup"><span data-stu-id="7b353-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="7b353-116">Esse buffer de saída deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="7b353-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="7b353-117">*pDataTotal* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7b353-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b353-118">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="7b353-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="7b353-119">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que é a soma em execução de todas as saídas de pDataOut anteriores.</span><span class="sxs-lookup"><span data-stu-id="7b353-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="7b353-120">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7b353-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b353-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b353-121">Return value</span></span>

<span data-ttu-id="7b353-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7b353-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7b353-123">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b353-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7b353-124">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7b353-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b353-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b353-125">Remarks</span></span>

<span data-ttu-id="7b353-126">Para modelar a dispersão de subsuperfície, chame esse método para cada salto leve depois que um método ID3DXPRTEngine:: ComputeDirectLighting for chamado.</span><span class="sxs-lookup"><span data-stu-id="7b353-126">To model subsurface scattering, call this method for each light bounce after an ID3DXPRTEngine::ComputeDirectLighting method is called.</span></span>

<span data-ttu-id="7b353-127">Use a sequência de chamada a seguir para modelar a dispersão de subsuperfície.</span><span class="sxs-lookup"><span data-stu-id="7b353-127">Use the following calling sequence to model subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
    
hr = m_pPRTEngine->ComputeDirectLightingSH( SHOrder, pDataA );
    
// *pDataC should be set to zero. The ComputeSS call will add together the    
// direct lighting results from pDataA for non-subsurface scattering elements   
// and subsurface scattering results for the subsurface scattering elements.
    
hr = m_pPRTEngine->ComputeSS( pDataA, pDataB, pDataC );
if ( FAILED( hr ) ) goto Exit;
```



<span data-ttu-id="7b353-128">A saída desse método não inclui albedo, e apenas a luz de entrada é integrada ao simulador.</span><span class="sxs-lookup"><span data-stu-id="7b353-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="7b353-129">Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que a radiante de origem, gerando assim resultados mais precisos da compactação.</span><span class="sxs-lookup"><span data-stu-id="7b353-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="7b353-130">Chame [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vetor de PRT (transferência de radiante preputado) pelo albedo.</span><span class="sxs-lookup"><span data-stu-id="7b353-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b353-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b353-131">Requirements</span></span>



| <span data-ttu-id="7b353-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b353-132">Requirement</span></span> | <span data-ttu-id="7b353-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7b353-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b353-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b353-134">Header</span></span><br/>  | <dl> <span data-ttu-id="7b353-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b353-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7b353-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b353-136">Library</span></span><br/> | <dl> <span data-ttu-id="7b353-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b353-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b353-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b353-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b353-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="7b353-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="7b353-140">**ID3DXPRTEngine::ComputeBounce**</span><span class="sxs-lookup"><span data-stu-id="7b353-140">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> </dl>

 

 




