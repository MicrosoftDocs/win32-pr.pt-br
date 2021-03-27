---
title: Método de ID3DX11EffectVariable asinterface (D3dx11effect. h)
description: Obter uma variável de interface.
ms.assetid: 5b1e5d05-ab36-42c2-9990-154baff5e9a4
keywords:
- Método asinterface Direct3D 11
- Método asinterface Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método asinterface
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsInterface
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0134aceea3202e0965bf05b709d29279be2fc29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663968"
---
# <a name="id3dx11effectvariableasinterface-method"></a><span data-ttu-id="9a22b-106">Método ID3DX11EffectVariable:: asinterface</span><span class="sxs-lookup"><span data-stu-id="9a22b-106">ID3DX11EffectVariable::AsInterface method</span></span>

<span data-ttu-id="9a22b-107">Obter uma variável de interface.</span><span class="sxs-lookup"><span data-stu-id="9a22b-107">Get an interface variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a22b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a22b-108">Syntax</span></span>


```C++
ID3DX11EffectInterfaceVariable* AsInterface();
```



## <a name="parameters"></a><span data-ttu-id="9a22b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a22b-109">Parameters</span></span>

<span data-ttu-id="9a22b-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9a22b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a22b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a22b-111">Return value</span></span>

<span data-ttu-id="9a22b-112">Tipo: **[ **ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a22b-112">Type: **[**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)\***</span></span>

<span data-ttu-id="9a22b-113">Um ponteiro para uma variável de interface.</span><span class="sxs-lookup"><span data-stu-id="9a22b-113">A pointer to an interface variable.</span></span> <span data-ttu-id="9a22b-114">Consulte [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md).</span><span class="sxs-lookup"><span data-stu-id="9a22b-114">See [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a22b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a22b-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9a22b-116">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="9a22b-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9a22b-117">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="9a22b-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9a22b-118">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9a22b-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a22b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a22b-119">Requirements</span></span>



| <span data-ttu-id="9a22b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a22b-120">Requirement</span></span> | <span data-ttu-id="9a22b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9a22b-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a22b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a22b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9a22b-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a22b-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9a22b-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a22b-124">Library</span></span><br/> | <dl> <span data-ttu-id="9a22b-125"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="9a22b-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a22b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a22b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a22b-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="9a22b-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





