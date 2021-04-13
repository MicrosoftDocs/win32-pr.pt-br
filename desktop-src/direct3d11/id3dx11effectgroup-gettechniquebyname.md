---
title: Método ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
description: Obtenha uma técnica por nome. | Método ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- Método GetTechniqueByName Direct3D 11
- Método GetTechniqueByName Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, método GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5121f67345ba863d773d8e7a73a5d6fa8b69895
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968612"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a><span data-ttu-id="00ed6-107">Método ID3DX11EffectGroup:: GetTechniqueByName</span><span class="sxs-lookup"><span data-stu-id="00ed6-107">ID3DX11EffectGroup::GetTechniqueByName method</span></span>

<span data-ttu-id="00ed6-108">Obtenha uma técnica por nome.</span><span class="sxs-lookup"><span data-stu-id="00ed6-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ed6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00ed6-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="00ed6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00ed6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ed6-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="00ed6-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="00ed6-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="00ed6-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="00ed6-113">O nome da técnica.</span><span class="sxs-lookup"><span data-stu-id="00ed6-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00ed6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00ed6-114">Return value</span></span>

<span data-ttu-id="00ed6-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="00ed6-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="00ed6-116">Um ponteiro para um [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)ou **NULL** se a técnica não for encontrada.</span><span class="sxs-lookup"><span data-stu-id="00ed6-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md), or **NULL** if the technique is not found.</span></span>

## <a name="remarks"></a><span data-ttu-id="00ed6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="00ed6-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="00ed6-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="00ed6-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="00ed6-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="00ed6-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="00ed6-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="00ed6-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00ed6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00ed6-121">Requirements</span></span>



| <span data-ttu-id="00ed6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="00ed6-122">Requirement</span></span> | <span data-ttu-id="00ed6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="00ed6-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00ed6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00ed6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="00ed6-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="00ed6-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="00ed6-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00ed6-126">Library</span></span><br/> | <dl> <span data-ttu-id="00ed6-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="00ed6-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00ed6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="00ed6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00ed6-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="00ed6-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

