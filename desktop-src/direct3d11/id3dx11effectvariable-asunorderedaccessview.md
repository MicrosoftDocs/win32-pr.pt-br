---
title: Método ID3DX11EffectVariable AsUnorderedAccessView (D3dx11effect. h)
description: Obter uma variável de exibição de acesso não ordenado.
ms.assetid: e8b7c104-09f7-4bfb-9980-a5603550b723
keywords:
- Método AsUnorderedAccessView Direct3D 11
- Método AsUnorderedAccessView Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método AsUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b9ce7dbbc99ef16ef3290ec1ba3135a8d2cb05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664118"
---
# <a name="id3dx11effectvariableasunorderedaccessview-method"></a><span data-ttu-id="fa599-106">Método ID3DX11EffectVariable:: AsUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="fa599-106">ID3DX11EffectVariable::AsUnorderedAccessView method</span></span>

<span data-ttu-id="fa599-107">Obter uma variável de exibição de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="fa599-107">Get an unordered-access-view variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa599-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa599-108">Syntax</span></span>


```C++
ID3DX11EffectUnorderedAccessViewVariable* AsUnorderedAccessView();
```



## <a name="parameters"></a><span data-ttu-id="fa599-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa599-109">Parameters</span></span>

<span data-ttu-id="fa599-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fa599-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa599-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa599-111">Return value</span></span>

<span data-ttu-id="fa599-112">Tipo: **[ **ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="fa599-112">Type: **[**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span></span>

<span data-ttu-id="fa599-113">Um ponteiro para uma variável de exibição de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="fa599-113">A pointer to an unordered-access-view variable.</span></span> <span data-ttu-id="fa599-114">Consulte [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span><span class="sxs-lookup"><span data-stu-id="fa599-114">See [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fa599-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa599-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fa599-116">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="fa599-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fa599-117">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="fa599-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fa599-118">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fa599-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fa599-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa599-119">Requirements</span></span>



| <span data-ttu-id="fa599-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa599-120">Requirement</span></span> | <span data-ttu-id="fa599-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fa599-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa599-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa599-122">Header</span></span><br/>  | <dl> <span data-ttu-id="fa599-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa599-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fa599-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa599-124">Library</span></span><br/> | <dl> <span data-ttu-id="fa599-125"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="fa599-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa599-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa599-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa599-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="fa599-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





