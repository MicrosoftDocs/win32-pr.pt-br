---
description: Computa a radiante de origem resultante de um único salto de luz interrefletida. Esse método pode ser usado para qualquer cena acesa, incluindo um modelo de PRT (computação radiante) com base em harmônica esférica (SH).
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'Método ID3DXPRTEngine:: ComputeBounce (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d40d4b2686087864cad17df0feb99dbc890033b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298790"
---
# <a name="id3dxprtenginecomputebounce-method"></a><span data-ttu-id="3b6f1-104">Método ID3DXPRTEngine:: ComputeBounce</span><span class="sxs-lookup"><span data-stu-id="3b6f1-104">ID3DXPRTEngine::ComputeBounce method</span></span>

<span data-ttu-id="3b6f1-105">Computa a radiante de origem resultante de um único salto de luz interrefletida.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-105">Computes the source radiance resulting from a single bounce of interreflected light.</span></span> <span data-ttu-id="3b6f1-106">Esse método pode ser usado para qualquer cena acesa, incluindo um modelo de PRT (computação radiante) com base em harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="3b6f1-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based precomputed radiance transfer (PRT) model.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b6f1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b6f1-107">Syntax</span></span>


```C++
HRESULT ComputeBounce(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="3b6f1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b6f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b6f1-109">*pDataIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b6f1-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6f1-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="3b6f1-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="3b6f1-111">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa o objeto 3D do salto claro anterior.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="3b6f1-112">Esse buffer de entrada deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="3b6f1-113">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3b6f1-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6f1-114">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="3b6f1-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="3b6f1-115">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que modela um único salto da luz interrefletida.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the interreflected light.</span></span> <span data-ttu-id="3b6f1-116">Esse buffer de saída deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="3b6f1-117">*pDataTotal* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3b6f1-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6f1-118">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="3b6f1-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="3b6f1-119">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que é a soma em execução de todas as saídas de pDataOut anteriores.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="3b6f1-120">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b6f1-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b6f1-121">Return value</span></span>

<span data-ttu-id="3b6f1-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b6f1-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b6f1-123">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3b6f1-124">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b6f1-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b6f1-125">Remarks</span></span>

<span data-ttu-id="3b6f1-126">Use a seguinte sequência de chamada para modelar vários retornos leves com iluminação direta.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-126">Use the following calling sequence to model multiple light bounces with direct lighting.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



<span data-ttu-id="3b6f1-127">Use a sequência de chamada a seguir para modelar vários retornos leves com dispersão de subsuperfície.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-127">Use the following calling sequence to model multiple light bounces with subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



<span data-ttu-id="3b6f1-128">A saída desse método não inclui albedo, e apenas a luz de entrada é integrada ao simulador.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="3b6f1-129">Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que a radiante de origem, gerando assim resultados mais precisos da compactação.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="3b6f1-130">Chame [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vetor de PRT pelo albedo.</span><span class="sxs-lookup"><span data-stu-id="3b6f1-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b6f1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b6f1-131">Requirements</span></span>



| <span data-ttu-id="3b6f1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b6f1-132">Requirement</span></span> | <span data-ttu-id="3b6f1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="3b6f1-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b6f1-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b6f1-134">Header</span></span><br/>  | <dl> <span data-ttu-id="3b6f1-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b6f1-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3b6f1-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b6f1-136">Library</span></span><br/> | <dl> <span data-ttu-id="3b6f1-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b6f1-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3b6f1-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b6f1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b6f1-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="3b6f1-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="3b6f1-140">**ID3DXPRTEngine:: computar**</span><span class="sxs-lookup"><span data-stu-id="3b6f1-140">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 




