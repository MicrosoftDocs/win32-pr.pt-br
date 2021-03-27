---
title: Método ID3DX11EffectVariable GetAnnotationByName (D3dx11effect. h)
description: Obter uma anotação por nome. | Método ID3DX11EffectVariable GetAnnotationByName (D3dx11effect. h)
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- Método GetAnnotationByName Direct3D 11
- Método GetAnnotationByName Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37efcd773728e563a4112f61a7c6c965d05bad4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298673"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a><span data-ttu-id="ebe9c-107">Método ID3DX11EffectVariable:: GetAnnotationByName</span><span class="sxs-lookup"><span data-stu-id="ebe9c-107">ID3DX11EffectVariable::GetAnnotationByName method</span></span>

<span data-ttu-id="ebe9c-108">Obter uma anotação por nome.</span><span class="sxs-lookup"><span data-stu-id="ebe9c-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe9c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebe9c-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="ebe9c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebe9c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebe9c-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="ebe9c-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="ebe9c-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ebe9c-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ebe9c-113">O nome da anotação.</span><span class="sxs-lookup"><span data-stu-id="ebe9c-113">The annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebe9c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebe9c-114">Return value</span></span>

<span data-ttu-id="ebe9c-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="ebe9c-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="ebe9c-116">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="ebe9c-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="ebe9c-117">Observe que, se a anotação não for encontrada, o **ID3DX11EffectVariable** retornado estará vazio.</span><span class="sxs-lookup"><span data-stu-id="ebe9c-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="ebe9c-118">O método [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md) deve ser chamado para determinar se a anotação foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="ebe9c-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebe9c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebe9c-119">Remarks</span></span>

<span data-ttu-id="ebe9c-120">Annonations pode ser anexado a uma técnica, uma passagem ou uma variável global.</span><span class="sxs-lookup"><span data-stu-id="ebe9c-120">Annonations can be attached to a technique, a pass, or a global variable.</span></span>

> [!Note]  
> <span data-ttu-id="ebe9c-121">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="ebe9c-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ebe9c-122">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="ebe9c-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ebe9c-123">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ebe9c-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ebe9c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebe9c-124">Requirements</span></span>



| <span data-ttu-id="ebe9c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebe9c-125">Requirement</span></span> | <span data-ttu-id="ebe9c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ebe9c-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe9c-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ebe9c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ebe9c-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebe9c-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ebe9c-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ebe9c-129">Library</span></span><br/> | <dl> <span data-ttu-id="ebe9c-130"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe9c-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe9c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebe9c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe9c-132">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="ebe9c-132">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

