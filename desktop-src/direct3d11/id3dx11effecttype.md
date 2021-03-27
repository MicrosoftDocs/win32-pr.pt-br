---
title: Interface ID3DX11EffectType (D3dx11effect. h)
description: A interface ID3DX11EffectType acessa variáveis de efeito por tipo. O tempo de vida de um objeto ID3DX11EffectType é igual ao tempo de vida de seu objeto ID3DX11Effect pai.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- Interface ID3DX11EffectType Direct3D 11
- Interface ID3DX11EffectType Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663983"
---
# <a name="id3dx11effecttype-interface"></a><span data-ttu-id="7deac-105">Interface ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="7deac-105">ID3DX11EffectType interface</span></span>

<span data-ttu-id="7deac-106">A interface **ID3DX11EffectType** acessa variáveis de efeito por tipo.</span><span class="sxs-lookup"><span data-stu-id="7deac-106">The **ID3DX11EffectType** interface accesses effect variables by type.</span></span>

<span data-ttu-id="7deac-107">O tempo de vida de um objeto **ID3DX11EffectType** é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.</span><span class="sxs-lookup"><span data-stu-id="7deac-107">The lifetime of an **ID3DX11EffectType** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="7deac-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7deac-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7deac-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7deac-109">Methods</span></span>

<span data-ttu-id="7deac-110">A interface **ID3DX11EffectType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7deac-110">The **ID3DX11EffectType** interface has these methods.</span></span>



| <span data-ttu-id="7deac-111">Método</span><span class="sxs-lookup"><span data-stu-id="7deac-111">Method</span></span>                                                                       | <span data-ttu-id="7deac-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7deac-112">Description</span></span>                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="7deac-113">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="7deac-113">**GetDesc**</span></span>](id3dx11effecttype-getdesc.md)                                 | <span data-ttu-id="7deac-114">Obter uma descrição do tipo de efeito.</span><span class="sxs-lookup"><span data-stu-id="7deac-114">Get an effect-type description.</span></span><br/>        |
| [<span data-ttu-id="7deac-115">**GetMemberName**</span><span class="sxs-lookup"><span data-stu-id="7deac-115">**GetMemberName**</span></span>](id3dx11effecttype-getmembername.md)                     | <span data-ttu-id="7deac-116">Obter o nome de um membro.</span><span class="sxs-lookup"><span data-stu-id="7deac-116">Get the name of a member.</span></span><br/>              |
| [<span data-ttu-id="7deac-117">**GetMemberSemantic**</span><span class="sxs-lookup"><span data-stu-id="7deac-117">**GetMemberSemantic**</span></span>](id3dx11effecttype-getmembersemantic.md)             | <span data-ttu-id="7deac-118">Obter a semântica anexada a um membro.</span><span class="sxs-lookup"><span data-stu-id="7deac-118">Get the semantic attached to a member.</span></span><br/> |
| [<span data-ttu-id="7deac-119">**GetMemberTypeByIndex**</span><span class="sxs-lookup"><span data-stu-id="7deac-119">**GetMemberTypeByIndex**</span></span>](id3dx11effecttype-getmembertypebyindex.md)       | <span data-ttu-id="7deac-120">Obter um tipo de membro por índice.</span><span class="sxs-lookup"><span data-stu-id="7deac-120">Get a member type by index.</span></span><br/>            |
| [<span data-ttu-id="7deac-121">**GetMemberTypeByName**</span><span class="sxs-lookup"><span data-stu-id="7deac-121">**GetMemberTypeByName**</span></span>](id3dx11effecttype-getmembertypebyname.md)         | <span data-ttu-id="7deac-122">Obter um tipo de membro por nome.</span><span class="sxs-lookup"><span data-stu-id="7deac-122">Get an member type by name.</span></span><br/>            |
| [<span data-ttu-id="7deac-123">**GetMemberTypeBySemantic**</span><span class="sxs-lookup"><span data-stu-id="7deac-123">**GetMemberTypeBySemantic**</span></span>](id3dx11effecttype-getmembertypebysemantic.md) | <span data-ttu-id="7deac-124">Obter um tipo de membro por semântica.</span><span class="sxs-lookup"><span data-stu-id="7deac-124">Get a member type by semantic.</span></span><br/>         |
| [<span data-ttu-id="7deac-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="7deac-125">**IsValid**</span></span>](id3dx11effecttype-isvalid.md)                                 | <span data-ttu-id="7deac-126">Testa se o tipo de efeito é válido.</span><span class="sxs-lookup"><span data-stu-id="7deac-126">Tests that the effect type is valid.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="7deac-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="7deac-127">Remarks</span></span>

<span data-ttu-id="7deac-128">Para obter informações sobre um tipo de efeito de uma variável de efeito, chame [**ID3DX11EffectVariable:: GetType**](id3dx11effectvariable-gettype.md).</span><span class="sxs-lookup"><span data-stu-id="7deac-128">To get information about an effect type from an effect variable, call [**ID3DX11EffectVariable::GetType**](id3dx11effectvariable-gettype.md).</span></span>

> [!Note]  
> <span data-ttu-id="7deac-129">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="7deac-129">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7deac-130">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="7deac-130">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7deac-131">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7deac-131">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7deac-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7deac-132">Requirements</span></span>



| <span data-ttu-id="7deac-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7deac-133">Requirement</span></span> | <span data-ttu-id="7deac-134">Valor</span><span class="sxs-lookup"><span data-stu-id="7deac-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7deac-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7deac-135">Header</span></span><br/>  | <dl> <span data-ttu-id="7deac-136"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7deac-136"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7deac-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7deac-137">Library</span></span><br/> | <dl> <span data-ttu-id="7deac-138"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="7deac-138"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7deac-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="7deac-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7deac-140">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="7deac-140">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="7deac-141">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="7deac-141">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





