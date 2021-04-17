---
title: Método ID3DX11EffectDepthStencilViewVariable GetDepthStencil (D3dx11effect. h)
description: Obtenha um recurso de exibição de estêncil de profundidade.
ms.assetid: 7d94d98b-7070-41ee-9a9d-fe848f8914f2
keywords:
- Método GetDepthStencil Direct3D 11
- Método GetDepthStencil Direct3D 11, interface ID3DX11EffectDepthStencilViewVariable
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, método GetDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49206f051922982ac77265e68fa3d7b7397d1348
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968664"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencil-method"></a><span data-ttu-id="7739e-106">Método ID3DX11EffectDepthStencilViewVariable:: GetDepthStencil</span><span class="sxs-lookup"><span data-stu-id="7739e-106">ID3DX11EffectDepthStencilViewVariable::GetDepthStencil method</span></span>

<span data-ttu-id="7739e-107">Obtenha um recurso de exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="7739e-107">Get a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="7739e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7739e-108">Syntax</span></span>


```C++
HRESULT GetDepthStencil(
   ID3D11DepthStencilView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="7739e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7739e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7739e-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="7739e-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="7739e-111">Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="7739e-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="7739e-112">O endereço de um ponteiro para uma interface de exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="7739e-112">The address of a pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="7739e-113">Consulte [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="7739e-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7739e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7739e-114">Return value</span></span>

<span data-ttu-id="7739e-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7739e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7739e-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7739e-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7739e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7739e-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7739e-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="7739e-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7739e-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="7739e-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7739e-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7739e-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7739e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7739e-121">Requirements</span></span>



| <span data-ttu-id="7739e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7739e-122">Requirement</span></span> | <span data-ttu-id="7739e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7739e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7739e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7739e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7739e-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7739e-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7739e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7739e-126">Library</span></span><br/> | <dl> <span data-ttu-id="7739e-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="7739e-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7739e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7739e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7739e-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="7739e-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





