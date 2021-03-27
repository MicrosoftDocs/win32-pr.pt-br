---
title: Método ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect. h)
description: Obter uma anotação por nome. | Método ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect. h)
ms.assetid: 3a9e1fa7-4586-42d6-a723-3140f29a01b4
keywords:
- Método GetAnnotationByName Direct3D 11
- Método GetAnnotationByName Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, método GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae5a7c24d392bd034dfcd69fb67723c9492f982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298674"
---
# <a name="id3dx11effecttechniquegetannotationbyname-method"></a><span data-ttu-id="13fb1-107">Método ID3DX11EffectTechnique:: GetAnnotationByName</span><span class="sxs-lookup"><span data-stu-id="13fb1-107">ID3DX11EffectTechnique::GetAnnotationByName method</span></span>

<span data-ttu-id="13fb1-108">Obter uma anotação por nome.</span><span class="sxs-lookup"><span data-stu-id="13fb1-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="13fb1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13fb1-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="13fb1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13fb1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13fb1-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="13fb1-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="13fb1-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="13fb1-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="13fb1-113">Nome da anotação.</span><span class="sxs-lookup"><span data-stu-id="13fb1-113">Name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13fb1-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13fb1-114">Return value</span></span>

<span data-ttu-id="13fb1-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="13fb1-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="13fb1-116">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="13fb1-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="13fb1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="13fb1-117">Remarks</span></span>

<span data-ttu-id="13fb1-118">Use uma anotação para anexar uma parte dos metadados a uma técnica.</span><span class="sxs-lookup"><span data-stu-id="13fb1-118">Use an annotation to attach a piece of metadata to a technique.</span></span>

> [!Note]  
> <span data-ttu-id="13fb1-119">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="13fb1-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="13fb1-120">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="13fb1-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="13fb1-121">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="13fb1-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="13fb1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13fb1-122">Requirements</span></span>



| <span data-ttu-id="13fb1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="13fb1-123">Requirement</span></span> | <span data-ttu-id="13fb1-124">Valor</span><span class="sxs-lookup"><span data-stu-id="13fb1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13fb1-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="13fb1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="13fb1-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="13fb1-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="13fb1-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="13fb1-127">Library</span></span><br/> | <dl> <span data-ttu-id="13fb1-128"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="13fb1-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13fb1-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="13fb1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13fb1-130">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="13fb1-130">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

