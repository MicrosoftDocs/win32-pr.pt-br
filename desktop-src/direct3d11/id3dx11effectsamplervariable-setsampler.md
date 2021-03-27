---
title: Método setamostrador ID3DX11EffectSamplerVariable (D3dx11effect. h)
description: Defina o estado de amostra.
ms.assetid: 1826923d-d770-4d79-818a-a42a279f0a8c
keywords:
- Método setamostrador Direct3D 11
- Método setamostrar Direct3D 11, interface ID3DX11EffectSamplerVariable
- Interface ID3DX11EffectSamplerVariable Direct3D 11, método setamostrar
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.SetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a68adef00ac980b532e2fcd877e71eb63dc470
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298689"
---
# <a name="id3dx11effectsamplervariablesetsampler-method"></a><span data-ttu-id="fbe68-106">Método ID3DX11EffectSamplerVariable:: setamostrar</span><span class="sxs-lookup"><span data-stu-id="fbe68-106">ID3DX11EffectSamplerVariable::SetSampler method</span></span>

<span data-ttu-id="fbe68-107">Defina o estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="fbe68-107">Set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbe68-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbe68-108">Syntax</span></span>


```C++
HRESULT SetSampler(
   UINT               Index,
   ID3D11SamplerState *pSampler
);
```



## <a name="parameters"></a><span data-ttu-id="fbe68-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbe68-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbe68-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="fbe68-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="fbe68-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fbe68-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fbe68-112">Indexe em uma matriz de interfaces de amostra.</span><span class="sxs-lookup"><span data-stu-id="fbe68-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="fbe68-113">Se houver apenas uma interface de amostra, use 0.</span><span class="sxs-lookup"><span data-stu-id="fbe68-113">If there is only one sampler interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="fbe68-114">*pSampler*</span><span class="sxs-lookup"><span data-stu-id="fbe68-114">*pSampler*</span></span> 
</dt> <dd>

<span data-ttu-id="fbe68-115">Tipo: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span><span class="sxs-lookup"><span data-stu-id="fbe68-115">Type: **[**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span></span>

<span data-ttu-id="fbe68-116">Ponteiro para uma interface [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) que contém o estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="fbe68-116">Pointer to an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) interface containing the sampler state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbe68-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbe68-117">Return value</span></span>

<span data-ttu-id="fbe68-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fbe68-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fbe68-119">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fbe68-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fbe68-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbe68-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fbe68-121">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="fbe68-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fbe68-122">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="fbe68-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fbe68-123">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fbe68-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fbe68-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbe68-124">Requirements</span></span>



| <span data-ttu-id="fbe68-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbe68-125">Requirement</span></span> | <span data-ttu-id="fbe68-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fbe68-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe68-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbe68-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fbe68-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbe68-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fbe68-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fbe68-129">Library</span></span><br/> | <dl> <span data-ttu-id="fbe68-130"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="fbe68-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbe68-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbe68-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe68-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="fbe68-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

