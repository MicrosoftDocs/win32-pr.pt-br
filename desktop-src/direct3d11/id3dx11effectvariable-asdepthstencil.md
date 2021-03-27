---
title: Método ID3DX11EffectVariable AsDepthStencil (D3dx11effect. h)
description: Obtenha uma variável de estêncil de profundidade.
ms.assetid: 3526812b-6c43-492e-b529-12f61ecd20e3
keywords:
- Método AsDepthStencil Direct3D 11
- Método AsDepthStencil Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método AsDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 980bd43f51d187252fab1872ba75d04f82820ef8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930642"
---
# <a name="id3dx11effectvariableasdepthstencil-method"></a><span data-ttu-id="7eb68-106">Método ID3DX11EffectVariable:: AsDepthStencil</span><span class="sxs-lookup"><span data-stu-id="7eb68-106">ID3DX11EffectVariable::AsDepthStencil method</span></span>

<span data-ttu-id="7eb68-107">Obtenha uma variável de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="7eb68-107">Get a depth-stencil variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb68-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7eb68-108">Syntax</span></span>


```C++
ID3DX11EffectDepthStencilVariable* AsDepthStencil();
```



## <a name="parameters"></a><span data-ttu-id="7eb68-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7eb68-109">Parameters</span></span>

<span data-ttu-id="7eb68-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7eb68-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7eb68-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7eb68-111">Return value</span></span>

<span data-ttu-id="7eb68-112">Tipo: **[ **ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="7eb68-112">Type: **[**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***</span></span>

<span data-ttu-id="7eb68-113">Um ponteiro para uma variável de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="7eb68-113">A pointer to a depth-stencil variable.</span></span> <span data-ttu-id="7eb68-114">Consulte [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).</span><span class="sxs-lookup"><span data-stu-id="7eb68-114">See [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7eb68-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7eb68-115">Remarks</span></span>

<span data-ttu-id="7eb68-116">AsDepthStencil retorna uma versão da variável de efeito que foi especializada em uma variável de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="7eb68-116">AsDepthStencil returns a version of the effect variable that has been specialized to a depth-stencil variable.</span></span> <span data-ttu-id="7eb68-117">De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="7eb68-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain depth-stencil data.</span></span>

<span data-ttu-id="7eb68-118">Os aplicativos podem testar a validade do objeto retornado chamando [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="7eb68-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="7eb68-119">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="7eb68-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7eb68-120">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="7eb68-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7eb68-121">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7eb68-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7eb68-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eb68-122">Requirements</span></span>



| <span data-ttu-id="7eb68-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eb68-123">Requirement</span></span> | <span data-ttu-id="7eb68-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7eb68-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb68-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7eb68-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7eb68-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7eb68-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7eb68-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7eb68-127">Library</span></span><br/> | <dl> <span data-ttu-id="7eb68-128"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="7eb68-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eb68-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7eb68-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb68-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="7eb68-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





