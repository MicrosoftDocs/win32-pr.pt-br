---
title: Interface ID3DX11EffectRasterizerVariable (D3dx11effect. h)
description: Uma interface de variável rasterizadora acessa o estado do rasterizador.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- Interface ID3DX11EffectRasterizerVariable Direct3D 11
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a19c5d529d6134ebad238be6e7c6195dc628a7f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989411"
---
# <a name="id3dx11effectrasterizervariable-interface"></a><span data-ttu-id="828da-105">Interface ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="828da-105">ID3DX11EffectRasterizerVariable interface</span></span>

<span data-ttu-id="828da-106">Uma interface de variável rasterizadora acessa o estado do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="828da-106">A rasterizer-variable interface accesses rasterizer state.</span></span>

## <a name="members"></a><span data-ttu-id="828da-107">Membros</span><span class="sxs-lookup"><span data-stu-id="828da-107">Members</span></span>

<span data-ttu-id="828da-108">A interface **ID3DX11EffectRasterizerVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="828da-108">The **ID3DX11EffectRasterizerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="828da-109">**ID3DX11EffectRasterizerVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="828da-109">**ID3DX11EffectRasterizerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="828da-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="828da-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="828da-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="828da-111">Methods</span></span>

<span data-ttu-id="828da-112">A interface **ID3DX11EffectRasterizerVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="828da-112">The **ID3DX11EffectRasterizerVariable** interface has these methods.</span></span>



| <span data-ttu-id="828da-113">Método</span><span class="sxs-lookup"><span data-stu-id="828da-113">Method</span></span>                                                                                   | <span data-ttu-id="828da-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="828da-114">Description</span></span>                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="828da-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="828da-115">**GetBackingStore**</span></span>](id3dx11effectrasterizervariable-getbackingstore.md)               | <span data-ttu-id="828da-116">Obtenha um ponteiro para uma variável que contém o estado rasteriser.</span><span class="sxs-lookup"><span data-stu-id="828da-116">Get a pointer to a variable that contains rasteriser state.</span></span><br/> |
| [<span data-ttu-id="828da-117">**GetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="828da-117">**GetRasterizerState**</span></span>](id3dx11effectrasterizervariable-getrasterizerstate.md)         | <span data-ttu-id="828da-118">Obter um ponteiro para uma interface do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="828da-118">Get a pointer to a rasterizer interface.</span></span><br/>                    |
| [<span data-ttu-id="828da-119">**SetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="828da-119">**SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)         | <span data-ttu-id="828da-120">Define o estado do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="828da-120">Sets the rasterizer state.</span></span><br/>                                  |
| [<span data-ttu-id="828da-121">**UndoSetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="828da-121">**UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | <span data-ttu-id="828da-122">Reverte um estado de rasterizador definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="828da-122">Reverts a previously set rasterizer state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="828da-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="828da-123">Remarks</span></span>

<span data-ttu-id="828da-124">Uma interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) é criada quando um efeito é lido na memória.</span><span class="sxs-lookup"><span data-stu-id="828da-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="828da-125">As variáveis de efeito são salvas na memória no repositório de backup; Quando uma técnica é aplicada, os valores no repositório de backup são copiados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="828da-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="828da-126">Você pode usar qualquer um desses métodos para retornar o estado.</span><span class="sxs-lookup"><span data-stu-id="828da-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="828da-127">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="828da-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="828da-128">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="828da-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="828da-129">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="828da-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="828da-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="828da-130">Requirements</span></span>



| <span data-ttu-id="828da-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="828da-131">Requirement</span></span> | <span data-ttu-id="828da-132">Valor</span><span class="sxs-lookup"><span data-stu-id="828da-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="828da-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="828da-133">Header</span></span><br/>  | <dl> <span data-ttu-id="828da-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="828da-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="828da-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="828da-135">Library</span></span><br/> | <dl> <span data-ttu-id="828da-136"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="828da-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="828da-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="828da-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="828da-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="828da-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="828da-139">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="828da-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="828da-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="828da-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





