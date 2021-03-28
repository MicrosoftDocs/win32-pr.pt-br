---
title: Método ID3DX11EffectShaderVariable GetComputeShader (D3dx11effect. h)
description: Obtenha um sombreador de computação.
ms.assetid: 16a48be1-4e73-4206-837f-615f8d624086
keywords:
- Método GetComputeShader Direct3D 11
- Método GetComputeShader Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, método GetComputeShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetComputeShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9312a7d603370d53c0721574623733c9e75da8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173208"
---
# <a name="id3dx11effectshadervariablegetcomputeshader-method"></a><span data-ttu-id="bfc57-106">Método ID3DX11EffectShaderVariable:: GetComputeShader</span><span class="sxs-lookup"><span data-stu-id="bfc57-106">ID3DX11EffectShaderVariable::GetComputeShader method</span></span>

<span data-ttu-id="bfc57-107">Obtenha um sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="bfc57-107">Get a compute shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfc57-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfc57-108">Syntax</span></span>


```C++
HRESULT GetComputeShader(
   UINT                ShaderIndex,
   ID3D11ComputeShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="bfc57-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfc57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfc57-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="bfc57-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="bfc57-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bfc57-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bfc57-112">Índice do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="bfc57-112">Index of the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="bfc57-113">*ppPS*</span><span class="sxs-lookup"><span data-stu-id="bfc57-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="bfc57-114">Tipo: **[ **ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="bfc57-114">Type: **[**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***</span></span>

<span data-ttu-id="bfc57-115">Ponteiro para um ponteiro [**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) que será definido para o sombreador de computação no retorno.</span><span class="sxs-lookup"><span data-stu-id="bfc57-115">Pointer to an [**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) pointer that will be set to the compute shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfc57-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bfc57-116">Return value</span></span>

<span data-ttu-id="bfc57-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bfc57-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bfc57-118">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bfc57-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bfc57-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfc57-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bfc57-120">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="bfc57-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bfc57-121">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="bfc57-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bfc57-122">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bfc57-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bfc57-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfc57-123">Requirements</span></span>



| <span data-ttu-id="bfc57-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfc57-124">Requirement</span></span> | <span data-ttu-id="bfc57-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bfc57-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc57-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bfc57-126">Header</span></span><br/>  | <dl> <span data-ttu-id="bfc57-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfc57-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bfc57-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfc57-128">Library</span></span><br/> | <dl> <span data-ttu-id="bfc57-129"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="bfc57-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfc57-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfc57-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc57-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="bfc57-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

