---
title: Método ID3DX11EffectDepthStencilVariable GetDepthStencilState (D3dx11effect. h)
description: Obtenha um ponteiro para uma interface de estêncil de profundidade.
ms.assetid: 3e8f7fc6-960c-45f5-9276-9aa2a5e7a6c9
keywords:
- Método GetDepthStencilState Direct3D 11
- Método GetDepthStencilState Direct3D 11, interface ID3DX11EffectDepthStencilVariable
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11, método GetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9276c7a126d5441361a4d449c4ee2ece70d995
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968667"
---
# <a name="id3dx11effectdepthstencilvariablegetdepthstencilstate-method"></a><span data-ttu-id="ff179-106">Método ID3DX11EffectDepthStencilVariable:: GetDepthStencilState</span><span class="sxs-lookup"><span data-stu-id="ff179-106">ID3DX11EffectDepthStencilVariable::GetDepthStencilState method</span></span>

<span data-ttu-id="ff179-107">Obtenha um ponteiro para uma interface de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="ff179-107">Get a pointer to a depth-stencil interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff179-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff179-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState **ppDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="ff179-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff179-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff179-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="ff179-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="ff179-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ff179-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ff179-112">Indexe em uma matriz de interfaces de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="ff179-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="ff179-113">Se houver apenas uma interface de estêncil de profundidade, use 0.</span><span class="sxs-lookup"><span data-stu-id="ff179-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="ff179-114">*ppDepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="ff179-114">*ppDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="ff179-115">Tipo: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="ff179-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span></span>

<span data-ttu-id="ff179-116">O endereço de um ponteiro para uma interface de estado de mesclagem (consulte [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span><span class="sxs-lookup"><span data-stu-id="ff179-116">The address of a pointer to a blend-state interface (see [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff179-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff179-117">Return value</span></span>

<span data-ttu-id="ff179-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ff179-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ff179-119">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ff179-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ff179-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff179-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ff179-121">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="ff179-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ff179-122">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="ff179-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ff179-123">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ff179-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ff179-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff179-124">Requirements</span></span>



| <span data-ttu-id="ff179-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff179-125">Requirement</span></span> | <span data-ttu-id="ff179-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ff179-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff179-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff179-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ff179-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff179-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ff179-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff179-129">Library</span></span><br/> | <dl> <span data-ttu-id="ff179-130"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="ff179-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff179-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff179-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff179-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="ff179-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

