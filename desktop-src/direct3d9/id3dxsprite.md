---
description: A interface ID3DXSprite fornece um conjunto de métodos que simplificam o processo de desenho de sprites usando o Microsoft Direct3D.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: Interface ID3DXSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3703132cd8a0f7744119d9b8cb5d9d48f260094c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837947"
---
# <a name="id3dxsprite-interface"></a><span data-ttu-id="3145a-103">Interface ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="3145a-103">ID3DXSprite interface</span></span>

<span data-ttu-id="3145a-104">A interface ID3DXSprite fornece um conjunto de métodos que simplificam o processo de desenho de sprites usando o Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3145a-104">The ID3DXSprite interface provides a set of methods that simplify the process of drawing sprites using Microsoft Direct3D.</span></span>

## <a name="members"></a><span data-ttu-id="3145a-105">Membros</span><span class="sxs-lookup"><span data-stu-id="3145a-105">Members</span></span>

<span data-ttu-id="3145a-106">A interface **ID3DXSprite** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3145a-106">The **ID3DXSprite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3145a-107">**ID3DXSprite** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3145a-107">**ID3DXSprite** also has these types of members:</span></span>

-   [<span data-ttu-id="3145a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3145a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3145a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="3145a-109">Methods</span></span>

<span data-ttu-id="3145a-110">A interface **ID3DXSprite** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3145a-110">The **ID3DXSprite** interface has these methods.</span></span>



| <span data-ttu-id="3145a-111">Método</span><span class="sxs-lookup"><span data-stu-id="3145a-111">Method</span></span>                                                | <span data-ttu-id="3145a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3145a-112">Description</span></span>                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3145a-113">**Começar**</span><span class="sxs-lookup"><span data-stu-id="3145a-113">**Begin**</span></span>](id3dxsprite--begin.md)                   | <span data-ttu-id="3145a-114">Prepara um dispositivo para desenhar sprites.</span><span class="sxs-lookup"><span data-stu-id="3145a-114">Prepares a device for drawing sprites.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="3145a-115">**Draw**</span><span class="sxs-lookup"><span data-stu-id="3145a-115">**Draw**</span></span>](id3dxsprite--draw.md)                     | <span data-ttu-id="3145a-116">Adiciona um Sprite à lista de sprites em lote.</span><span class="sxs-lookup"><span data-stu-id="3145a-116">Adds a sprite to the list of batched sprites.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="3145a-117">**Completo**</span><span class="sxs-lookup"><span data-stu-id="3145a-117">**End**</span></span>](id3dxsprite--end.md)                       | <span data-ttu-id="3145a-118">Chama [**ID3DXSprite:: flush**](id3dxsprite--flush.md) e restaura o estado do dispositivo para como ele estava antes de [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) foi chamado.</span><span class="sxs-lookup"><span data-stu-id="3145a-118">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span><br/>                                            |
| [<span data-ttu-id="3145a-119">**Liberar**</span><span class="sxs-lookup"><span data-stu-id="3145a-119">**Flush**</span></span>](id3dxsprite--flush.md)                   | <span data-ttu-id="3145a-120">Força a envio de todos os sprites em lotes para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3145a-120">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="3145a-121">Os Estados do dispositivo permanecem como estavam após a última chamada para [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="3145a-121">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="3145a-122">A lista de sprites em lote é desmarcada.</span><span class="sxs-lookup"><span data-stu-id="3145a-122">The list of batched sprites is then cleared.</span></span><br/> |
| [<span data-ttu-id="3145a-123">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="3145a-123">**GetDevice**</span></span>](id3dxsprite--getdevice.md)           | <span data-ttu-id="3145a-124">Recupera o dispositivo associado ao objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="3145a-124">Retrieves the device associated with the sprite object.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="3145a-125">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="3145a-125">**GetTransform**</span></span>](id3dxsprite--gettransform.md)     | <span data-ttu-id="3145a-126">Obtém a transformação de Sprite.</span><span class="sxs-lookup"><span data-stu-id="3145a-126">Gets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="3145a-127">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="3145a-127">**OnLostDevice**</span></span>](id3dxsprite--onlostdevice.md)     | <span data-ttu-id="3145a-128">Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks.</span><span class="sxs-lookup"><span data-stu-id="3145a-128">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="3145a-129">Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3145a-129">This method should be called whenever a device is lost or before resetting a device.</span></span><br/>                              |
| [<span data-ttu-id="3145a-130">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="3145a-130">**OnResetDevice**</span></span>](id3dxsprite--onresetdevice.md)   | <span data-ttu-id="3145a-131">Use este método para readquirir recursos e salvar o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="3145a-131">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="3145a-132">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="3145a-132">**SetTransform**</span></span>](id3dxsprite--settransform.md)     | <span data-ttu-id="3145a-133">Define a transformação Sprite.</span><span class="sxs-lookup"><span data-stu-id="3145a-133">Sets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="3145a-134">**SetWorldViewLH**</span><span class="sxs-lookup"><span data-stu-id="3145a-134">**SetWorldViewLH**</span></span>](id3dxsprite--setworldviewlh.md) | <span data-ttu-id="3145a-135">Define a transformação de exibição Mundial da mão esquerda para um Sprite.</span><span class="sxs-lookup"><span data-stu-id="3145a-135">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="3145a-136">Uma chamada para esse método é necessária antes de obter ou classificar sprites.</span><span class="sxs-lookup"><span data-stu-id="3145a-136">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                 |
| [<span data-ttu-id="3145a-137">**SetWorldViewRH**</span><span class="sxs-lookup"><span data-stu-id="3145a-137">**SetWorldViewRH**</span></span>](id3dxsprite--setworldviewrh.md) | <span data-ttu-id="3145a-138">Define a transformação de exibição Mundial da mão direita para um Sprite.</span><span class="sxs-lookup"><span data-stu-id="3145a-138">Sets the right-handed world-view transform for a sprite.</span></span> <span data-ttu-id="3145a-139">Uma chamada para esse método é necessária antes de obter ou classificar sprites.</span><span class="sxs-lookup"><span data-stu-id="3145a-139">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="3145a-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="3145a-140">Remarks</span></span>

