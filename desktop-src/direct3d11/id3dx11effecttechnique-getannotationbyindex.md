---
title: Método ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect. h)
description: Obter uma anotação por índice. | Método ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: 703663b0-ee00-4686-a038-6c99ce61266b
keywords:
- Método GetAnnotationByIndex Direct3D 11
- Método GetAnnotationByIndex Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, método GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e30712ba38f1360a992a8e409c249a746cca036
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989401"
---
# <a name="id3dx11effecttechniquegetannotationbyindex-method"></a><span data-ttu-id="39317-107">Método ID3DX11EffectTechnique:: GetAnnotationByIndex</span><span class="sxs-lookup"><span data-stu-id="39317-107">ID3DX11EffectTechnique::GetAnnotationByIndex method</span></span>

<span data-ttu-id="39317-108">Obter uma anotação por índice.</span><span class="sxs-lookup"><span data-stu-id="39317-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="39317-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39317-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="39317-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39317-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39317-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="39317-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="39317-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39317-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39317-113">O índice de base zero do ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="39317-113">The zero-based index of the interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39317-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39317-114">Return value</span></span>

<span data-ttu-id="39317-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="39317-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="39317-116">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="39317-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="39317-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="39317-117">Remarks</span></span>

<span data-ttu-id="39317-118">Use uma anotação para anexar uma parte dos metadados a uma técnica.</span><span class="sxs-lookup"><span data-stu-id="39317-118">Use an annotation to attach a piece of metadata to a technique.</span></span>

> [!Note]  
> <span data-ttu-id="39317-119">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="39317-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="39317-120">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="39317-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="39317-121">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="39317-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="39317-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39317-122">Requirements</span></span>



| <span data-ttu-id="39317-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="39317-123">Requirement</span></span> | <span data-ttu-id="39317-124">Valor</span><span class="sxs-lookup"><span data-stu-id="39317-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39317-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39317-125">Header</span></span><br/>  | <dl> <span data-ttu-id="39317-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="39317-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="39317-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39317-127">Library</span></span><br/> | <dl> <span data-ttu-id="39317-128"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="39317-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39317-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="39317-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39317-130">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="39317-130">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

