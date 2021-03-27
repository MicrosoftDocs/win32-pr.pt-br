---
title: Método ID3DX11EffectRenderTargetViewVariable SetRenderTarget (D3dx11effect. h)
description: Defina um destino de renderização.
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- Método SetRenderTarget Direct3D 11
- Método SetRenderTarget Direct3D 11, interface ID3DX11EffectRenderTargetViewVariable
- Interface ID3DX11EffectRenderTargetViewVariable Direct3D 11, método SetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb53f0dff19fcd8990575dc9b305b0fb2f7e149b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837984"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a><span data-ttu-id="9266d-106">Método ID3DX11EffectRenderTargetViewVariable:: SetRenderTarget</span><span class="sxs-lookup"><span data-stu-id="9266d-106">ID3DX11EffectRenderTargetViewVariable::SetRenderTarget method</span></span>

<span data-ttu-id="9266d-107">Defina um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="9266d-107">Set a render-target.</span></span>

## <a name="syntax"></a><span data-ttu-id="9266d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9266d-108">Syntax</span></span>


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="9266d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9266d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9266d-110">*origem*</span><span class="sxs-lookup"><span data-stu-id="9266d-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="9266d-111">Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span><span class="sxs-lookup"><span data-stu-id="9266d-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span></span>

<span data-ttu-id="9266d-112">Um ponteiro para uma interface de exibição de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="9266d-112">A pointer to a render-target-view interface.</span></span> <span data-ttu-id="9266d-113">Consulte [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="9266d-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9266d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9266d-114">Return value</span></span>

<span data-ttu-id="9266d-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9266d-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9266d-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9266d-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9266d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9266d-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9266d-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="9266d-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9266d-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="9266d-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9266d-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9266d-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9266d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9266d-121">Requirements</span></span>



| <span data-ttu-id="9266d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9266d-122">Requirement</span></span> | <span data-ttu-id="9266d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9266d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9266d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9266d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9266d-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9266d-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9266d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9266d-126">Library</span></span><br/> | <dl> <span data-ttu-id="9266d-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="9266d-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9266d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9266d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9266d-129">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="9266d-129">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





