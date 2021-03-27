---
title: Método ID3DX11EffectType GetMemberTypeByIndex (D3dx11effect. h)
description: Obter um tipo de membro por índice.
ms.assetid: 6421f08f-0236-4d8f-b3c2-ef7ec5ffe2a1
keywords:
- Método GetMemberTypeByIndex Direct3D 11
- Método GetMemberTypeByIndex Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, método GetMemberTypeByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5023e064539f57af9998c788385f2a1316433f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506499"
---
# <a name="id3dx11effecttypegetmembertypebyindex-method"></a><span data-ttu-id="c3d34-106">Método ID3DX11EffectType:: GetMemberTypeByIndex</span><span class="sxs-lookup"><span data-stu-id="c3d34-106">ID3DX11EffectType::GetMemberTypeByIndex method</span></span>

<span data-ttu-id="c3d34-107">Obter um tipo de membro por índice.</span><span class="sxs-lookup"><span data-stu-id="c3d34-107">Get a member type by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d34-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3d34-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="c3d34-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3d34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3d34-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c3d34-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c3d34-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3d34-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3d34-112">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="c3d34-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3d34-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3d34-113">Return value</span></span>

<span data-ttu-id="c3d34-114">Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3d34-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="c3d34-115">Um ponteiro para um [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="c3d34-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3d34-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3d34-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c3d34-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="c3d34-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c3d34-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="c3d34-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c3d34-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c3d34-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c3d34-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3d34-120">Requirements</span></span>



| <span data-ttu-id="c3d34-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3d34-121">Requirement</span></span> | <span data-ttu-id="c3d34-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c3d34-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d34-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3d34-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c3d34-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3d34-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c3d34-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3d34-125">Library</span></span><br/> | <dl> <span data-ttu-id="c3d34-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d34-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3d34-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3d34-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d34-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="c3d34-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

