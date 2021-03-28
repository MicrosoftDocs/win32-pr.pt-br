---
title: Método ID3DX11Effect GetGroupByIndex (D3dx11effect. h)
description: Obtém um grupo de efeitos por índice.
ms.assetid: b38ecdbf-0920-48ff-a599-9629a3581d75
keywords:
- Método GetGroupByIndex Direct3D 11
- Método GetGroupByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetGroupByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd0f629a60255ed28aa5cc426b99198867e0b23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930699"
---
# <a name="id3dx11effectgetgroupbyindex-method"></a><span data-ttu-id="2108c-106">Método ID3DX11Effect:: GetGroupByIndex</span><span class="sxs-lookup"><span data-stu-id="2108c-106">ID3DX11Effect::GetGroupByIndex method</span></span>

<span data-ttu-id="2108c-107">Obtém um grupo de efeitos por índice.</span><span class="sxs-lookup"><span data-stu-id="2108c-107">Gets an effect group by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2108c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2108c-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="2108c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2108c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2108c-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="2108c-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="2108c-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2108c-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2108c-112">Índice do grupo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="2108c-112">Index of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2108c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2108c-113">Return value</span></span>

<span data-ttu-id="2108c-114">Tipo: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="2108c-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="2108c-115">Um ponteiro para uma interface [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="2108c-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="2108c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2108c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2108c-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="2108c-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2108c-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="2108c-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2108c-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2108c-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2108c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2108c-120">Requirements</span></span>



| <span data-ttu-id="2108c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2108c-121">Requirement</span></span> | <span data-ttu-id="2108c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2108c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2108c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2108c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2108c-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2108c-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2108c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2108c-125">Library</span></span><br/> | <dl> <span data-ttu-id="2108c-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="2108c-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2108c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2108c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2108c-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="2108c-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

