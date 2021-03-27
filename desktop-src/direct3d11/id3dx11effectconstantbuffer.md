---
title: Interface ID3DX11EffectConstantBuffer (D3dx11effect. h)
description: Uma interface de buffer constante acessa buffers constantes ou buffers de textura.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- Interface ID3DX11EffectConstantBuffer Direct3D 11
- Interface ID3DX11EffectConstantBuffer Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298700"
---
# <a name="id3dx11effectconstantbuffer-interface"></a><span data-ttu-id="2bc93-105">Interface ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="2bc93-105">ID3DX11EffectConstantBuffer interface</span></span>

<span data-ttu-id="2bc93-106">Uma interface de buffer constante acessa buffers constantes ou buffers de textura.</span><span class="sxs-lookup"><span data-stu-id="2bc93-106">A constant-buffer interface accesses constant buffers or texture buffers.</span></span>

## <a name="members"></a><span data-ttu-id="2bc93-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2bc93-107">Members</span></span>

<span data-ttu-id="2bc93-108">A interface **ID3DX11EffectConstantBuffer** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="2bc93-108">The **ID3DX11EffectConstantBuffer** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="2bc93-109">**ID3DX11EffectConstantBuffer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2bc93-109">**ID3DX11EffectConstantBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="2bc93-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2bc93-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2bc93-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2bc93-111">Methods</span></span>

<span data-ttu-id="2bc93-112">A interface **ID3DX11EffectConstantBuffer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2bc93-112">The **ID3DX11EffectConstantBuffer** interface has these methods.</span></span>



| <span data-ttu-id="2bc93-113">Método</span><span class="sxs-lookup"><span data-stu-id="2bc93-113">Method</span></span>                                                                             | <span data-ttu-id="2bc93-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2bc93-114">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="2bc93-115">**GetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="2bc93-115">**GetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-getconstantbuffer.md)         | <span data-ttu-id="2bc93-116">Obtenha um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="2bc93-116">Get a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="2bc93-117">**GetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="2bc93-117">**GetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-gettexturebuffer.md)           | <span data-ttu-id="2bc93-118">Obter um buffer de textura.</span><span class="sxs-lookup"><span data-stu-id="2bc93-118">Get a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="2bc93-119">**SetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="2bc93-119">**SetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-setconstantbuffer.md)         | <span data-ttu-id="2bc93-120">Definir um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="2bc93-120">Set a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="2bc93-121">**SetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="2bc93-121">**SetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-settexturebuffer.md)           | <span data-ttu-id="2bc93-122">Defina um buffer de textura.</span><span class="sxs-lookup"><span data-stu-id="2bc93-122">Set a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="2bc93-123">**UndoSetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="2bc93-123">**UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | <span data-ttu-id="2bc93-124">Reverte um buffer de constante definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2bc93-124">Reverts a previously set constant buffer.</span></span><br/> |
| [<span data-ttu-id="2bc93-125">**UndoSetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="2bc93-125">**UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | <span data-ttu-id="2bc93-126">Reverte um buffer de textura definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2bc93-126">Reverts a previously set texture buffer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="2bc93-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bc93-127">Remarks</span></span>

<span data-ttu-id="2bc93-128">Usar buffers de constantes para armazenar muitas constantes de efeito; Agrupamento de constantes em buffers com base em sua frequência de atualização.</span><span class="sxs-lookup"><span data-stu-id="2bc93-128">Use constant buffers to store many effect constants; grouping constants into buffers based on their frequency of update.</span></span> <span data-ttu-id="2bc93-129">Isso permite minimizar o número de alterações de estado, bem como fazer com que as menores chamadas à API mudem de estado.</span><span class="sxs-lookup"><span data-stu-id="2bc93-129">This allows you to minimize the number of state changes as well as make the fewest API calls to change state.</span></span> <span data-ttu-id="2bc93-130">Esses dois fatores levam a um melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="2bc93-130">Both of these factors lead to better performance.</span></span>

> [!Note]  
> <span data-ttu-id="2bc93-131">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="2bc93-131">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2bc93-132">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="2bc93-132">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2bc93-133">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2bc93-133">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2bc93-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bc93-134">Requirements</span></span>



| <span data-ttu-id="2bc93-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bc93-135">Requirement</span></span> | <span data-ttu-id="2bc93-136">Valor</span><span class="sxs-lookup"><span data-stu-id="2bc93-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc93-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2bc93-137">Header</span></span><br/>  | <dl> <span data-ttu-id="2bc93-138"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bc93-138"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2bc93-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2bc93-139">Library</span></span><br/> | <dl> <span data-ttu-id="2bc93-140"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="2bc93-140"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bc93-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bc93-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc93-142">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="2bc93-142">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="2bc93-143">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="2bc93-143">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2bc93-144">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="2bc93-144">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





