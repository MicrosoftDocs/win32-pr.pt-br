---
description: Usa a GPU para calcular a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica (SH) esférica. A computação da iluminação na GPU geralmente será muito mais rápida do que na CPU.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'Método ID3DXPRTEngine:: ComputeDirectLightingSHGPU (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105769371"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a><span data-ttu-id="a92d5-104">Método ID3DXPRTEngine:: ComputeDirectLightingSHGPU</span><span class="sxs-lookup"><span data-stu-id="a92d5-104">ID3DXPRTEngine::ComputeDirectLightingSHGPU method</span></span>

<span data-ttu-id="a92d5-105">Usa a GPU para calcular a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica (SH) esférica.</span><span class="sxs-lookup"><span data-stu-id="a92d5-105">Uses the GPU to compute the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span> <span data-ttu-id="a92d5-106">A computação da iluminação na GPU geralmente será muito mais rápida do que na CPU.</span><span class="sxs-lookup"><span data-stu-id="a92d5-106">Computing the lighting on the GPU will generally be much faster than on the CPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="a92d5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a92d5-107">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="a92d5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a92d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a92d5-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a92d5-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92d5-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a92d5-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a92d5-111">Ponteiro para o objeto de dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usado para executar a simulação na GPU.</span><span class="sxs-lookup"><span data-stu-id="a92d5-111">Pointer to the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used to run the simulation on the GPU.</span></span> <span data-ttu-id="a92d5-112">O dispositivo deve dar suporte a sombreadores do [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) pixel.</span><span class="sxs-lookup"><span data-stu-id="a92d5-112">The device must support [ps\_2\_0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) pixel shaders.</span></span>

> [!Note]  
> <span data-ttu-id="a92d5-113">As funções de retorno de chamada não devem usar o objeto de dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usado pelo simulador de GPU.</span><span class="sxs-lookup"><span data-stu-id="a92d5-113">Callback functions should not use the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used by the GPU simulator.</span></span>

 

</dd> <dt>

<span data-ttu-id="a92d5-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a92d5-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92d5-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a92d5-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a92d5-116">Parâmetro de simulação de GPU que define a resolução da sombra z-buffer.</span><span class="sxs-lookup"><span data-stu-id="a92d5-116">GPU simulation parameter that defines the resolution of the shadow z-buffer.</span></span> <span data-ttu-id="a92d5-117">Deve ser definido como um dos valores constantes de [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span><span class="sxs-lookup"><span data-stu-id="a92d5-117">Should be set to one of the constant values from [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span></span> <span data-ttu-id="a92d5-118">Para especificar uma simulação de precisão mais alta, o \_ valor de Highquality D3DXSHGPUSIMOPT pode ser combinado com um dos \_ valores SHADOWRESxxx D3DXSHGPUSIMOPT.</span><span class="sxs-lookup"><span data-stu-id="a92d5-118">To specifiy higher precision simulation, the D3DXSHGPUSIMOPT\_HIGHQUALITY value may be combined with one of the D3DXSHGPUSIMOPT\_SHADOWRESxxx values.</span></span>

</dd> <dt>

<span data-ttu-id="a92d5-119">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a92d5-119">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92d5-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a92d5-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a92d5-121">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="a92d5-121">Order of the SH evaluation.</span></span> <span data-ttu-id="a92d5-122">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="a92d5-122">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="a92d5-123">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="a92d5-123">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a92d5-124">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="a92d5-124">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="a92d5-125">*ZBias* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a92d5-125">*ZBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92d5-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a92d5-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a92d5-127">Tendência na direção normal.</span><span class="sxs-lookup"><span data-stu-id="a92d5-127">Bias in the normal direction.</span></span>

</dd> <dt>

<span data-ttu-id="a92d5-128">*ZAngleBias* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a92d5-128">*ZAngleBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92d5-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a92d5-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a92d5-130">Tendência na direção normal, dimensionada por um menos o cosseno do ângulo com o raio de luz.</span><span class="sxs-lookup"><span data-stu-id="a92d5-130">Bias in the normal direction, scaled by one minus the cosine of the angle with the light ray.</span></span>

</dd> <dt>

<span data-ttu-id="a92d5-131">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a92d5-131">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a92d5-132">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="a92d5-132">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="a92d5-133">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a92d5-133">Pointer to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="a92d5-134">Esse buffer deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="a92d5-134">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a92d5-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a92d5-135">Return value</span></span>

<span data-ttu-id="a92d5-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a92d5-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a92d5-137">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a92d5-137">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a92d5-138">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a92d5-138">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a92d5-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="a92d5-139">Remarks</span></span>

<span data-ttu-id="a92d5-140">Nesse método, o albedo não é multiplicado pelo sinal luminoso e apenas a luz de entrada é integrada ao simulador.</span><span class="sxs-lookup"><span data-stu-id="a92d5-140">In this method, the albedo is not multiplied by the light signal, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="a92d5-141">Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que a radiante de origem, gerando assim resultados mais precisos da compactação.</span><span class="sxs-lookup"><span data-stu-id="a92d5-141">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="a92d5-142">Chame [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vetor de PRT (transferência de radiante) precomputado pelo albedo.</span><span class="sxs-lookup"><span data-stu-id="a92d5-142">Call [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="a92d5-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a92d5-143">Requirements</span></span>



| <span data-ttu-id="a92d5-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="a92d5-144">Requirement</span></span> | <span data-ttu-id="a92d5-145">Valor</span><span class="sxs-lookup"><span data-stu-id="a92d5-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a92d5-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a92d5-146">Header</span></span><br/>  | <dl> <span data-ttu-id="a92d5-147"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a92d5-147"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a92d5-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a92d5-148">Library</span></span><br/> | <dl> <span data-ttu-id="a92d5-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a92d5-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a92d5-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="a92d5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a92d5-151">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="a92d5-151">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
