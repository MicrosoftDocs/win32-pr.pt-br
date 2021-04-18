---
description: Computa a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica esférica (SH).
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: 'Método ID3DXPRTEngine:: ComputeDirectLightingSH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 01b6c3cff082c40c4df5d9bee1d997599a41965b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813669"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a><span data-ttu-id="b74c2-103">Método ID3DXPRTEngine:: ComputeDirectLightingSH</span><span class="sxs-lookup"><span data-stu-id="b74c2-103">ID3DXPRTEngine::ComputeDirectLightingSH method</span></span>

<span data-ttu-id="b74c2-104">Computa a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="b74c2-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b74c2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b74c2-105">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="b74c2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b74c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b74c2-107">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b74c2-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b74c2-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b74c2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b74c2-109">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="b74c2-109">Order of the SH evaluation.</span></span> <span data-ttu-id="b74c2-110">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="b74c2-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="b74c2-111">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="b74c2-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="b74c2-112">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="b74c2-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="b74c2-113">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b74c2-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b74c2-114">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="b74c2-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="b74c2-115">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que modela a contribuição de iluminação direta com a aproximação sh.</span><span class="sxs-lookup"><span data-stu-id="b74c2-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution with the SH approximation.</span></span> <span data-ttu-id="b74c2-116">Esse buffer deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="b74c2-116">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b74c2-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b74c2-117">Return value</span></span>

<span data-ttu-id="b74c2-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b74c2-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b74c2-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b74c2-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b74c2-120">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b74c2-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b74c2-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b74c2-121">Remarks</span></span>

<span data-ttu-id="b74c2-122">A saída não inclui albedo, e apenas a luz de entrada é integrada ao simulador.</span><span class="sxs-lookup"><span data-stu-id="b74c2-122">The output does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="b74c2-123">Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que a radiante de origem, gerando assim resultados mais precisos da compactação.</span><span class="sxs-lookup"><span data-stu-id="b74c2-123">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="b74c2-124">Chame [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vetor de PRT (transferência de radiante preputado) pelo albedo.</span><span class="sxs-lookup"><span data-stu-id="b74c2-124">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="b74c2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b74c2-125">Requirements</span></span>



| <span data-ttu-id="b74c2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b74c2-126">Requirement</span></span> | <span data-ttu-id="b74c2-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b74c2-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b74c2-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b74c2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b74c2-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b74c2-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b74c2-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b74c2-130">Library</span></span><br/> | <dl> <span data-ttu-id="b74c2-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b74c2-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b74c2-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b74c2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b74c2-133">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="b74c2-133">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
