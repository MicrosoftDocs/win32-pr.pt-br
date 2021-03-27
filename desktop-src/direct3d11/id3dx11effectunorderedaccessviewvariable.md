---
title: Interface ID3DX11EffectUnorderedAccessViewVariable (D3dx11effect. h)
description: Acessa uma exibição de acesso não ordenada.
ms.assetid: f78dc8c5-c85a-48cf-b579-f2937aa5ce2a
keywords:
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d48161ad4d9fc1773889fab0e8a0fd9a21ec793e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989272"
---
# <a name="id3dx11effectunorderedaccessviewvariable-interface"></a><span data-ttu-id="926eb-105">Interface ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="926eb-105">ID3DX11EffectUnorderedAccessViewVariable interface</span></span>

<span data-ttu-id="926eb-106">Acessa uma exibição de acesso não ordenada.</span><span class="sxs-lookup"><span data-stu-id="926eb-106">Accesses an unordered access view.</span></span>

## <a name="members"></a><span data-ttu-id="926eb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="926eb-107">Members</span></span>

<span data-ttu-id="926eb-108">A interface **ID3DX11EffectUnorderedAccessViewVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="926eb-108">The **ID3DX11EffectUnorderedAccessViewVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="926eb-109">**ID3DX11EffectUnorderedAccessViewVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="926eb-109">**ID3DX11EffectUnorderedAccessViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="926eb-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="926eb-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="926eb-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="926eb-111">Methods</span></span>

<span data-ttu-id="926eb-112">A interface **ID3DX11EffectUnorderedAccessViewVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="926eb-112">The **ID3DX11EffectUnorderedAccessViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="926eb-113">Método</span><span class="sxs-lookup"><span data-stu-id="926eb-113">Method</span></span>                                                                                                      | <span data-ttu-id="926eb-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="926eb-114">Description</span></span>                                        |
|:------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="926eb-115">**GetUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="926eb-115">**GetUnorderedAccessView**</span></span>](id3dx11effectunorderedaccessviewvariable-getunorderedaccessview.md)           | <span data-ttu-id="926eb-116">Obtenha um modo de exibição de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="926eb-116">Get an unordered-access-view.</span></span><br/>           |
| [<span data-ttu-id="926eb-117">**GetUnorderedAccessViewArray**</span><span class="sxs-lookup"><span data-stu-id="926eb-117">**GetUnorderedAccessViewArray**</span></span>](id3dx11effectunorderedaccessviewvariable-getunorderedaccessviewarray.md) | <span data-ttu-id="926eb-118">Obter uma matriz de exibições de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="926eb-118">Get an array of unordered-access-views.</span></span><br/> |
| [<span data-ttu-id="926eb-119">**SetUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="926eb-119">**SetUnorderedAccessView**</span></span>](id3dx11effectunorderedaccessviewvariable-setunorderedaccessview.md)           | <span data-ttu-id="926eb-120">Defina um modo de exibição de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="926eb-120">Set an unordered-access-view.</span></span><br/>           |
| [<span data-ttu-id="926eb-121">**SetUnorderedAccessViewArray**</span><span class="sxs-lookup"><span data-stu-id="926eb-121">**SetUnorderedAccessViewArray**</span></span>](id3dx11effectunorderedaccessviewvariable-setunorderedaccessviewarray.md) | <span data-ttu-id="926eb-122">Defina uma matriz de modos de exibição de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="926eb-122">Set an array of unordered-access-views.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="926eb-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="926eb-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="926eb-124">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="926eb-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="926eb-125">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="926eb-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="926eb-126">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="926eb-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="926eb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="926eb-127">Requirements</span></span>



| <span data-ttu-id="926eb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="926eb-128">Requirement</span></span> | <span data-ttu-id="926eb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="926eb-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="926eb-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="926eb-130">Header</span></span><br/>  | <dl> <span data-ttu-id="926eb-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="926eb-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="926eb-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="926eb-132">Library</span></span><br/> | <dl> <span data-ttu-id="926eb-133"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="926eb-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="926eb-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="926eb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="926eb-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="926eb-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="926eb-136">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="926eb-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="926eb-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="926eb-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





