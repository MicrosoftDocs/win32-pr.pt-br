---
title: Método ID3DX11EffectVariable GetMemberByIndex (D3dx11effect. h)
description: Obter um membro de estrutura por índice.
ms.assetid: 256f65aa-5f49-4b83-8dde-ddb6b31c581a
keywords:
- Método GetMemberByIndex Direct3D 11
- Método GetMemberByIndex Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método GetMemberByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4be490251a83907dcd16231d62d492caf05768f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989330"
---
# <a name="id3dx11effectvariablegetmemberbyindex-method"></a><span data-ttu-id="73e63-106">Método ID3DX11EffectVariable:: GetMemberByIndex</span><span class="sxs-lookup"><span data-stu-id="73e63-106">ID3DX11EffectVariable::GetMemberByIndex method</span></span>

<span data-ttu-id="73e63-107">Obter um membro de estrutura por índice.</span><span class="sxs-lookup"><span data-stu-id="73e63-107">Get a structure member by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e63-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73e63-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="73e63-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73e63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73e63-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="73e63-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="73e63-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="73e63-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="73e63-112">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="73e63-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73e63-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73e63-113">Return value</span></span>

<span data-ttu-id="73e63-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="73e63-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="73e63-115">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="73e63-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="73e63-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="73e63-116">Remarks</span></span>

<span data-ttu-id="73e63-117">Se a variável de efeito for uma estrutura, use esse método para pesquisar um membro por índice.</span><span class="sxs-lookup"><span data-stu-id="73e63-117">If the effect variable is an structure, use this method to look up a member by index.</span></span>

> [!Note]  
> <span data-ttu-id="73e63-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="73e63-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="73e63-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="73e63-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="73e63-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="73e63-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73e63-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73e63-121">Requirements</span></span>



| <span data-ttu-id="73e63-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="73e63-122">Requirement</span></span> | <span data-ttu-id="73e63-123">Valor</span><span class="sxs-lookup"><span data-stu-id="73e63-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e63-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73e63-124">Header</span></span><br/>  | <dl> <span data-ttu-id="73e63-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="73e63-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="73e63-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73e63-126">Library</span></span><br/> | <dl> <span data-ttu-id="73e63-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="73e63-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e63-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="73e63-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e63-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="73e63-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

