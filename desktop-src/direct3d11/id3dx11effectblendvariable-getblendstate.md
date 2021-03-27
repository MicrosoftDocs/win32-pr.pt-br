---
title: Método getblendstate ID3DX11EffectBlendVariable (D3dx11effect. h)
description: Obtenha um ponteiro para uma interface de estado de mesclagem.
ms.assetid: ab4ee765-b5ad-4dc3-9b00-48052528d3bd
keywords:
- Método getblendstate Direct3D 11
- Método getblendstate Direct3D 11, interface ID3DX11EffectBlendVariable
- Interface ID3DX11EffectBlendVariable Direct3D 11, método getblendstate
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48092b496fa8a38be7c9dd8aea67a26e8b56f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298754"
---
# <a name="id3dx11effectblendvariablegetblendstate-method"></a><span data-ttu-id="c4177-106">Método ID3DX11EffectBlendVariable:: getblendstate</span><span class="sxs-lookup"><span data-stu-id="c4177-106">ID3DX11EffectBlendVariable::GetBlendState method</span></span>

<span data-ttu-id="c4177-107">Obtenha um ponteiro para uma interface de estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="c4177-107">Get a pointer to a blend-state interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4177-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4177-108">Syntax</span></span>


```C++
HRESULT GetBlendState(
   UINT             Index,
   ID3D11BlendState **ppBlendState
);
```



## <a name="parameters"></a><span data-ttu-id="c4177-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4177-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4177-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c4177-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c4177-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c4177-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c4177-112">Indexe em uma matriz de interfaces de estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="c4177-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="c4177-113">Se houver apenas uma interface de estado de mesclagem, use 0.</span><span class="sxs-lookup"><span data-stu-id="c4177-113">If there is only one blend-state interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="c4177-114">*ppBlendState*</span><span class="sxs-lookup"><span data-stu-id="c4177-114">*ppBlendState*</span></span> 
</dt> <dd>

<span data-ttu-id="c4177-115">Tipo: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="c4177-115">Type: **[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***</span></span>

<span data-ttu-id="c4177-116">O endereço de um ponteiro para uma interface de estado de mesclagem (consulte [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).</span><span class="sxs-lookup"><span data-stu-id="c4177-116">The address of a pointer to a blend-state interface (see [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4177-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4177-117">Return value</span></span>

<span data-ttu-id="c4177-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4177-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4177-119">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c4177-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4177-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4177-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c4177-121">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="c4177-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c4177-122">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="c4177-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c4177-123">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c4177-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4177-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4177-124">Requirements</span></span>



| <span data-ttu-id="c4177-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4177-125">Requirement</span></span> | <span data-ttu-id="c4177-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c4177-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4177-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4177-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c4177-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4177-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c4177-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4177-129">Library</span></span><br/> | <dl> <span data-ttu-id="c4177-130"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="c4177-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4177-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4177-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4177-132">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="c4177-132">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

