---
title: Método ID3DX11EffectType GetMemberTypeByName (D3dx11effect. h)
description: Obter um tipo de membro por nome.
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- Método GetMemberTypeByName Direct3D 11
- Método GetMemberTypeByName Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, método GetMemberTypeByName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e573bcdc2dc4470e87539a307cdc38b71a6320ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989288"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a><span data-ttu-id="278c8-106">Método ID3DX11EffectType:: GetMemberTypeByName</span><span class="sxs-lookup"><span data-stu-id="278c8-106">ID3DX11EffectType::GetMemberTypeByName method</span></span>

<span data-ttu-id="278c8-107">Obter um tipo de membro por nome.</span><span class="sxs-lookup"><span data-stu-id="278c8-107">Get an member type by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="278c8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="278c8-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="278c8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="278c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="278c8-110">*Nome*</span><span class="sxs-lookup"><span data-stu-id="278c8-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="278c8-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="278c8-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="278c8-112">O nome de um membro.</span><span class="sxs-lookup"><span data-stu-id="278c8-112">A member's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="278c8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="278c8-113">Return value</span></span>

<span data-ttu-id="278c8-114">Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="278c8-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="278c8-115">Um ponteiro para um [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="278c8-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="278c8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="278c8-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="278c8-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="278c8-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="278c8-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="278c8-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="278c8-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="278c8-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="278c8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="278c8-120">Requirements</span></span>



| <span data-ttu-id="278c8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="278c8-121">Requirement</span></span> | <span data-ttu-id="278c8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="278c8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="278c8-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="278c8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="278c8-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="278c8-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="278c8-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="278c8-125">Library</span></span><br/> | <dl> <span data-ttu-id="278c8-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="278c8-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="278c8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="278c8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="278c8-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="278c8-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

