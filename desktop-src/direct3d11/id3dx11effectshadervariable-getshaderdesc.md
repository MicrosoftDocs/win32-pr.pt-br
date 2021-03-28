---
title: Método ID3DX11EffectShaderVariable GetShaderDesc (D3dx11effect. h)
description: Obter uma descrição do sombreador.
ms.assetid: 7dd667d3-c500-4486-b279-a165befe8733
keywords:
- Método GetShaderDesc Direct3D 11
- Método GetShaderDesc Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, método GetShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c76730d1ad5f3de35e273034d3a17beb71fb7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968658"
---
# <a name="id3dx11effectshadervariablegetshaderdesc-method"></a><span data-ttu-id="bdf9e-106">Método ID3DX11EffectShaderVariable:: GetShaderDesc</span><span class="sxs-lookup"><span data-stu-id="bdf9e-106">ID3DX11EffectShaderVariable::GetShaderDesc method</span></span>

<span data-ttu-id="bdf9e-107">Obter uma descrição do sombreador.</span><span class="sxs-lookup"><span data-stu-id="bdf9e-107">Get a shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdf9e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdf9e-108">Syntax</span></span>


```C++
HRESULT GetShaderDesc(
   UINT                      ShaderIndex,
   D3DX11_EFFECT_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="bdf9e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdf9e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdf9e-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="bdf9e-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="bdf9e-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bdf9e-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bdf9e-112">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="bdf9e-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="bdf9e-113">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="bdf9e-113">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="bdf9e-114">Tipo: **[ **D3DX11 \_ de \_ sombreador de efeito \_ desc**](d3dx11-effect-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="bdf9e-114">Type: **[**D3DX11\_EFFECT\_SHADER\_DESC**](d3dx11-effect-shader-desc.md)\***</span></span>

<span data-ttu-id="bdf9e-115">Um ponteiro para uma descrição do sombreador (consulte [**D3DX11 \_ Effect \_ Shader \_ desc**](d3dx11-effect-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="bdf9e-115">A pointer to a shader description (see [**D3DX11\_EFFECT\_SHADER\_DESC**](d3dx11-effect-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdf9e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bdf9e-116">Return value</span></span>

<span data-ttu-id="bdf9e-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bdf9e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bdf9e-118">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bdf9e-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf9e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdf9e-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bdf9e-120">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="bdf9e-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bdf9e-121">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="bdf9e-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bdf9e-122">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bdf9e-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bdf9e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdf9e-123">Requirements</span></span>



| <span data-ttu-id="bdf9e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdf9e-124">Requirement</span></span> | <span data-ttu-id="bdf9e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bdf9e-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf9e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdf9e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="bdf9e-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf9e-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bdf9e-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdf9e-128">Library</span></span><br/> | <dl> <span data-ttu-id="bdf9e-129"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="bdf9e-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdf9e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdf9e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf9e-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="bdf9e-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

