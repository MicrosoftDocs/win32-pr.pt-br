---
title: Método ID3DX11EffectShaderVariable GetOutputSignatureElementDesc (D3dx11effect. h)
description: Obtenha uma descrição de assinatura de saída.
ms.assetid: 05f43a57-18fa-4be7-814e-ffbe53837cab
keywords:
- Método GetOutputSignatureElementDesc Direct3D 11
- Método GetOutputSignatureElementDesc Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, método GetOutputSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetOutputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29545754be560a3a7710adf23963566a324d8a3f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989387"
---
# <a name="id3dx11effectshadervariablegetoutputsignatureelementdesc-method"></a><span data-ttu-id="6abf6-106">Método ID3DX11EffectShaderVariable:: GetOutputSignatureElementDesc</span><span class="sxs-lookup"><span data-stu-id="6abf6-106">ID3DX11EffectShaderVariable::GetOutputSignatureElementDesc method</span></span>

<span data-ttu-id="6abf6-107">Obtenha uma descrição de assinatura de saída.</span><span class="sxs-lookup"><span data-stu-id="6abf6-107">Get an output-signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6abf6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6abf6-108">Syntax</span></span>


```C++
HRESULT GetOutputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="6abf6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6abf6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6abf6-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="6abf6-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="6abf6-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6abf6-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6abf6-112">Um índice de sombreador baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="6abf6-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="6abf6-113">*Element*</span><span class="sxs-lookup"><span data-stu-id="6abf6-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="6abf6-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6abf6-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6abf6-115">Um índice de elemento baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="6abf6-115">A zero-based element index.</span></span>

</dd> <dt>

<span data-ttu-id="6abf6-116">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="6abf6-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="6abf6-117">Tipo: **[ **D3D11 de \_ assinatura de \_ parâmetro \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="6abf6-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="6abf6-118">Um ponteiro para uma descrição de parâmetro (consulte o [**\_ parâmetro de assinatura D3D11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="6abf6-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6abf6-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6abf6-119">Return value</span></span>

<span data-ttu-id="6abf6-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6abf6-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6abf6-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6abf6-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6abf6-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6abf6-122">Remarks</span></span>

<span data-ttu-id="6abf6-123">Um efeito contém um ou mais sombreadores; cada sombreador tem uma assinatura de entrada e saída; cada assinatura contém um ou mais elementos (ou parâmetros).</span><span class="sxs-lookup"><span data-stu-id="6abf6-123">An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters).</span></span> <span data-ttu-id="6abf6-124">O índice do sombreador identifica o sombreador e o índice do elemento identifica o elemento (ou parâmetro) na assinatura do sombreador.</span><span class="sxs-lookup"><span data-stu-id="6abf6-124">The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.</span></span>

> [!Note]  
> <span data-ttu-id="6abf6-125">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="6abf6-125">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6abf6-126">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="6abf6-126">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6abf6-127">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6abf6-127">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6abf6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6abf6-128">Requirements</span></span>



| <span data-ttu-id="6abf6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6abf6-129">Requirement</span></span> | <span data-ttu-id="6abf6-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6abf6-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6abf6-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6abf6-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6abf6-132"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6abf6-132"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6abf6-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6abf6-133">Library</span></span><br/> | <dl> <span data-ttu-id="6abf6-134"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="6abf6-134"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6abf6-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6abf6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6abf6-136">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="6abf6-136">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

