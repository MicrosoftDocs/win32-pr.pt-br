---
title: Método ID3DX11EffectBlendVariable UndoSetBlendState (D3dx11effect. h)
description: Reverte um estado de mesclagem definido anteriormente.
ms.assetid: 375c225b-558f-4ad0-81e7-62eff3e28cf1
keywords:
- Método UndoSetBlendState Direct3D 11
- Método UndoSetBlendState Direct3D 11, interface ID3DX11EffectBlendVariable
- Interface ID3DX11EffectBlendVariable Direct3D 11, método UndoSetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.UndoSetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e117eafa9b6379b2240cf491809c58d8600d840f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989363"
---
# <a name="id3dx11effectblendvariableundosetblendstate-method"></a><span data-ttu-id="8b146-106">Método ID3DX11EffectBlendVariable:: UndoSetBlendState</span><span class="sxs-lookup"><span data-stu-id="8b146-106">ID3DX11EffectBlendVariable::UndoSetBlendState method</span></span>

<span data-ttu-id="8b146-107">Reverte um estado de mesclagem definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8b146-107">Reverts a previously set blend-state.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b146-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b146-108">Syntax</span></span>


```C++
HRESULT UndoSetBlendState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="8b146-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b146-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b146-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="8b146-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="8b146-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8b146-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8b146-112">Indexe em uma matriz de interfaces de estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8b146-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="8b146-113">Se houver apenas uma interface de estado de mesclagem, use 0.</span><span class="sxs-lookup"><span data-stu-id="8b146-113">If there is only one blend-state interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b146-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b146-114">Return value</span></span>

<span data-ttu-id="8b146-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b146-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b146-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8b146-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b146-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b146-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8b146-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="8b146-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8b146-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="8b146-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8b146-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8b146-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b146-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b146-121">Requirements</span></span>



| <span data-ttu-id="8b146-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b146-122">Requirement</span></span> | <span data-ttu-id="8b146-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8b146-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b146-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b146-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8b146-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b146-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8b146-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b146-126">Library</span></span><br/> | <dl> <span data-ttu-id="8b146-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="8b146-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b146-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b146-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b146-129">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="8b146-129">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

