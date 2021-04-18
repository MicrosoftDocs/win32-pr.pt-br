---
description: Computa uma projeção da iluminação direta da luz anterior devolvida em vetores de base esféricas (SH) que representam o radiante do incidente em locais especificados.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'Método ID3DXPRTEngine:: ComputeVolumeSamples (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810862"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a><span data-ttu-id="e0dd9-103">Método ID3DXPRTEngine:: ComputeVolumeSamples</span><span class="sxs-lookup"><span data-stu-id="e0dd9-103">ID3DXPRTEngine::ComputeVolumeSamples method</span></span>

<span data-ttu-id="e0dd9-104">Computa uma projeção da iluminação direta da luz anterior devolvida em vetores de base esféricas (SH) que representam o radiante do incidente em locais especificados.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-104">Computes a projection of the direct lighting from the previous light bounce into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0dd9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0dd9-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="e0dd9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0dd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0dd9-107">*pSurfDataIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0dd9-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dd9-108">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e0dd9-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e0dd9-109">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa o objeto 3D do salto claro anterior.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span>

</dd> <dt>

<span data-ttu-id="e0dd9-110">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0dd9-110">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dd9-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0dd9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0dd9-112">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-112">Order of the SH evaluation.</span></span> <span data-ttu-id="e0dd9-113">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-113">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e0dd9-114">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="e0dd9-114">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e0dd9-115">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-115">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e0dd9-116">*NumVolSamples.xml* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0dd9-116">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dd9-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0dd9-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0dd9-118">Número de locais de exemplo.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-118">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="e0dd9-119">*pSampleLocs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0dd9-119">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dd9-120">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e0dd9-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e0dd9-121">Posição de cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-121">Position for each sample.</span></span> <span data-ttu-id="e0dd9-122">Se pSampleLocs for **nulo**, o ComputeVolumeSamples computará as matrizes de transferência em cada vértice de malha.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-122">If pSampleLocs is **NULL**, ComputeVolumeSamples will compute transfer matrices at every mesh vertex.</span></span> <span data-ttu-id="e0dd9-123">No entanto, se pSampleLocs não for **nulo**, você deverá obter uma amostra em uma esfera (Set UseSphere = **true** e UseCosine = **false** em [**ID3DXPRTEngine:: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); caso contrário, ComputeVolumeSamples retornará D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-123">However, if pSampleLocs is not **NULL**, you must sample over a sphere (set UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); otherwise, ComputeVolumeSamples will return D3DERR\_INVALIDCALL.</span></span>

</dd> <dt>

<span data-ttu-id="e0dd9-124">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e0dd9-124">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dd9-125">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e0dd9-125">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e0dd9-126">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que projeta a iluminação direta da luz anterior, saltou para vetores de base sh.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-126">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the direct lighting from the previous light bounce into SH basis vectors.</span></span> <span data-ttu-id="e0dd9-127">Esse buffer deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-127">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0dd9-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0dd9-128">Return value</span></span>

<span data-ttu-id="e0dd9-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0dd9-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0dd9-130">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e0dd9-131">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0dd9-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0dd9-132">Remarks</span></span>

<span data-ttu-id="e0dd9-133">Esse método computa como a luz da função radiante de origem é refletida na superfície que representa a cena (pSurfDataIn) e chega em cada ponto no espaço especificado por pSampleLocs.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-133">This method computes how the light from the source radiance function is reflected off the surface that represents the scene (pSurfDataIn) and arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="e0dd9-134">Os coeficientes de SH representam o mapeamento, em cada ponto de pSampleLocs, do radiante de origem para transferir o incidente radiante.</span><span class="sxs-lookup"><span data-stu-id="e0dd9-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0dd9-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0dd9-135">Requirements</span></span>



| <span data-ttu-id="e0dd9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0dd9-136">Requirement</span></span> | <span data-ttu-id="e0dd9-137">Valor</span><span class="sxs-lookup"><span data-stu-id="e0dd9-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0dd9-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0dd9-138">Header</span></span><br/>  | <dl> <span data-ttu-id="e0dd9-139"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0dd9-139"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e0dd9-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0dd9-140">Library</span></span><br/> | <dl> <span data-ttu-id="e0dd9-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0dd9-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0dd9-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0dd9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0dd9-143">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="e0dd9-143">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="e0dd9-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span><span class="sxs-lookup"><span data-stu-id="e0dd9-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span></span>](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
