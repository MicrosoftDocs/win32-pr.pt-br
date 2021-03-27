---
title: Método setblendstate ID3DX11EffectBlendVariable (D3dx11effect. h)
description: Define o estado de mesclagem de um efeito.
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- Método setblendstate Direct3D 11
- Método setblendstate Direct3D 11, interface ID3DX11EffectBlendVariable
- Interface ID3DX11EffectBlendVariable Direct3D 11, método setblendstate
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce781f29c521df7b81821cb19a56e6fd3999310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664061"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a><span data-ttu-id="480da-106">Método ID3DX11EffectBlendVariable:: setblendstate</span><span class="sxs-lookup"><span data-stu-id="480da-106">ID3DX11EffectBlendVariable::SetBlendState method</span></span>

<span data-ttu-id="480da-107">Define o estado de mesclagem de um efeito.</span><span class="sxs-lookup"><span data-stu-id="480da-107">Sets an effect's blend-state.</span></span>

## <a name="syntax"></a><span data-ttu-id="480da-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="480da-108">Syntax</span></span>


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a><span data-ttu-id="480da-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="480da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="480da-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="480da-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="480da-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="480da-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="480da-112">Indexe em uma matriz de interfaces de estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="480da-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="480da-113">Se houver apenas uma interface de estado de mesclagem, use 0.</span><span class="sxs-lookup"><span data-stu-id="480da-113">If there is only one blend-state interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="480da-114">*pBlendState*</span><span class="sxs-lookup"><span data-stu-id="480da-114">*pBlendState*</span></span> 
</dt> <dd>

<span data-ttu-id="480da-115">Tipo: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span><span class="sxs-lookup"><span data-stu-id="480da-115">Type: **[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span></span>

<span data-ttu-id="480da-116">Um ponteiro para uma interface [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) que contém o estado de mesclagem a ser definido.</span><span class="sxs-lookup"><span data-stu-id="480da-116">A pointer to an [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) interface containing the blend-state to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="480da-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="480da-117">Return value</span></span>

<span data-ttu-id="480da-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="480da-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="480da-119">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="480da-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="480da-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="480da-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="480da-121">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="480da-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="480da-122">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="480da-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="480da-123">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="480da-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="480da-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="480da-124">Requirements</span></span>



| <span data-ttu-id="480da-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="480da-125">Requirement</span></span> | <span data-ttu-id="480da-126">Valor</span><span class="sxs-lookup"><span data-stu-id="480da-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="480da-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="480da-127">Header</span></span><br/>  | <dl> <span data-ttu-id="480da-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="480da-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="480da-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="480da-129">Library</span></span><br/> | <dl> <span data-ttu-id="480da-130"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="480da-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="480da-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="480da-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="480da-132">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="480da-132">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

