---
title: Método ID3DX11EffectVariable GetAnnotationByIndex (D3dx11effect. h)
description: Obter uma anotação por índice. | Método ID3DX11EffectVariable GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: fc130098-0269-4c78-bc45-284aa0b77865
keywords:
- Método GetAnnotationByIndex Direct3D 11
- Método GetAnnotationByIndex Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e13cfcb27e94c64af132e5eec600941d0b41cd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091943"
---
# <a name="id3dx11effectvariablegetannotationbyindex-method"></a><span data-ttu-id="de3bf-107">Método ID3DX11EffectVariable:: GetAnnotationByIndex</span><span class="sxs-lookup"><span data-stu-id="de3bf-107">ID3DX11EffectVariable::GetAnnotationByIndex method</span></span>

<span data-ttu-id="de3bf-108">Obter uma anotação por índice.</span><span class="sxs-lookup"><span data-stu-id="de3bf-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="de3bf-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de3bf-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="de3bf-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de3bf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3bf-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="de3bf-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="de3bf-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="de3bf-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="de3bf-113">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="de3bf-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de3bf-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de3bf-114">Return value</span></span>

<span data-ttu-id="de3bf-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="de3bf-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="de3bf-116">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="de3bf-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="de3bf-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="de3bf-117">Remarks</span></span>

<span data-ttu-id="de3bf-118">Annonations pode ser anexado a uma técnica, uma passagem ou uma variável global.</span><span class="sxs-lookup"><span data-stu-id="de3bf-118">Annonations can be attached to a technique, a pass, or a global variable.</span></span>

> [!Note]  
> <span data-ttu-id="de3bf-119">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="de3bf-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="de3bf-120">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="de3bf-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="de3bf-121">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="de3bf-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de3bf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de3bf-122">Requirements</span></span>



| <span data-ttu-id="de3bf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="de3bf-123">Requirement</span></span> | <span data-ttu-id="de3bf-124">Valor</span><span class="sxs-lookup"><span data-stu-id="de3bf-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3bf-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de3bf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="de3bf-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="de3bf-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="de3bf-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de3bf-127">Library</span></span><br/> | <dl> <span data-ttu-id="de3bf-128"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="de3bf-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de3bf-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="de3bf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3bf-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="de3bf-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

