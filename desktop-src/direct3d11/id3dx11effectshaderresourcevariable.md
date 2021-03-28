---
title: Interface ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Uma interface de recurso de sombreador acessa um recurso de sombreador.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- Interface ID3DX11EffectShaderResourceVariable Direct3D 11
- Interface ID3DX11EffectShaderResourceVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abfc2bf29bf3ea5333bf9e7da6630a62c5747aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989420"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a><span data-ttu-id="7920f-105">Interface ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="7920f-105">ID3DX11EffectShaderResourceVariable interface</span></span>

<span data-ttu-id="7920f-106">Uma interface de recurso de sombreador acessa um recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7920f-106">A shader-resource interface accesses a shader resource.</span></span>

## <a name="members"></a><span data-ttu-id="7920f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7920f-107">Members</span></span>

<span data-ttu-id="7920f-108">A interface **ID3DX11EffectShaderResourceVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="7920f-108">The **ID3DX11EffectShaderResourceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="7920f-109">**ID3DX11EffectShaderResourceVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7920f-109">**ID3DX11EffectShaderResourceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="7920f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7920f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7920f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7920f-111">Methods</span></span>

<span data-ttu-id="7920f-112">A interface **ID3DX11EffectShaderResourceVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7920f-112">The **ID3DX11EffectShaderResourceVariable** interface has these methods.</span></span>



| <span data-ttu-id="7920f-113">Método</span><span class="sxs-lookup"><span data-stu-id="7920f-113">Method</span></span>                                                                           | <span data-ttu-id="7920f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7920f-114">Description</span></span>                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="7920f-115">**GetResource**</span><span class="sxs-lookup"><span data-stu-id="7920f-115">**GetResource**</span></span>](id3dx11effectshaderresourcevariable-getresource.md)           | <span data-ttu-id="7920f-116">Obter um recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7920f-116">Get a shader resource.</span></span><br/>            |
| [<span data-ttu-id="7920f-117">**GetResourceArray**</span><span class="sxs-lookup"><span data-stu-id="7920f-117">**GetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-getresourcearray.md) | <span data-ttu-id="7920f-118">Obtenha uma matriz de recursos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7920f-118">Get an array of shader resources.</span></span><br/> |
| [<span data-ttu-id="7920f-119">**Setresource**</span><span class="sxs-lookup"><span data-stu-id="7920f-119">**SetResource**</span></span>](id3dx11effectshaderresourcevariable-setresource.md)           | <span data-ttu-id="7920f-120">Definir um recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7920f-120">Set a shader resource.</span></span><br/>            |
| [<span data-ttu-id="7920f-121">**SetResourceArray**</span><span class="sxs-lookup"><span data-stu-id="7920f-121">**SetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-setresourcearray.md) | <span data-ttu-id="7920f-122">Defina uma matriz de recursos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7920f-122">Set an array of shader resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7920f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="7920f-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7920f-124">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="7920f-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7920f-125">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="7920f-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7920f-126">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7920f-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7920f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7920f-127">Requirements</span></span>



| <span data-ttu-id="7920f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7920f-128">Requirement</span></span> | <span data-ttu-id="7920f-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7920f-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7920f-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7920f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7920f-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7920f-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7920f-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7920f-132">Library</span></span><br/> | <dl> <span data-ttu-id="7920f-133"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="7920f-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7920f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7920f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7920f-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="7920f-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="7920f-136">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="7920f-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="7920f-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="7920f-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





