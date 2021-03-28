---
title: Método ID3DX11EffectVariable GetMemberByName (D3dx11effect. h)
description: Obter um membro da estrutura por nome.
ms.assetid: 09f7f2f8-f55f-411c-8130-6ae44015d58a
keywords:
- Método GetMemberByName Direct3D 11
- Método GetMemberByName Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método GetMemberByName
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9851a2f74502a79b5cc85c494e468c4a346798f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989416"
---
# <a name="id3dx11effectvariablegetmemberbyname-method"></a><span data-ttu-id="16974-106">Método ID3DX11EffectVariable:: GetMemberByName</span><span class="sxs-lookup"><span data-stu-id="16974-106">ID3DX11EffectVariable::GetMemberByName method</span></span>

<span data-ttu-id="16974-107">Obter um membro da estrutura por nome.</span><span class="sxs-lookup"><span data-stu-id="16974-107">Get a structure member by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="16974-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16974-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="16974-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16974-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16974-110">*Nome*</span><span class="sxs-lookup"><span data-stu-id="16974-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="16974-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="16974-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="16974-112">Nome do membro.</span><span class="sxs-lookup"><span data-stu-id="16974-112">Member name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16974-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16974-113">Return value</span></span>

<span data-ttu-id="16974-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="16974-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="16974-115">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="16974-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="16974-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="16974-116">Remarks</span></span>

<span data-ttu-id="16974-117">Se a variável de efeito for uma estrutura, use esse método para pesquisar um membro por nome.</span><span class="sxs-lookup"><span data-stu-id="16974-117">If the effect variable is an structure, use this method to look up a member by name.</span></span>

> [!Note]  
> <span data-ttu-id="16974-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="16974-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="16974-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="16974-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="16974-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="16974-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16974-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16974-121">Requirements</span></span>



| <span data-ttu-id="16974-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="16974-122">Requirement</span></span> | <span data-ttu-id="16974-123">Valor</span><span class="sxs-lookup"><span data-stu-id="16974-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16974-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16974-124">Header</span></span><br/>  | <dl> <span data-ttu-id="16974-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="16974-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="16974-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16974-126">Library</span></span><br/> | <dl> <span data-ttu-id="16974-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="16974-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16974-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="16974-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16974-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="16974-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

