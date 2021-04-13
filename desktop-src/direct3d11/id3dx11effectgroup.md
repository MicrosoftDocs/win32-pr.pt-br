---
title: Interface ID3DX11EffectGroup (D3dx11effect. h)
description: A interface ID3DX11EffectGroup acessa um grupo de efeitos. O tempo de vida de um objeto ID3DX11EffectGroup é igual ao tempo de vida de seu objeto ID3DX11Effect pai.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Interface ID3DX11EffectGroup Direct3D 11
- Interface ID3DX11EffectGroup Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968608"
---
# <a name="id3dx11effectgroup-interface"></a><span data-ttu-id="361b8-105">Interface ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="361b8-105">ID3DX11EffectGroup interface</span></span>

<span data-ttu-id="361b8-106">A interface **ID3DX11EffectGroup** acessa um grupo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="361b8-106">The **ID3DX11EffectGroup** interface accesses an Effect group.</span></span>

<span data-ttu-id="361b8-107">O tempo de vida de um objeto **ID3DX11EffectGroup** é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.</span><span class="sxs-lookup"><span data-stu-id="361b8-107">The lifetime of an **ID3DX11EffectGroup** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="361b8-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="361b8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="361b8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="361b8-109">Methods</span></span>

<span data-ttu-id="361b8-110">A interface **ID3DX11EffectGroup** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="361b8-110">The **ID3DX11EffectGroup** interface has these methods.</span></span>



| <span data-ttu-id="361b8-111">Método</span><span class="sxs-lookup"><span data-stu-id="361b8-111">Method</span></span>                                                                  | <span data-ttu-id="361b8-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="361b8-112">Description</span></span>                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="361b8-113">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="361b8-113">**GetAnnotationByIndex**</span></span>](id3dx11effectgroup-getannotationbyindex.md) | <span data-ttu-id="361b8-114">Obter uma anotação por índice.</span><span class="sxs-lookup"><span data-stu-id="361b8-114">Get an annotation by index.</span></span><br/>                        |
| [<span data-ttu-id="361b8-115">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="361b8-115">**GetAnnotationByName**</span></span>](id3dx11effectgroup-getannotationbyname.md)   | <span data-ttu-id="361b8-116">Obter uma anotação por nome.</span><span class="sxs-lookup"><span data-stu-id="361b8-116">Get an annotation by name.</span></span><br/>                         |
| [<span data-ttu-id="361b8-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="361b8-117">**GetDesc**</span></span>](id3dx11effectgroup-getdesc.md)                           | <span data-ttu-id="361b8-118">Obtém uma descrição do grupo.</span><span class="sxs-lookup"><span data-stu-id="361b8-118">Gets a group description.</span></span><br/>                          |
| [<span data-ttu-id="361b8-119">**GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="361b8-119">**GetTechniqueByIndex**</span></span>](id3dx11effectgroup-gettechniquebyindex.md)   | <span data-ttu-id="361b8-120">Obtenha uma técnica por índice.</span><span class="sxs-lookup"><span data-stu-id="361b8-120">Get a technique by index.</span></span><br/>                          |
| [<span data-ttu-id="361b8-121">**GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="361b8-121">**GetTechniqueByName**</span></span>](id3dx11effectgroup-gettechniquebyname.md)     | <span data-ttu-id="361b8-122">Obtenha uma técnica por nome.</span><span class="sxs-lookup"><span data-stu-id="361b8-122">Get a technique by name.</span></span><br/>                           |
| [<span data-ttu-id="361b8-123">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="361b8-123">**IsValid**</span></span>](id3dx11effectgroup-isvalid.md)                           | <span data-ttu-id="361b8-124">Teste um efeito para ver se ele contém uma sintaxe válida.</span><span class="sxs-lookup"><span data-stu-id="361b8-124">Test an effect to see if it contains valid syntax.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="361b8-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="361b8-125">Remarks</span></span>

<span data-ttu-id="361b8-126">Para obter uma interface **ID3DX11EffectGroup** , chame um método como [**ID3DX11Effect:: getgroupbyname**](id3dx11effect-getgroupbyname.md).</span><span class="sxs-lookup"><span data-stu-id="361b8-126">To get an **ID3DX11EffectGroup** interface, call a method like [**ID3DX11Effect::GetGroupByName**](id3dx11effect-getgroupbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="361b8-127">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="361b8-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="361b8-128">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="361b8-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="361b8-129">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="361b8-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="361b8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="361b8-130">Requirements</span></span>



| <span data-ttu-id="361b8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="361b8-131">Requirement</span></span> | <span data-ttu-id="361b8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="361b8-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="361b8-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="361b8-133">Header</span></span><br/>  | <dl> <span data-ttu-id="361b8-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="361b8-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="361b8-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="361b8-135">Library</span></span><br/> | <dl> <span data-ttu-id="361b8-136"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="361b8-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="361b8-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="361b8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="361b8-138">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="361b8-138">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="361b8-139">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="361b8-139">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





