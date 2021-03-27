---
title: Método GetMemberName de ID3DX11EffectType (D3dx11effect. h)
description: Obter o nome de um membro.
ms.assetid: cd231741-09e1-4e69-9384-5cdfbf83fc8b
keywords:
- Método GetMemberName Direct3D 11
- Método GetMemberName Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, método GetMemberName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4aa9a24067d8ef19680ca58e41659da850659b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298683"
---
# <a name="id3dx11effecttypegetmembername-method"></a><span data-ttu-id="45965-106">Método ID3DX11EffectType:: GetMemberName</span><span class="sxs-lookup"><span data-stu-id="45965-106">ID3DX11EffectType::GetMemberName method</span></span>

<span data-ttu-id="45965-107">Obter o nome de um membro.</span><span class="sxs-lookup"><span data-stu-id="45965-107">Get the name of a member.</span></span>

## <a name="syntax"></a><span data-ttu-id="45965-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45965-108">Syntax</span></span>


```C++
LPCSTR GetMemberName(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="45965-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45965-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45965-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="45965-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="45965-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="45965-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="45965-112">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="45965-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45965-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45965-113">Return value</span></span>

<span data-ttu-id="45965-114">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="45965-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="45965-115">O nome do membro.</span><span class="sxs-lookup"><span data-stu-id="45965-115">The name of the member.</span></span>

## <a name="remarks"></a><span data-ttu-id="45965-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="45965-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="45965-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="45965-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="45965-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="45965-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="45965-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="45965-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="45965-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45965-120">Requirements</span></span>



| <span data-ttu-id="45965-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="45965-121">Requirement</span></span> | <span data-ttu-id="45965-122">Valor</span><span class="sxs-lookup"><span data-stu-id="45965-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45965-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45965-123">Header</span></span><br/>  | <dl> <span data-ttu-id="45965-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="45965-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="45965-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45965-125">Library</span></span><br/> | <dl> <span data-ttu-id="45965-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="45965-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45965-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="45965-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45965-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="45965-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

