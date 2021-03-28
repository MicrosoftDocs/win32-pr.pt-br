---
title: Interface ID3DX11EffectClassInstanceVariable (D3dx11effect. h)
description: Acessa uma instância de classe.
ms.assetid: 64bbae01-1b54-4b3c-9115-80d7b8911ff8
keywords:
- Interface ID3DX11EffectClassInstanceVariable Direct3D 11
- Interface ID3DX11EffectClassInstanceVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e8b6c7ca76dd595363fa0cd80753fce0b66b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298846"
---
# <a name="id3dx11effectclassinstancevariable-interface"></a><span data-ttu-id="58d4c-105">Interface ID3DX11EffectClassInstanceVariable</span><span class="sxs-lookup"><span data-stu-id="58d4c-105">ID3DX11EffectClassInstanceVariable interface</span></span>

<span data-ttu-id="58d4c-106">Acessa uma instância de classe.</span><span class="sxs-lookup"><span data-stu-id="58d4c-106">Accesses a class instance.</span></span>

## <a name="members"></a><span data-ttu-id="58d4c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="58d4c-107">Members</span></span>

<span data-ttu-id="58d4c-108">A interface **ID3DX11EffectClassInstanceVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="58d4c-108">The **ID3DX11EffectClassInstanceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="58d4c-109">**ID3DX11EffectClassInstanceVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="58d4c-109">**ID3DX11EffectClassInstanceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="58d4c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="58d4c-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="58d4c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="58d4c-111">Methods</span></span>

<span data-ttu-id="58d4c-112">A interface **ID3DX11EffectClassInstanceVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="58d4c-112">The **ID3DX11EffectClassInstanceVariable** interface has these methods.</span></span>



| <span data-ttu-id="58d4c-113">Método</span><span class="sxs-lookup"><span data-stu-id="58d4c-113">Method</span></span>                                                                          | <span data-ttu-id="58d4c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="58d4c-114">Description</span></span>                       |
|:--------------------------------------------------------------------------------|:----------------------------------|
| [<span data-ttu-id="58d4c-115">**GetClassInstance**</span><span class="sxs-lookup"><span data-stu-id="58d4c-115">**GetClassInstance**</span></span>](id3dx11effectclassinstancevariable-getclassinstance.md) | <span data-ttu-id="58d4c-116">Obtém uma instância de classe.</span><span class="sxs-lookup"><span data-stu-id="58d4c-116">Gets a class instance.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="58d4c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="58d4c-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="58d4c-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="58d4c-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="58d4c-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="58d4c-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="58d4c-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="58d4c-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58d4c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58d4c-121">Requirements</span></span>



| <span data-ttu-id="58d4c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="58d4c-122">Requirement</span></span> | <span data-ttu-id="58d4c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="58d4c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58d4c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58d4c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="58d4c-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="58d4c-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="58d4c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58d4c-126">Library</span></span><br/> | <dl> <span data-ttu-id="58d4c-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="58d4c-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58d4c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="58d4c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d4c-129">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="58d4c-129">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="58d4c-130">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="58d4c-130">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="58d4c-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="58d4c-131">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





