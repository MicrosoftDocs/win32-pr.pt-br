---
title: Método GetElement ID3DX11EffectVariable (D3dx11effect. h)
description: Obter um elemento de matriz.
ms.assetid: 3edf2084-570a-4423-8205-0b94a2a0cfde
keywords:
- Método GetElement, Direct3D 11
- Método GetElement Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método GetElement
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetElement
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b887bb9e4c1d40f4d3eb0d36b9a7b4d2698b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968560"
---
# <a name="id3dx11effectvariablegetelement-method"></a><span data-ttu-id="d809e-106">Método ID3DX11EffectVariable:: GetElement</span><span class="sxs-lookup"><span data-stu-id="d809e-106">ID3DX11EffectVariable::GetElement method</span></span>

<span data-ttu-id="d809e-107">Obter um elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="d809e-107">Get an array element.</span></span>

## <a name="syntax"></a><span data-ttu-id="d809e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d809e-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetElement(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="d809e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d809e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d809e-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="d809e-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="d809e-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d809e-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d809e-112">Um índice de base zero; caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="d809e-112">A zero-based index; otherwise 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d809e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d809e-113">Return value</span></span>

<span data-ttu-id="d809e-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="d809e-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="d809e-115">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="d809e-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d809e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d809e-116">Remarks</span></span>

<span data-ttu-id="d809e-117">Se a variável de efeito for uma matriz, use esse método para retornar um dos elementos.</span><span class="sxs-lookup"><span data-stu-id="d809e-117">If the effect variable is an array, use this method to return one of the elements.</span></span>

> [!Note]  
> <span data-ttu-id="d809e-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="d809e-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d809e-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="d809e-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d809e-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d809e-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d809e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d809e-121">Requirements</span></span>



| <span data-ttu-id="d809e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d809e-122">Requirement</span></span> | <span data-ttu-id="d809e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d809e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d809e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d809e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d809e-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d809e-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d809e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d809e-126">Library</span></span><br/> | <dl> <span data-ttu-id="d809e-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="d809e-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d809e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d809e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d809e-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="d809e-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

