---
description: Computa, em um ponto arbitrário que não está em uma malha, um vetor de transferência que mapeia radiante de origem (representado por uma aproximação harmônica esférica (SH)) para sair de radiante.
ms.assetid: 44790465-440d-4426-b780-ed872fbf8efb
title: 'Método ID3DXPRTEngine:: ComputeSurfSamplesDirectSH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03adb1729a8a2e771ea681ccbdd180999d3adcbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298858"
---
# <a name="id3dxprtenginecomputesurfsamplesdirectsh-method"></a><span data-ttu-id="a68c5-103">Método ID3DXPRTEngine:: ComputeSurfSamplesDirectSH</span><span class="sxs-lookup"><span data-stu-id="a68c5-103">ID3DXPRTEngine::ComputeSurfSamplesDirectSH method</span></span>

<span data-ttu-id="a68c5-104">Computa, em um ponto arbitrário que não está em uma malha, um vetor de transferência que mapeia radiante de origem (representado por uma aproximação harmônica esférica (SH)) para sair de radiante.</span><span class="sxs-lookup"><span data-stu-id="a68c5-104">Computes, at an arbitrary point not on a mesh, a transfer vector that maps source radiance (represented by a spherical harmonic (SH) approximation) to exit radiance.</span></span>

## <a name="syntax"></a><span data-ttu-id="a68c5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a68c5-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesDirectSH(
  [in]            UINT            SHOrder,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="a68c5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a68c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a68c5-107">*SHOrder* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a68c5-107">*SHOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a68c5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a68c5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a68c5-109">Ordem da aproximação de SH a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a68c5-109">Order of the SH approximation to use.</span></span>

</dd> <dt>

<span data-ttu-id="a68c5-110">*NumSamples* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a68c5-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a68c5-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a68c5-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a68c5-112">Número de locais de exemplo.</span><span class="sxs-lookup"><span data-stu-id="a68c5-112">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="a68c5-113">*pSampleLocs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a68c5-113">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a68c5-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a68c5-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a68c5-115">Posição de cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="a68c5-115">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="a68c5-116">*pSampleNorms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a68c5-116">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a68c5-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a68c5-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a68c5-118">Vetor normal para cada local de exemplo.</span><span class="sxs-lookup"><span data-stu-id="a68c5-118">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="a68c5-119">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a68c5-119">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a68c5-120">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="a68c5-120">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="a68c5-121">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que modela a contribuição de iluminação direta até o ponto, usando a aproximação sh.</span><span class="sxs-lookup"><span data-stu-id="a68c5-121">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the SH approximation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a68c5-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a68c5-122">Return value</span></span>

<span data-ttu-id="a68c5-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a68c5-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a68c5-124">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a68c5-124">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a68c5-125">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a68c5-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a68c5-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="a68c5-126">Remarks</span></span>

<span data-ttu-id="a68c5-127">Não use um buffer de textura ao chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="a68c5-127">Do not use a texture buffer when calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a68c5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a68c5-128">Requirements</span></span>



| <span data-ttu-id="a68c5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a68c5-129">Requirement</span></span> | <span data-ttu-id="a68c5-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a68c5-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a68c5-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a68c5-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a68c5-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a68c5-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a68c5-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a68c5-133">Library</span></span><br/> | <dl> <span data-ttu-id="a68c5-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a68c5-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a68c5-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a68c5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a68c5-136">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="a68c5-136">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="a68c5-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span><span class="sxs-lookup"><span data-stu-id="a68c5-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> <dt>

[<span data-ttu-id="a68c5-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span><span class="sxs-lookup"><span data-stu-id="a68c5-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span></span>](id3dxprtengine--computesurfsamplesbounce.md)
</dt> </dl>

 

 
