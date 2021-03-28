---
title: Método ID3DX11EffectType GetMemberSemantic (D3dx11effect. h)
description: Obter a semântica anexada a um membro.
ms.assetid: e0666d4e-7510-4496-849e-a0531238b5f8
keywords:
- Método GetMemberSemantic Direct3D 11
- Método GetMemberSemantic Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, método GetMemberSemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberSemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6255860dc9f7dc5cf12742e6f40b7e5148a3f27c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989294"
---
# <a name="id3dx11effecttypegetmembersemantic-method"></a><span data-ttu-id="d8509-106">Método ID3DX11EffectType:: GetMemberSemantic</span><span class="sxs-lookup"><span data-stu-id="d8509-106">ID3DX11EffectType::GetMemberSemantic method</span></span>

<span data-ttu-id="d8509-107">Obter a semântica anexada a um membro.</span><span class="sxs-lookup"><span data-stu-id="d8509-107">Get the semantic attached to a member.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8509-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8509-108">Syntax</span></span>


```C++
LPCSTR GetMemberSemantic(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="d8509-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8509-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8509-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="d8509-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="d8509-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8509-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8509-112">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="d8509-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8509-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8509-113">Return value</span></span>

<span data-ttu-id="d8509-114">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8509-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8509-115">Uma cadeia de caracteres que contém a semântica.</span><span class="sxs-lookup"><span data-stu-id="d8509-115">A string that contains the semantic.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8509-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8509-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d8509-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="d8509-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d8509-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="d8509-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d8509-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d8509-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d8509-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8509-120">Requirements</span></span>



| <span data-ttu-id="d8509-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8509-121">Requirement</span></span> | <span data-ttu-id="d8509-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d8509-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8509-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8509-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d8509-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8509-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d8509-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8509-125">Library</span></span><br/> | <dl> <span data-ttu-id="d8509-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="d8509-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8509-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8509-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8509-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="d8509-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

