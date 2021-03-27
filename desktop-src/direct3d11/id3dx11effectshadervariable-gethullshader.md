---
title: Método ID3DX11EffectShaderVariable GetHullShader (D3dx11effect. h)
description: Obtenha um sombreador envoltória.
ms.assetid: 18b2a8fc-2c53-4858-9aaa-00d0dc86adee
keywords:
- Método GetHullShader Direct3D 11
- Método GetHullShader Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, método GetHullShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetHullShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac8e6e095eb1ddbba93d68bec87e85e0c4e22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989418"
---
# <a name="id3dx11effectshadervariablegethullshader-method"></a><span data-ttu-id="17791-106">Método ID3DX11EffectShaderVariable:: GetHullShader</span><span class="sxs-lookup"><span data-stu-id="17791-106">ID3DX11EffectShaderVariable::GetHullShader method</span></span>

<span data-ttu-id="17791-107">Obtenha um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="17791-107">Get a hull shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="17791-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17791-108">Syntax</span></span>


```C++
HRESULT GetHullShader(
   UINT             ShaderIndex,
   ID3D11HullShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="17791-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17791-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17791-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="17791-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="17791-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="17791-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="17791-112">Índice do sombreador.</span><span class="sxs-lookup"><span data-stu-id="17791-112">Index of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="17791-113">*ppPS*</span><span class="sxs-lookup"><span data-stu-id="17791-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="17791-114">Tipo: **[ **ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="17791-114">Type: **[**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)\*\***</span></span>

<span data-ttu-id="17791-115">Um ponteiro para um ponteiro [**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader) que será definido como o sombreador envoltória no retorno.</span><span class="sxs-lookup"><span data-stu-id="17791-115">A pointer to an [**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader) pointer that will be set to the hull shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17791-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17791-116">Return value</span></span>

<span data-ttu-id="17791-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17791-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17791-118">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="17791-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="17791-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="17791-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="17791-120">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="17791-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="17791-121">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="17791-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="17791-122">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="17791-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17791-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17791-123">Requirements</span></span>



| <span data-ttu-id="17791-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="17791-124">Requirement</span></span> | <span data-ttu-id="17791-125">Valor</span><span class="sxs-lookup"><span data-stu-id="17791-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17791-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17791-126">Header</span></span><br/>  | <dl> <span data-ttu-id="17791-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="17791-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="17791-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17791-128">Library</span></span><br/> | <dl> <span data-ttu-id="17791-129"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="17791-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17791-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="17791-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17791-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="17791-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

