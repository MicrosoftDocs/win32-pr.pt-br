---
title: Método ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
description: Obtenha uma técnica por índice. | Método ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: b0962957-20d1-4ec6-9f8e-acc7a62c5f4e
keywords:
- Método GetTechniqueByIndex Direct3D 11
- Método GetTechniqueByIndex Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, método GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe42d71886ae93bdaff7ac956554ff9a97fc9f8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930662"
---
# <a name="id3dx11effectgroupgettechniquebyindex-method"></a><span data-ttu-id="7f265-107">Método ID3DX11EffectGroup:: GetTechniqueByIndex</span><span class="sxs-lookup"><span data-stu-id="7f265-107">ID3DX11EffectGroup::GetTechniqueByIndex method</span></span>

<span data-ttu-id="7f265-108">Obtenha uma técnica por índice.</span><span class="sxs-lookup"><span data-stu-id="7f265-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f265-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f265-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="7f265-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f265-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f265-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="7f265-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="7f265-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7f265-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7f265-113">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="7f265-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f265-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f265-114">Return value</span></span>

<span data-ttu-id="7f265-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f265-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="7f265-116">Um ponteiro para um [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="7f265-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f265-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f265-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7f265-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="7f265-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7f265-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="7f265-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7f265-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7f265-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7f265-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f265-121">Requirements</span></span>



| <span data-ttu-id="7f265-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f265-122">Requirement</span></span> | <span data-ttu-id="7f265-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7f265-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f265-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f265-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7f265-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f265-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7f265-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7f265-126">Library</span></span><br/> | <dl> <span data-ttu-id="7f265-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="7f265-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f265-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f265-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f265-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="7f265-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

