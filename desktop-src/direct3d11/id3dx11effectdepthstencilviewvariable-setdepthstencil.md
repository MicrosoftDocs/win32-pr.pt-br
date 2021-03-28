---
title: Método ID3DX11EffectDepthStencilViewVariable SetDepthStencil (D3dx11effect. h)
description: Defina um recurso de exibição de estêncil de profundidade.
ms.assetid: 35cbcd3b-6fc8-448d-a82e-724f91038d07
keywords:
- Método SetDepthStencil Direct3D 11
- Método SetDepthStencil Direct3D 11, interface ID3DX11EffectDepthStencilViewVariable
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, método SetDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 723be51bc769982acf43c19482978bd581cafa13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989325"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencil-method"></a><span data-ttu-id="8df1b-106">Método ID3DX11EffectDepthStencilViewVariable:: SetDepthStencil</span><span class="sxs-lookup"><span data-stu-id="8df1b-106">ID3DX11EffectDepthStencilViewVariable::SetDepthStencil method</span></span>

<span data-ttu-id="8df1b-107">Defina um recurso de exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="8df1b-107">Set a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df1b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8df1b-108">Syntax</span></span>


```C++
HRESULT SetDepthStencil(
   ID3D11DepthStencilView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="8df1b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8df1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df1b-110">*origem*</span><span class="sxs-lookup"><span data-stu-id="8df1b-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="8df1b-111">Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span><span class="sxs-lookup"><span data-stu-id="8df1b-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span></span>

<span data-ttu-id="8df1b-112">Um ponteiro para uma interface de exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="8df1b-112">A pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="8df1b-113">Consulte [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="8df1b-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df1b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8df1b-114">Return value</span></span>

<span data-ttu-id="8df1b-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8df1b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8df1b-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8df1b-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8df1b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8df1b-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8df1b-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="8df1b-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8df1b-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="8df1b-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8df1b-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8df1b-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8df1b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8df1b-121">Requirements</span></span>



| <span data-ttu-id="8df1b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8df1b-122">Requirement</span></span> | <span data-ttu-id="8df1b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8df1b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8df1b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8df1b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8df1b-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8df1b-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8df1b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8df1b-126">Library</span></span><br/> | <dl> <span data-ttu-id="8df1b-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="8df1b-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8df1b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8df1b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df1b-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="8df1b-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