<span data-ttu-id="3145a-141">A interface **ID3DXSprite** é obtida chamando a função [**D3DXCreateSprite**](d3dxcreatesprite.md) .</span><span class="sxs-lookup"><span data-stu-id="3145a-141">The **ID3DXSprite** interface is obtained by calling the [**D3DXCreateSprite**](d3dxcreatesprite.md) function.</span></span>

<span data-ttu-id="3145a-142">Normalmente, o aplicativo primeiro chama [**ID3DXSprite:: Begin**](id3dxsprite--begin.md), que permite o controle sobre o estado de renderização do dispositivo, a mistura alfa e a transformação e classificação de Sprite.</span><span class="sxs-lookup"><span data-stu-id="3145a-142">The application typically first calls [**ID3DXSprite::Begin**](id3dxsprite--begin.md), which allows control over the device render state, alpha blending, and sprite transformation and sorting.</span></span> <span data-ttu-id="3145a-143">Em seguida, para cada sprite a ser exibido, chame [**ID3DXSprite::D RAW**](id3dxsprite--draw.md).</span><span class="sxs-lookup"><span data-stu-id="3145a-143">Then for each sprite to be displayed, call [**ID3DXSprite::Draw**](id3dxsprite--draw.md).</span></span> <span data-ttu-id="3145a-144">**ID3DXSprite::D RAW** pode ser chamado repetidamente para armazenar qualquer número de sprites.</span><span class="sxs-lookup"><span data-stu-id="3145a-144">**ID3DXSprite::Draw** can be called repeatedly to store any number of sprites.</span></span> <span data-ttu-id="3145a-145">Para exibir os sprites em lote para o dispositivo, chame [**ID3DXSprite:: End**](id3dxsprite--end.md) ou [**ID3DXSprite:: flush**](id3dxsprite--flush.md).</span><span class="sxs-lookup"><span data-stu-id="3145a-145">To display the batched sprites to the device, call [**ID3DXSprite::End**](id3dxsprite--end.md) or [**ID3DXSprite::Flush**](id3dxsprite--flush.md).</span></span>

<span data-ttu-id="3145a-146">O tipo LPD3DXSPRITE é definido como um ponteiro para a interface **ID3DXSprite** .</span><span class="sxs-lookup"><span data-stu-id="3145a-146">The LPD3DXSPRITE type is defined as a pointer to the **ID3DXSprite** interface.</span></span>


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a><span data-ttu-id="3145a-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3145a-147">Requirements</span></span>



| <span data-ttu-id="3145a-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="3145a-148">Requirement</span></span> | <span data-ttu-id="3145a-149">Valor</span><span class="sxs-lookup"><span data-stu-id="3145a-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3145a-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3145a-150">Header</span></span><br/>  | <dl> <span data-ttu-id="3145a-151"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3145a-151"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3145a-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3145a-152">Library</span></span><br/> | <dl> <span data-ttu-id="3145a-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3145a-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3145a-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="3145a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3145a-155">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="3145a-155">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
