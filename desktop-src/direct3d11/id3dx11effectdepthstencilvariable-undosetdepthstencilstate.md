---
title: Método ID3DX11EffectDepthStencilVariable UndoSetDepthStencilState (D3dx11effect. h)
description: Reverte um estado de estêncil de profundidade definido anteriormente.
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- Método UndoSetDepthStencilState Direct3D 11
- Método UndoSetDepthStencilState Direct3D 11, interface ID3DX11EffectDepthStencilVariable
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11, método UndoSetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd44d486d2613406617f0534046c54818267dd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989382"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a><span data-ttu-id="e86da-106">Método ID3DX11EffectDepthStencilVariable:: UndoSetDepthStencilState</span><span class="sxs-lookup"><span data-stu-id="e86da-106">ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState method</span></span>

<span data-ttu-id="e86da-107">Reverte um estado de estêncil de profundidade definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e86da-107">Reverts a previously set depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e86da-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e86da-108">Syntax</span></span>


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="e86da-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e86da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e86da-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="e86da-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="e86da-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e86da-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e86da-112">Indexe em uma matriz de interfaces de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e86da-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="e86da-113">Se houver apenas uma interface de estêncil de profundidade, use 0.</span><span class="sxs-lookup"><span data-stu-id="e86da-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e86da-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e86da-114">Return value</span></span>

<span data-ttu-id="e86da-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e86da-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e86da-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e86da-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e86da-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e86da-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e86da-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="e86da-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e86da-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="e86da-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e86da-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e86da-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e86da-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e86da-121">Requirements</span></span>



| <span data-ttu-id="e86da-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e86da-122">Requirement</span></span> | <span data-ttu-id="e86da-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e86da-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e86da-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e86da-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e86da-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e86da-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e86da-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e86da-126">Library</span></span><br/> | <dl> <span data-ttu-id="e86da-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="e86da-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e86da-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e86da-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86da-129">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="e86da-129">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

