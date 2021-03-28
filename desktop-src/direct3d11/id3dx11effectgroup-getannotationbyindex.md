---
title: Método ID3DX11EffectGroup GetAnnotationByIndex (D3dx11effect. h)
description: Obter uma anotação por índice. | Método ID3DX11EffectGroup GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: 9d3a54b1-384b-4ed4-96a3-09d6bacafda1
keywords:
- Método GetAnnotationByIndex Direct3D 11
- Método GetAnnotationByIndex Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, método GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663dc8d487552dba521c8e47f9a1eecf6db38122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173090"
---
# <a name="id3dx11effectgroupgetannotationbyindex-method"></a><span data-ttu-id="35584-107">Método ID3DX11EffectGroup:: GetAnnotationByIndex</span><span class="sxs-lookup"><span data-stu-id="35584-107">ID3DX11EffectGroup::GetAnnotationByIndex method</span></span>

<span data-ttu-id="35584-108">Obter uma anotação por índice.</span><span class="sxs-lookup"><span data-stu-id="35584-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="35584-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35584-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="35584-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35584-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35584-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="35584-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="35584-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35584-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="35584-113">Índice da anotação.</span><span class="sxs-lookup"><span data-stu-id="35584-113">Index of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35584-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35584-114">Return value</span></span>

<span data-ttu-id="35584-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="35584-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="35584-116">Ponteiro para uma interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) .</span><span class="sxs-lookup"><span data-stu-id="35584-116">Pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="35584-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="35584-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="35584-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="35584-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="35584-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="35584-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="35584-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="35584-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="35584-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35584-121">Requirements</span></span>



| <span data-ttu-id="35584-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="35584-122">Requirement</span></span> | <span data-ttu-id="35584-123">Valor</span><span class="sxs-lookup"><span data-stu-id="35584-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35584-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35584-124">Header</span></span><br/>  | <dl> <span data-ttu-id="35584-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="35584-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="35584-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35584-126">Library</span></span><br/> | <dl> <span data-ttu-id="35584-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="35584-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35584-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="35584-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35584-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="35584-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

