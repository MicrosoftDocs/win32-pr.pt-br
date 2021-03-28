---
title: Método ID3DX11EffectSamplerVariable UndoSetSampler (D3dx11effect. h)
description: Reverter um estado de amostra definido anteriormente.
ms.assetid: bb837b12-d6c3-47e9-a0a1-0bfcfe0f3e4e
keywords:
- Método UndoSetSampler Direct3D 11
- Método UndoSetSampler Direct3D 11, interface ID3DX11EffectSamplerVariable
- Interface ID3DX11EffectSamplerVariable Direct3D 11, método UndoSetSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.UndoSetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e89d72130e92a477b3824f8e5f8fc935e99bd5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298801"
---
# <a name="id3dx11effectsamplervariableundosetsampler-method"></a><span data-ttu-id="d5e67-106">Método ID3DX11EffectSamplerVariable:: UndoSetSampler</span><span class="sxs-lookup"><span data-stu-id="d5e67-106">ID3DX11EffectSamplerVariable::UndoSetSampler method</span></span>

<span data-ttu-id="d5e67-107">Reverter um estado de amostra definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d5e67-107">Revert a previously set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e67-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5e67-108">Syntax</span></span>


```C++
HRESULT UndoSetSampler(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="d5e67-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5e67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e67-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="d5e67-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="d5e67-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d5e67-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d5e67-112">Indexe em uma matriz de interfaces de amostra.</span><span class="sxs-lookup"><span data-stu-id="d5e67-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="d5e67-113">Se houver apenas uma interface de amostra, use 0.</span><span class="sxs-lookup"><span data-stu-id="d5e67-113">If there is only one sampler interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5e67-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5e67-114">Return value</span></span>

<span data-ttu-id="d5e67-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5e67-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5e67-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d5e67-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5e67-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5e67-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5e67-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="d5e67-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d5e67-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="d5e67-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d5e67-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d5e67-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d5e67-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5e67-121">Requirements</span></span>



| <span data-ttu-id="d5e67-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5e67-122">Requirement</span></span> | <span data-ttu-id="d5e67-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d5e67-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e67-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5e67-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d5e67-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5e67-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d5e67-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5e67-126">Library</span></span><br/> | <dl> <span data-ttu-id="d5e67-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="d5e67-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5e67-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5e67-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e67-129">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="d5e67-129">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

