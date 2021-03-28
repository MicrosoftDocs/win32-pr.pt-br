---
title: Método ID3DX11EffectPass GetAnnotationByIndex (D3dx11effect. h)
description: Obter uma anotação por índice. | Método ID3DX11EffectPass GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: 734eeeca-58c2-4f0c-84d1-2898394a03d6
keywords:
- Método GetAnnotationByIndex Direct3D 11
- Método GetAnnotationByIndex Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, método GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afd43a52758e82434a0e0a4161484ea0d4dcc611
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968661"
---
# <a name="id3dx11effectpassgetannotationbyindex-method"></a><span data-ttu-id="95761-107">Método ID3DX11EffectPass:: GetAnnotationByIndex</span><span class="sxs-lookup"><span data-stu-id="95761-107">ID3DX11EffectPass::GetAnnotationByIndex method</span></span>

<span data-ttu-id="95761-108">Obter uma anotação por índice.</span><span class="sxs-lookup"><span data-stu-id="95761-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="95761-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95761-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="95761-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95761-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95761-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="95761-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="95761-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95761-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="95761-113">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="95761-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95761-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95761-114">Return value</span></span>

<span data-ttu-id="95761-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="95761-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="95761-116">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="95761-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95761-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="95761-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95761-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="95761-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="95761-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="95761-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="95761-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="95761-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95761-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95761-121">Requirements</span></span>



| <span data-ttu-id="95761-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="95761-122">Requirement</span></span> | <span data-ttu-id="95761-123">Valor</span><span class="sxs-lookup"><span data-stu-id="95761-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95761-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95761-124">Header</span></span><br/>  | <dl> <span data-ttu-id="95761-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="95761-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="95761-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95761-126">Library</span></span><br/> | <dl> <span data-ttu-id="95761-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="95761-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95761-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="95761-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95761-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="95761-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

