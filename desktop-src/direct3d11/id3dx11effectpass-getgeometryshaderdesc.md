---
title: Método ID3DX11EffectPass GetGeometryShaderDesc (D3dx11effect. h)
description: Obtenha uma descrição do sombreador Geometry.
ms.assetid: 03298ec3-6b85-40bf-8920-a82c7606d326
keywords:
- Método GetGeometryShaderDesc Direct3D 11
- Método GetGeometryShaderDesc Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, método GetGeometryShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetGeometryShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c3b84ed9e8c245611c1442987b68a94e7b10ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989322"
---
# <a name="id3dx11effectpassgetgeometryshaderdesc-method"></a><span data-ttu-id="2da41-106">Método ID3DX11EffectPass:: GetGeometryShaderDesc</span><span class="sxs-lookup"><span data-stu-id="2da41-106">ID3DX11EffectPass::GetGeometryShaderDesc method</span></span>

<span data-ttu-id="2da41-107">Obtenha uma descrição do sombreador Geometry.</span><span class="sxs-lookup"><span data-stu-id="2da41-107">Get a geometry-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da41-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2da41-108">Syntax</span></span>


```C++
HRESULT GetGeometryShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="2da41-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2da41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da41-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="2da41-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="2da41-111">Tipo: **[ **D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="2da41-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="2da41-112">Um ponteiro para uma descrição Geometry-Shader (consulte [**D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="2da41-112">A pointer to a geometry-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da41-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2da41-113">Return value</span></span>

<span data-ttu-id="2da41-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2da41-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2da41-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2da41-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2da41-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2da41-116">Remarks</span></span>

<span data-ttu-id="2da41-117">Uma passagem de efeito pode conter atribuições de estado de renderização e atribuições de objeto do sombreador.</span><span class="sxs-lookup"><span data-stu-id="2da41-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="2da41-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="2da41-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2da41-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="2da41-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2da41-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2da41-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2da41-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2da41-121">Requirements</span></span>



| <span data-ttu-id="2da41-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2da41-122">Requirement</span></span> | <span data-ttu-id="2da41-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2da41-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da41-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2da41-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2da41-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2da41-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2da41-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2da41-126">Library</span></span><br/> | <dl> <span data-ttu-id="2da41-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="2da41-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da41-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2da41-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da41-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="2da41-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





