---
description: Computa uma projeção de iluminação distante em vetores de base esféricas (SH) que representam o radiante do incidente em locais especificados.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'Método ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807806"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a><span data-ttu-id="b3e54-103">Método ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH</span><span class="sxs-lookup"><span data-stu-id="b3e54-103">ID3DXPRTEngine::ComputeVolumeSamplesDirectSH method</span></span>

<span data-ttu-id="b3e54-104">Computa uma projeção de iluminação distante em vetores de base esféricas (SH) que representam o radiante do incidente em locais especificados.</span><span class="sxs-lookup"><span data-stu-id="b3e54-104">Computes a projection of distant lighting into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3e54-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3e54-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="b3e54-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3e54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3e54-107">*Ordenar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3e54-107">*OrderIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3e54-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3e54-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3e54-109">Ordem da representação de SH de iluminação distante.</span><span class="sxs-lookup"><span data-stu-id="b3e54-109">Order of the SH representation of distant lighting.</span></span> <span data-ttu-id="b3e54-110">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="b3e54-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="b3e54-111">O grau da avaliação é o pedido-1.</span><span class="sxs-lookup"><span data-stu-id="b3e54-111">The degree of the evaluation is OrderIn - 1.</span></span>

</dd> <dt>

<span data-ttu-id="b3e54-112">*Pedido* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3e54-112">*OrderOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3e54-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3e54-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3e54-114">Ordem da representação de SH da iluminação local.</span><span class="sxs-lookup"><span data-stu-id="b3e54-114">Order of the SH representation of local lighting.</span></span> <span data-ttu-id="b3e54-115">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="b3e54-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="b3e54-116">O grau da avaliação é Order out-1.</span><span class="sxs-lookup"><span data-stu-id="b3e54-116">The degree of the evaluation is OrderOut - 1.</span></span>

</dd> <dt>

<span data-ttu-id="b3e54-117">*NumVolSamples.xml* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3e54-117">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3e54-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3e54-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3e54-119">Número de locais de exemplo.</span><span class="sxs-lookup"><span data-stu-id="b3e54-119">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="b3e54-120">*pSampleLocs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3e54-120">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3e54-121">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3e54-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b3e54-122">Posição de cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="b3e54-122">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="b3e54-123">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b3e54-123">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3e54-124">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="b3e54-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="b3e54-125">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que projeta a iluminação distante em vetores de base de sh.</span><span class="sxs-lookup"><span data-stu-id="b3e54-125">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the distant lighting into SH basis vectors.</span></span> <span data-ttu-id="b3e54-126">Esse buffer deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="b3e54-126">This buffer must have the proper number of color channels allocated for the simulation.</span></span> <span data-ttu-id="b3e54-127">Esse método gera o pedido \* de pedido ² "² escalars por canal em cada local de exemplo.</span><span class="sxs-lookup"><span data-stu-id="b3e54-127">This method generates OrderIn² \* OrderOut"² scalars per channel at each sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3e54-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3e54-128">Return value</span></span>

<span data-ttu-id="b3e54-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3e54-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3e54-130">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3e54-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b3e54-131">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b3e54-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3e54-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3e54-132">Remarks</span></span>

<span data-ttu-id="b3e54-133">Esse método computa como a luz de uma fonte distante chega em cada ponto no espaço especificado por pSampleLocs.</span><span class="sxs-lookup"><span data-stu-id="b3e54-133">This method computes how light from a distant source arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="b3e54-134">Os coeficientes de SH representam o mapeamento, em cada ponto de pSampleLocs, do radiante de origem para transferir o incidente radiante.</span><span class="sxs-lookup"><span data-stu-id="b3e54-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

<span data-ttu-id="b3e54-135">Para usar esse método com êxito, você deve definir a amostragem em uma esfera com UseSphere = **true** e UseCosine = **false** em [**ID3DXPRTEngine:: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); caso contrário, esse método retornará um erro com D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b3e54-135">To use this method successfully, you must set sampling over a sphere with UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); otherwise, this method will return an error with D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3e54-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3e54-136">Requirements</span></span>



| <span data-ttu-id="b3e54-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3e54-137">Requirement</span></span> | <span data-ttu-id="b3e54-138">Valor</span><span class="sxs-lookup"><span data-stu-id="b3e54-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e54-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3e54-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b3e54-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3e54-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b3e54-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3e54-141">Library</span></span><br/> | <dl> <span data-ttu-id="b3e54-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3e54-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3e54-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3e54-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e54-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="b3e54-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="b3e54-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span><span class="sxs-lookup"><span data-stu-id="b3e54-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span></span>](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
