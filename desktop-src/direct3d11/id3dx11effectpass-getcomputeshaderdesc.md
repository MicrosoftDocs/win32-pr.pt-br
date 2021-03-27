---
title: Método ID3DX11EffectPass GetComputeShaderDesc (D3dx11effect. h)
description: Obtenha uma descrição do sombreador de computação.
ms.assetid: 9c3a702f-2016-4b1a-a832-d1bb968aec2d
keywords:
- Método GetComputeShaderDesc Direct3D 11
- Método GetComputeShaderDesc Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, método GetComputeShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetComputeShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21cc13699553b0da60498209ddffd31a56607809
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930705"
---
# <a name="id3dx11effectpassgetcomputeshaderdesc-method"></a><span data-ttu-id="fd8fd-106">Método ID3DX11EffectPass:: GetComputeShaderDesc</span><span class="sxs-lookup"><span data-stu-id="fd8fd-106">ID3DX11EffectPass::GetComputeShaderDesc method</span></span>

<span data-ttu-id="fd8fd-107">Obtenha uma descrição do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="fd8fd-107">Get a compute-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd8fd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd8fd-108">Syntax</span></span>


```C++
HRESULT GetComputeShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="fd8fd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd8fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd8fd-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="fd8fd-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="fd8fd-111">Tipo: **[ **D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd8fd-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="fd8fd-112">Um ponteiro para uma descrição de sombreador de computação (consulte [**D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="fd8fd-112">A pointer to a compute-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd8fd-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd8fd-113">Return value</span></span>

<span data-ttu-id="fd8fd-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd8fd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd8fd-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fd8fd-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd8fd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd8fd-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fd8fd-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="fd8fd-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fd8fd-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="fd8fd-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fd8fd-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fd8fd-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd8fd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd8fd-120">Requirements</span></span>



| <span data-ttu-id="fd8fd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd8fd-121">Requirement</span></span> | <span data-ttu-id="fd8fd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fd8fd-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8fd-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd8fd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fd8fd-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd8fd-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fd8fd-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd8fd-125">Library</span></span><br/> | <dl> <span data-ttu-id="fd8fd-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="fd8fd-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd8fd-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd8fd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8fd-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="fd8fd-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





