---
description: Computa amostras de PRT (transferência de radiante de computação) para um ponto arbitrário (e um vetor normal).
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: 'Método ID3DXPRTEngine:: ComputeSurfSamplesBounce (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55cea3e87850273b6ea8d190422bd77afeb831f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298860"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a><span data-ttu-id="7ae5d-103">Método ID3DXPRTEngine:: ComputeSurfSamplesBounce</span><span class="sxs-lookup"><span data-stu-id="7ae5d-103">ID3DXPRTEngine::ComputeSurfSamplesBounce method</span></span>

<span data-ttu-id="7ae5d-104">Computa amostras de PRT (transferência de radiante de computação) para um ponto arbitrário (e um vetor normal).</span><span class="sxs-lookup"><span data-stu-id="7ae5d-104">Computes precomputed radiance transfer (PRT) samples for an arbitrary point (and normal vector).</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ae5d-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="7ae5d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ae5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ae5d-107">*pSurfDataIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ae5d-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae5d-108">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="7ae5d-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="7ae5d-109">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa o radiante de origem do objeto 3D.</span><span class="sxs-lookup"><span data-stu-id="7ae5d-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the source radiance of the 3D object.</span></span> <span data-ttu-id="7ae5d-110">Esse buffer de entrada deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="7ae5d-110">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="7ae5d-111">*NumSamples* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ae5d-111">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae5d-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ae5d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ae5d-113">Número de locais de exemplo.</span><span class="sxs-lookup"><span data-stu-id="7ae5d-113">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="7ae5d-114">*pSampleLocs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ae5d-114">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae5d-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ae5d-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7ae5d-116">Posição de cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="7ae5d-116">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="7ae5d-117">*pSampleNorms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ae5d-117">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae5d-118">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ae5d-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7ae5d-119">Vetor normal para cada local de exemplo.</span><span class="sxs-lookup"><span data-stu-id="7ae5d-119">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="7ae5d-120">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7ae5d-120">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae5d-121">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="7ae5d-121">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="7ae5d-122">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que modela a contribuição de iluminação direta até o ponto, usando a aproximação harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="7ae5d-122">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the spherical harmonic (SH) approximation.</span></span>

</dd> <dt>

<span data-ttu-id="7ae5d-123">*pDataTotal* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7ae5d-123">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae5d-124">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="7ae5d-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="7ae5d-125">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que é a soma em execução de todas as saídas de pDataOut anteriores.</span><span class="sxs-lookup"><span data-stu-id="7ae5d-125">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="7ae5d-126">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7ae5d-126">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ae5d-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ae5d-127">Return value</span></span>

<span data-ttu-id="7ae5d-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ae5d-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ae5d-129">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7ae5d-129">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7ae5d-130">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7ae5d-130">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae5d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ae5d-131">Requirements</span></span>



| <span data-ttu-id="7ae5d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ae5d-132">Requirement</span></span> | <span data-ttu-id="7ae5d-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7ae5d-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae5d-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ae5d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="7ae5d-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ae5d-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7ae5d-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ae5d-136">Library</span></span><br/> | <dl> <span data-ttu-id="7ae5d-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ae5d-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7ae5d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ae5d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae5d-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="7ae5d-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="7ae5d-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span><span class="sxs-lookup"><span data-stu-id="7ae5d-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span></span>](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
