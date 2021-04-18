---
description: Computa coeficientes de LDPRT (transferência de radiante precomputada) de forma local em relação aos vetores normais por amostra para minimizar o erro de quadrados mínimos em relação aos dados de ID3DXPRTBuffer de entrada.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'Método ID3DXPRTEngine:: ComputeLDPRTCoeffs (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815543"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a><span data-ttu-id="dbd3d-103">Método ID3DXPRTEngine:: ComputeLDPRTCoeffs</span><span class="sxs-lookup"><span data-stu-id="dbd3d-103">ID3DXPRTEngine::ComputeLDPRTCoeffs method</span></span>

<span data-ttu-id="dbd3d-104">Computa coeficientes de LDPRT (transferência de radiante precomputada) de forma local em relação aos vetores normais por amostra para minimizar o erro de quadrados mínimos em relação aos dados de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-104">Computes locally-deformable precomputed radiance transfer (LDPRT) coefficients relative to per-sample normal vectors to minimize the least-squares error with respect to input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) data.</span></span> <span data-ttu-id="dbd3d-105">Esses coeficientes podem ser usados com vetores normais de aparência ou transformação para modelar efeitos globais em objetos dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-105">These coefficients can be used with skinned or transformed normal vectors to model global effects on dynamic objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbd3d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbd3d-106">Syntax</span></span>


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="dbd3d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbd3d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbd3d-108">*pDataIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dbd3d-108">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd3d-109">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="dbd3d-109">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="dbd3d-110">Ponteiro para um objeto de dados de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada esférico harmônica (SH) radiante.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-110">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) spherical harmonic (SH) precomputed radiance transfer (PRT) data object.</span></span>

</dd> <dt>

<span data-ttu-id="dbd3d-111">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dbd3d-111">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd3d-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbd3d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbd3d-113">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-113">Order of the SH evaluation.</span></span> <span data-ttu-id="dbd3d-114">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-114">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="dbd3d-115">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="dbd3d-115">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="dbd3d-116">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-116">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="dbd3d-117">*pNormOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="dbd3d-117">*pNormOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd3d-118">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="dbd3d-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dbd3d-119">Matriz de vetor opcional a ser preenchida com sombreador-vetores normais ideais para os quais os coeficientes LDPRT são otimizados.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-119">Optional vector array to be filled with shader-optimal normal vectors for which LDPRT coefficients are optimized.</span></span> <span data-ttu-id="dbd3d-120">Essa matriz deve ter o mesmo tamanho que o número de amostras em pDataIn.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-120">This array must be the same size as the number of samples in pDataIn.</span></span> <span data-ttu-id="dbd3d-121">Se for **NULL**, os vetores normais da superfície serão usados.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-121">If **NULL**, surface normal vectors are used.</span></span>

</dd> <dt>

<span data-ttu-id="dbd3d-122">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="dbd3d-122">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd3d-123">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="dbd3d-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="dbd3d-124">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que contém os coeficientes de ordem harmônica por canal de cor por amostra.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-124">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that contains Order zonal harmonic coefficients per color channel per sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbd3d-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dbd3d-125">Return value</span></span>

<span data-ttu-id="dbd3d-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dbd3d-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dbd3d-127">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dbd3d-128">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbd3d-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbd3d-129">Remarks</span></span>

<span data-ttu-id="dbd3d-130">As soluções para sombreamento de vetores normais podem, opcionalmente, ser obtidas com esse método.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-130">Solutions for shading normal vectors can optionally be obtained with this method.</span></span> <span data-ttu-id="dbd3d-131">Esses vetores normais, juntamente com os coeficientes de LDPRT, podem representar com mais precisão o sinal de PRT.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-131">These normal vectors, along with the LDPRT coefficients, can more accurately represent the PRT signal.</span></span> <span data-ttu-id="dbd3d-132">Nesse caso, os coeficientes representam as harmônicas zonais orientadas na direção normal.</span><span class="sxs-lookup"><span data-stu-id="dbd3d-132">In this case, the coefficients represent zonal harmonics oriented in the normal direction.</span></span>

<span data-ttu-id="dbd3d-133">Este método não pode ser usado com resultados de [**ID3DXPRTEngine:: ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) ou [**ID3DXPRTEngine:: ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).</span><span class="sxs-lookup"><span data-stu-id="dbd3d-133">This method cannot be used with results from [**ID3DXPRTEngine::ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) or [**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbd3d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbd3d-134">Requirements</span></span>



| <span data-ttu-id="dbd3d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbd3d-135">Requirement</span></span> | <span data-ttu-id="dbd3d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="dbd3d-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbd3d-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbd3d-137">Header</span></span><br/>  | <dl> <span data-ttu-id="dbd3d-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbd3d-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dbd3d-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dbd3d-139">Library</span></span><br/> | <dl> <span data-ttu-id="dbd3d-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbd3d-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dbd3d-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbd3d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbd3d-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="dbd3d-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
