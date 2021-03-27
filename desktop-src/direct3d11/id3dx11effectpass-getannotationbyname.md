---
title: Método ID3DX11EffectPass GetAnnotationByName (D3dx11effect. h)
description: Obter uma anotação por nome. | Método ID3DX11EffectPass GetAnnotationByName (D3dx11effect. h)
ms.assetid: b54a4fb0-62c7-4d96-af30-f9ae04ff7dab
keywords:
- Método GetAnnotationByName Direct3D 11
- Método GetAnnotationByName Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, método GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129f1548e7f63c47906ac736cbddb5f6b2548b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930680"
---
# <a name="id3dx11effectpassgetannotationbyname-method"></a><span data-ttu-id="9d558-107">Método ID3DX11EffectPass:: GetAnnotationByName</span><span class="sxs-lookup"><span data-stu-id="9d558-107">ID3DX11EffectPass::GetAnnotationByName method</span></span>

<span data-ttu-id="9d558-108">Obter uma anotação por nome.</span><span class="sxs-lookup"><span data-stu-id="9d558-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d558-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d558-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="9d558-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d558-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d558-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="9d558-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="9d558-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9d558-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9d558-113">O nome da anotação.</span><span class="sxs-lookup"><span data-stu-id="9d558-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d558-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d558-114">Return value</span></span>

<span data-ttu-id="9d558-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d558-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="9d558-116">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="9d558-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d558-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d558-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9d558-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="9d558-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9d558-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="9d558-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9d558-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9d558-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9d558-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d558-121">Requirements</span></span>



| <span data-ttu-id="9d558-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d558-122">Requirement</span></span> | <span data-ttu-id="9d558-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9d558-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d558-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d558-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9d558-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d558-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9d558-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d558-126">Library</span></span><br/> | <dl> <span data-ttu-id="9d558-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="9d558-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d558-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d558-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d558-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="9d558-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

