---
title: Método ID3DX11EffectPass GetVertexShaderDesc (D3dx11effect. h)
description: Obter uma descrição de sombreador de vértice.
ms.assetid: 7e02a438-2ff4-4e32-bc16-d112aafa57cb
keywords:
- Método GetVertexShaderDesc Direct3D 11
- Método GetVertexShaderDesc Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, método GetVertexShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetVertexShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8c69bab360fa3d12ccfc1a701926183dad7bbe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930704"
---
# <a name="id3dx11effectpassgetvertexshaderdesc-method"></a><span data-ttu-id="5e902-106">Método ID3DX11EffectPass:: GetVertexShaderDesc</span><span class="sxs-lookup"><span data-stu-id="5e902-106">ID3DX11EffectPass::GetVertexShaderDesc method</span></span>

<span data-ttu-id="5e902-107">Obter uma descrição de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="5e902-107">Get a vertex-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e902-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e902-108">Syntax</span></span>


```C++
HRESULT GetVertexShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="5e902-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e902-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e902-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="5e902-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="5e902-111">Tipo: **[ **D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e902-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="5e902-112">Um ponteiro para uma descrição de sombreador de vértice (consulte [**D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="5e902-112">A pointer to a vertex-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e902-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e902-113">Return value</span></span>

<span data-ttu-id="5e902-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e902-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e902-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5e902-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e902-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e902-116">Remarks</span></span>

<span data-ttu-id="5e902-117">Uma passagem de efeito pode conter atribuições de estado de renderização e atribuições de objeto do sombreador.</span><span class="sxs-lookup"><span data-stu-id="5e902-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="5e902-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="5e902-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5e902-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="5e902-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5e902-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5e902-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e902-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e902-121">Requirements</span></span>



| <span data-ttu-id="5e902-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e902-122">Requirement</span></span> | <span data-ttu-id="5e902-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5e902-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e902-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e902-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5e902-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e902-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5e902-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e902-126">Library</span></span><br/> | <dl> <span data-ttu-id="5e902-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="5e902-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e902-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e902-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e902-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="5e902-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





