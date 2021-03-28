---
title: Método ID3DX11EffectVariable de multiamostrar (D3dx11effect. h)
description: Obter uma variável de amostra.
ms.assetid: dff699f7-758a-442b-93eb-23a09468251f
keywords:
- Método asamostrador Direct3D 11
- Método asamostrador Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método asamostrador
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1213320950377f6981348a158c3d8c8ef4d4fd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989425"
---
# <a name="id3dx11effectvariableassampler-method"></a><span data-ttu-id="bccc1-106">Método ID3DX11EffectVariable:: asamostrador</span><span class="sxs-lookup"><span data-stu-id="bccc1-106">ID3DX11EffectVariable::AsSampler method</span></span>

<span data-ttu-id="bccc1-107">Obter uma variável de amostra.</span><span class="sxs-lookup"><span data-stu-id="bccc1-107">Get a sampler variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="bccc1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bccc1-108">Syntax</span></span>


```C++
ID3DX11EffectSamplerVariable* AsSampler();
```



## <a name="parameters"></a><span data-ttu-id="bccc1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bccc1-109">Parameters</span></span>

<span data-ttu-id="bccc1-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bccc1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bccc1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bccc1-111">Return value</span></span>

<span data-ttu-id="bccc1-112">Tipo: **[ **ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="bccc1-112">Type: **[**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)\***</span></span>

<span data-ttu-id="bccc1-113">Um ponteiro para uma variável de amostra.</span><span class="sxs-lookup"><span data-stu-id="bccc1-113">A pointer to a sampler variable.</span></span> <span data-ttu-id="bccc1-114">Consulte [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md).</span><span class="sxs-lookup"><span data-stu-id="bccc1-114">See [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bccc1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bccc1-115">Remarks</span></span>

<span data-ttu-id="bccc1-116">O asamostrador retorna uma versão da variável de efeito que foi especializada em uma variável de amostra.</span><span class="sxs-lookup"><span data-stu-id="bccc1-116">AsSampler returns a version of the effect variable that has been specialized to a sampler variable.</span></span> <span data-ttu-id="bccc1-117">De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados de amostra.</span><span class="sxs-lookup"><span data-stu-id="bccc1-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain sampler data.</span></span>

<span data-ttu-id="bccc1-118">Os aplicativos podem testar a validade do objeto retornado chamando [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="bccc1-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="bccc1-119">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="bccc1-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bccc1-120">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="bccc1-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bccc1-121">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bccc1-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bccc1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bccc1-122">Requirements</span></span>



| <span data-ttu-id="bccc1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bccc1-123">Requirement</span></span> | <span data-ttu-id="bccc1-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bccc1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bccc1-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bccc1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bccc1-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bccc1-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bccc1-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bccc1-127">Library</span></span><br/> | <dl> <span data-ttu-id="bccc1-128"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="bccc1-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bccc1-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bccc1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bccc1-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="bccc1-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





