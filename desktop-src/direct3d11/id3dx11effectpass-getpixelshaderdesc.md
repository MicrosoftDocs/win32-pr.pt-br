---
title: Método ID3DX11EffectPass GetPixelShaderDesc (D3dx11effect. h)
description: Obtenha uma descrição do sombreador de pixel.
ms.assetid: 5772f197-7ac5-4492-9a41-eedb1a8b22c9
keywords:
- Método GetPixelShaderDesc Direct3D 11
- Método GetPixelShaderDesc Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, método GetPixelShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetPixelShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c04479a58eed0aa94616f0ffc092f17d52d9af4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968597"
---
# <a name="id3dx11effectpassgetpixelshaderdesc-method"></a><span data-ttu-id="4b642-106">Método ID3DX11EffectPass:: GetPixelShaderDesc</span><span class="sxs-lookup"><span data-stu-id="4b642-106">ID3DX11EffectPass::GetPixelShaderDesc method</span></span>

<span data-ttu-id="4b642-107">Obtenha uma descrição do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="4b642-107">Get a pixel-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b642-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b642-108">Syntax</span></span>


```C++
HRESULT GetPixelShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="4b642-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b642-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b642-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="4b642-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="4b642-111">Tipo: **[ **D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="4b642-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="4b642-112">Um ponteiro para uma descrição do sombreador de pixel (consulte [**D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="4b642-112">A pointer to a pixel-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b642-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b642-113">Return value</span></span>

<span data-ttu-id="4b642-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4b642-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4b642-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4b642-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b642-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b642-116">Remarks</span></span>

<span data-ttu-id="4b642-117">Uma passagem de efeito pode conter atribuições de estado de renderização e atribuições de objeto do sombreador.</span><span class="sxs-lookup"><span data-stu-id="4b642-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="4b642-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="4b642-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4b642-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="4b642-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4b642-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4b642-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b642-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b642-121">Requirements</span></span>



| <span data-ttu-id="4b642-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b642-122">Requirement</span></span> | <span data-ttu-id="4b642-123">Valor</span><span class="sxs-lookup"><span data-stu-id="4b642-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b642-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b642-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4b642-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b642-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4b642-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b642-126">Library</span></span><br/> | <dl> <span data-ttu-id="4b642-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="4b642-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b642-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b642-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b642-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="4b642-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





