---
title: Método ID3DX11EffectShaderVariable GetDomainShader (D3dx11effect. h)
description: Obtenha um sombreador de domínio.
ms.assetid: fd95a4f0-7df3-4098-843f-0a1e22209603
keywords:
- Método GetDomainShader Direct3D 11
- Método GetDomainShader Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, método GetDomainShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetDomainShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7f097fb950b60aaa9c7fa2d5b763b393d5e275
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173207"
---
# <a name="id3dx11effectshadervariablegetdomainshader-method"></a><span data-ttu-id="e0245-106">Método ID3DX11EffectShaderVariable:: GetDomainShader</span><span class="sxs-lookup"><span data-stu-id="e0245-106">ID3DX11EffectShaderVariable::GetDomainShader method</span></span>

<span data-ttu-id="e0245-107">Obtenha um sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="e0245-107">Get a domain shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0245-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0245-108">Syntax</span></span>


```C++
HRESULT GetDomainShader(
   UINT               ShaderIndex,
   ID3D11DomainShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="e0245-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0245-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0245-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="e0245-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="e0245-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e0245-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e0245-112">Índice do sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="e0245-112">Index of the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="e0245-113">*ppPS*</span><span class="sxs-lookup"><span data-stu-id="e0245-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="e0245-114">Tipo: **[ **ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="e0245-114">Type: **[**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***</span></span>

<span data-ttu-id="e0245-115">Ponteiro para um ponteiro [**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) que será definido para o sombreador de domínio no retorno.</span><span class="sxs-lookup"><span data-stu-id="e0245-115">Pointer to an [**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) pointer that will be set to the domain shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0245-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0245-116">Return value</span></span>

<span data-ttu-id="e0245-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0245-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0245-118">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e0245-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e0245-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0245-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e0245-120">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="e0245-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e0245-121">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="e0245-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e0245-122">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e0245-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e0245-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0245-123">Requirements</span></span>



| <span data-ttu-id="e0245-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0245-124">Requirement</span></span> | <span data-ttu-id="e0245-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e0245-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0245-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0245-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e0245-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0245-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e0245-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0245-128">Library</span></span><br/> | <dl> <span data-ttu-id="e0245-129"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="e0245-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0245-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0245-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0245-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="e0245-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

