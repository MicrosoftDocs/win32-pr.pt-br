---
title: Método asshadr ID3DX11EffectVariable (D3dx11effect. h)
description: Obter uma variável de sombreador.
ms.assetid: 660ba087-5320-44f7-946f-e500101fc6bb
keywords:
- Método asshadr Direct3D 11
- Método asshadr Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método asshadr
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3c8d9f1a487e4003bd032180d1f815e4a48fe0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989362"
---
# <a name="id3dx11effectvariableasshader-method"></a><span data-ttu-id="e7efb-106">Método ID3DX11EffectVariable:: asshadr</span><span class="sxs-lookup"><span data-stu-id="e7efb-106">ID3DX11EffectVariable::AsShader method</span></span>

<span data-ttu-id="e7efb-107">Obter uma variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e7efb-107">Get a shader variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7efb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7efb-108">Syntax</span></span>


```C++
ID3DX11EffectShaderVariable* AsShader();
```



## <a name="parameters"></a><span data-ttu-id="e7efb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7efb-109">Parameters</span></span>

<span data-ttu-id="e7efb-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e7efb-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7efb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7efb-111">Return value</span></span>

<span data-ttu-id="e7efb-112">Tipo: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7efb-112">Type: **[**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span></span>

<span data-ttu-id="e7efb-113">Um ponteiro para uma variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e7efb-113">A pointer to a shader variable.</span></span> <span data-ttu-id="e7efb-114">Consulte [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md).</span><span class="sxs-lookup"><span data-stu-id="e7efb-114">See [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7efb-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7efb-115">Remarks</span></span>

<span data-ttu-id="e7efb-116">O asshadr retorna uma versão da variável de efeito que foi especializada em uma variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e7efb-116">AsShader returns a version of the effect variable that has been specialized to a shader variable.</span></span> <span data-ttu-id="e7efb-117">De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e7efb-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain shader data.</span></span>

<span data-ttu-id="e7efb-118">Os aplicativos podem testar a validade do objeto retornado chamando [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="e7efb-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="e7efb-119">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="e7efb-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e7efb-120">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="e7efb-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e7efb-121">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e7efb-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7efb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7efb-122">Requirements</span></span>



| <span data-ttu-id="e7efb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7efb-123">Requirement</span></span> | <span data-ttu-id="e7efb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e7efb-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7efb-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7efb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e7efb-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7efb-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e7efb-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7efb-127">Library</span></span><br/> | <dl> <span data-ttu-id="e7efb-128"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="e7efb-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7efb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7efb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7efb-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="e7efb-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





