---
title: Método ID3DX11EffectShaderVariable GetPatchConstantSignatureElementDesc (D3dx11effect. h)
description: Obtenha uma descrição da assinatura constante de patch.
ms.assetid: 72a86cf6-ace2-4306-ac5c-37d888c087f7
keywords:
- Método GetPatchConstantSignatureElementDesc Direct3D 11
- Método GetPatchConstantSignatureElementDesc Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, método GetPatchConstantSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPatchConstantSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fcbc8f7c1bc34b0da42dd08c255a04a6d2fc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989386"
---
# <a name="id3dx11effectshadervariablegetpatchconstantsignatureelementdesc-method"></a><span data-ttu-id="fa311-106">Método ID3DX11EffectShaderVariable:: GetPatchConstantSignatureElementDesc</span><span class="sxs-lookup"><span data-stu-id="fa311-106">ID3DX11EffectShaderVariable::GetPatchConstantSignatureElementDesc method</span></span>

<span data-ttu-id="fa311-107">Obtenha uma descrição da assinatura constante de patch.</span><span class="sxs-lookup"><span data-stu-id="fa311-107">Get a patch constant signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa311-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa311-108">Syntax</span></span>


```C++
HRESULT GetPatchConstantSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="fa311-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa311-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa311-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="fa311-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="fa311-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fa311-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fa311-112">Um índice de sombreador baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="fa311-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="fa311-113">*Element*</span><span class="sxs-lookup"><span data-stu-id="fa311-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="fa311-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fa311-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fa311-115">Um índice de elemento baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="fa311-115">A zero-based element index.</span></span>

</dd> <dt>

<span data-ttu-id="fa311-116">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="fa311-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="fa311-117">Tipo: **[ **D3D11 de \_ assinatura de \_ parâmetro \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="fa311-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="fa311-118">Um ponteiro para uma descrição de parâmetro (consulte o [**\_ parâmetro de assinatura D3D11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="fa311-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa311-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa311-119">Return value</span></span>

<span data-ttu-id="fa311-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fa311-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fa311-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fa311-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fa311-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa311-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fa311-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="fa311-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fa311-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="fa311-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fa311-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fa311-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fa311-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa311-126">Requirements</span></span>



| <span data-ttu-id="fa311-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa311-127">Requirement</span></span> | <span data-ttu-id="fa311-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fa311-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa311-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa311-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fa311-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa311-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fa311-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa311-131">Library</span></span><br/> | <dl> <span data-ttu-id="fa311-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="fa311-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa311-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa311-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa311-134">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="fa311-134">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

