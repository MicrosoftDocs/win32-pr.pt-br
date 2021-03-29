---
title: Interface ID3DX11EffectTechnique (D3dx11effect. h)
description: Uma interface ID3DX11EffectTechnique é uma coleção de passagens. O tempo de vida de um objeto ID3DX11EffectTechnique é igual ao tempo de vida de seu objeto ID3DX11Effect pai.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- Interface ID3DX11EffectTechnique Direct3D 11
- Interface ID3DX11EffectTechnique Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968688"
---
# <a name="id3dx11effecttechnique-interface"></a><span data-ttu-id="08428-105">Interface ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="08428-105">ID3DX11EffectTechnique interface</span></span>

<span data-ttu-id="08428-106">Uma interface **ID3DX11EffectTechnique** é uma coleção de passagens.</span><span class="sxs-lookup"><span data-stu-id="08428-106">An **ID3DX11EffectTechnique** interface is a collection of passes.</span></span>

<span data-ttu-id="08428-107">O tempo de vida de um objeto **ID3DX11EffectTechnique** é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.</span><span class="sxs-lookup"><span data-stu-id="08428-107">The lifetime of an **ID3DX11EffectTechnique** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="08428-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="08428-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="08428-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="08428-109">Methods</span></span>

<span data-ttu-id="08428-110">A interface **ID3DX11EffectTechnique** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="08428-110">The **ID3DX11EffectTechnique** interface has these methods.</span></span>



| <span data-ttu-id="08428-111">Método</span><span class="sxs-lookup"><span data-stu-id="08428-111">Method</span></span>                                                                        | <span data-ttu-id="08428-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="08428-112">Description</span></span>                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="08428-113">**ComputeStateBlockMask**</span><span class="sxs-lookup"><span data-stu-id="08428-113">**ComputeStateBlockMask**</span></span>](id3dx11effecttechnique-computestateblockmask.md) | <span data-ttu-id="08428-114">Compute uma máscara de bloco de estado para permitir/impedir alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="08428-114">Compute a state-block mask to allow/prevent state changes.</span></span><br/> |
| [<span data-ttu-id="08428-115">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="08428-115">**GetAnnotationByIndex**</span></span>](id3dx11effecttechnique-getannotationbyindex.md)   | <span data-ttu-id="08428-116">Obter uma anotação por índice.</span><span class="sxs-lookup"><span data-stu-id="08428-116">Get an annotation by index.</span></span><br/>                                |
| [<span data-ttu-id="08428-117">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="08428-117">**GetAnnotationByName**</span></span>](id3dx11effecttechnique-getannotationbyname.md)     | <span data-ttu-id="08428-118">Obter uma anotação por nome.</span><span class="sxs-lookup"><span data-stu-id="08428-118">Get an annotation by name.</span></span><br/>                                 |
| [<span data-ttu-id="08428-119">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="08428-119">**GetDesc**</span></span>](id3dx11effecttechnique-getdesc.md)                             | <span data-ttu-id="08428-120">Obtenha uma descrição técnica.</span><span class="sxs-lookup"><span data-stu-id="08428-120">Get a technique description.</span></span><br/>                               |
| [<span data-ttu-id="08428-121">**GetPassByIndex**</span><span class="sxs-lookup"><span data-stu-id="08428-121">**GetPassByIndex**</span></span>](id3dx11effecttechnique-getpassbyindex.md)               | <span data-ttu-id="08428-122">Obter uma passagem por índice.</span><span class="sxs-lookup"><span data-stu-id="08428-122">Get a pass by index.</span></span><br/>                                       |
| [<span data-ttu-id="08428-123">**GetPassByName**</span><span class="sxs-lookup"><span data-stu-id="08428-123">**GetPassByName**</span></span>](id3dx11effecttechnique-getpassbyname.md)                 | <span data-ttu-id="08428-124">Obter uma passagem por nome.</span><span class="sxs-lookup"><span data-stu-id="08428-124">Get a pass by name.</span></span><br/>                                        |
| [<span data-ttu-id="08428-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="08428-125">**IsValid**</span></span>](id3dx11effecttechnique-isvalid.md)                             | <span data-ttu-id="08428-126">Teste uma técnica para ver se ela contém uma sintaxe válida.</span><span class="sxs-lookup"><span data-stu-id="08428-126">Test a technique to see if it contains valid syntax.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="08428-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="08428-127">Remarks</span></span>

<span data-ttu-id="08428-128">Um efeito contém uma ou mais técnicas; cada técnica contém uma ou mais passagens; cada passagem contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="08428-128">An effect contains one or more techniques; each technique contains one or more passes; each pass contains state assignments.</span></span>

<span data-ttu-id="08428-129">Para obter uma interface de técnica de efeito, chame um método como [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).</span><span class="sxs-lookup"><span data-stu-id="08428-129">To get an effect-technique interface, call a method such as [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="08428-130">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="08428-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="08428-131">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="08428-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="08428-132">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="08428-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08428-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08428-133">Requirements</span></span>



| <span data-ttu-id="08428-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="08428-134">Requirement</span></span> | <span data-ttu-id="08428-135">Valor</span><span class="sxs-lookup"><span data-stu-id="08428-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08428-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08428-136">Header</span></span><br/>  | <dl> <span data-ttu-id="08428-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="08428-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="08428-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="08428-138">Library</span></span><br/> | <dl> <span data-ttu-id="08428-139"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="08428-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08428-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="08428-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08428-141">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="08428-141">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="08428-142">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="08428-142">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





