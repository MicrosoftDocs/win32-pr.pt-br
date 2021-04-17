---
description: Usado para definir e para efeitos de consulta e para escolher técnicas. Um objeto Effect pode conter várias técnicas para renderizar o mesmo efeito.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: Interface ID3DXEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275376234739964940d70381a34331ff5b89f2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765718"
---
# <a name="id3dxeffect-interface"></a><span data-ttu-id="b958f-104">Interface ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="b958f-104">ID3DXEffect interface</span></span>

<span data-ttu-id="b958f-105">Usado para definir e para efeitos de consulta e para escolher técnicas.</span><span class="sxs-lookup"><span data-stu-id="b958f-105">Used to set and query effects, and to choose techniques.</span></span> <span data-ttu-id="b958f-106">Um objeto Effect pode conter várias técnicas para renderizar o mesmo efeito.</span><span class="sxs-lookup"><span data-stu-id="b958f-106">An effect object can contain multiple techniques to render the same effect.</span></span>

## <a name="members"></a><span data-ttu-id="b958f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b958f-107">Members</span></span>

<span data-ttu-id="b958f-108">A interface **ID3DXEffect** herda de [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="b958f-108">The **ID3DXEffect** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="b958f-109">**ID3DXEffect** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b958f-109">**ID3DXEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="b958f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b958f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b958f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b958f-111">Methods</span></span>

<span data-ttu-id="b958f-112">A interface **ID3DXEffect** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b958f-112">The **ID3DXEffect** interface has these methods.</span></span>



| <span data-ttu-id="b958f-113">Método</span><span class="sxs-lookup"><span data-stu-id="b958f-113">Method</span></span>                                                                | <span data-ttu-id="b958f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b958f-114">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b958f-115">**ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="b958f-115">**ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)       | <span data-ttu-id="b958f-116">Aplique os valores em um bloco de estado ao estado atual do sistema de efeito.</span><span class="sxs-lookup"><span data-stu-id="b958f-116">Apply the values in a state block to the current effect system state.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="b958f-117">**Começar**</span><span class="sxs-lookup"><span data-stu-id="b958f-117">**Begin**</span></span>](id3dxeffect--begin.md)                                   | <span data-ttu-id="b958f-118">Inicia uma técnica ativa.</span><span class="sxs-lookup"><span data-stu-id="b958f-118">Starts an active technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="b958f-119">**BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="b958f-119">**BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)       | <span data-ttu-id="b958f-120">Iniciar a captura de alterações de estado em um bloco de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b958f-120">Start capturing state changes in a parameter block.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="b958f-121">**BeginPass**</span><span class="sxs-lookup"><span data-stu-id="b958f-121">**BeginPass**</span></span>](id3dxeffect--beginpass.md)                           | <span data-ttu-id="b958f-122">Inicia uma passagem, dentro da técnica ativa.</span><span class="sxs-lookup"><span data-stu-id="b958f-122">Begins a pass, within the active technique.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="b958f-123">**CloneEffect**</span><span class="sxs-lookup"><span data-stu-id="b958f-123">**CloneEffect**</span></span>](id3dxeffect--cloneeffect.md)                       | <span data-ttu-id="b958f-124">Cria uma cópia de um efeito.</span><span class="sxs-lookup"><span data-stu-id="b958f-124">Creates a copy of an effect.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="b958f-125">**CommitChanges**</span><span class="sxs-lookup"><span data-stu-id="b958f-125">**CommitChanges**</span></span>](id3dxeffect--commitchanges.md)                   | <span data-ttu-id="b958f-126">Propagar alterações de estado que ocorrem dentro de uma passagem ativa para o dispositivo antes da renderização.</span><span class="sxs-lookup"><span data-stu-id="b958f-126">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span><br/>                                                                                           |
| [<span data-ttu-id="b958f-127">**DeleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="b958f-127">**DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)     | <span data-ttu-id="b958f-128">Excluir um bloco de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b958f-128">Delete a parameter block.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="b958f-129">**Completo**</span><span class="sxs-lookup"><span data-stu-id="b958f-129">**End**</span></span>](id3dxeffect--end.md)                                       | <span data-ttu-id="b958f-130">Termina uma técnica ativa.</span><span class="sxs-lookup"><span data-stu-id="b958f-130">Ends an active technique.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="b958f-131">**EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="b958f-131">**EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)           | <span data-ttu-id="b958f-132">Parar a captura de alterações de estado de parâmetro de efeito.</span><span class="sxs-lookup"><span data-stu-id="b958f-132">Stop capturing effect parameter state changes.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="b958f-133">**Fim da passagem**</span><span class="sxs-lookup"><span data-stu-id="b958f-133">**EndPass**</span></span>](id3dxeffect--endpass.md)                               | <span data-ttu-id="b958f-134">Encerrar uma passagem ativa.</span><span class="sxs-lookup"><span data-stu-id="b958f-134">End an active pass.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="b958f-135">**FindNextValidTechnique**</span><span class="sxs-lookup"><span data-stu-id="b958f-135">**FindNextValidTechnique**</span></span>](id3dxeffect--findnextvalidtechnique.md) | <span data-ttu-id="b958f-136">Pesquisa a próxima técnica válida, começando na técnica após a técnica especificada.</span><span class="sxs-lookup"><span data-stu-id="b958f-136">Searches for the next valid technique, starting at the technique after the specified technique.</span></span><br/>                                                                                       |
| [<span data-ttu-id="b958f-137">**GetCurrentTechnique**</span><span class="sxs-lookup"><span data-stu-id="b958f-137">**GetCurrentTechnique**</span></span>](id3dxeffect--getcurrenttechnique.md)       | <span data-ttu-id="b958f-138">Obtém a técnica atual.</span><span class="sxs-lookup"><span data-stu-id="b958f-138">Gets the current technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="b958f-139">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="b958f-139">**GetDevice**</span></span>](id3dxeffect--getdevice.md)                           | <span data-ttu-id="b958f-140">Recupera o dispositivo associado ao efeito.</span><span class="sxs-lookup"><span data-stu-id="b958f-140">Retrieves the device associated with the effect.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="b958f-141">**GetPool**</span><span class="sxs-lookup"><span data-stu-id="b958f-141">**GetPool**</span></span>](id3dxeffect--getpool.md)                               | <span data-ttu-id="b958f-142">Obtém um ponteiro para o pool de parâmetros compartilhados.</span><span class="sxs-lookup"><span data-stu-id="b958f-142">Gets a pointer to the pool of shared parameters.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="b958f-143">**Getstatemanager**</span><span class="sxs-lookup"><span data-stu-id="b958f-143">**GetStateManager**</span></span>](id3dxeffect--getstatemanager.md)               | <span data-ttu-id="b958f-144">Obtenha o Gerenciador de estado do efeito.</span><span class="sxs-lookup"><span data-stu-id="b958f-144">Get the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="b958f-145">**IsParameterUsed**</span><span class="sxs-lookup"><span data-stu-id="b958f-145">**IsParameterUsed**</span></span>](id3dxeffect--isparameterused.md)               | <span data-ttu-id="b958f-146">Determina se um parâmetro é usado pela técnica.</span><span class="sxs-lookup"><span data-stu-id="b958f-146">Determines if a parameter is used by the technique.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="b958f-147">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="b958f-147">**OnLostDevice**</span></span>](id3dxeffect--onlostdevice.md)                     | <span data-ttu-id="b958f-148">Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks.</span><span class="sxs-lookup"><span data-stu-id="b958f-148">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="b958f-149">Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b958f-149">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="b958f-150">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="b958f-150">**OnResetDevice**</span></span>](id3dxeffect--onresetdevice.md)                   | <span data-ttu-id="b958f-151">Use este método para readquirir recursos e salvar o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="b958f-151">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="b958f-152">**SetRawValue**</span><span class="sxs-lookup"><span data-stu-id="b958f-152">**SetRawValue**</span></span>](id3dxeffect--setrawvalue.md)                       | <span data-ttu-id="b958f-153">Defina um intervalo contíguo de constantes de sombreador com uma cópia de memória.</span><span class="sxs-lookup"><span data-stu-id="b958f-153">Set a contiguous range of shader constants with a memory copy.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="b958f-154">**Setstatemanager**</span><span class="sxs-lookup"><span data-stu-id="b958f-154">**SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)               | <span data-ttu-id="b958f-155">Defina o Gerenciador de estado do efeito.</span><span class="sxs-lookup"><span data-stu-id="b958f-155">Set the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="b958f-156">**Settécnica**</span><span class="sxs-lookup"><span data-stu-id="b958f-156">**SetTechnique**</span></span>](id3dxeffect--settechnique.md)                     | <span data-ttu-id="b958f-157">Define a técnica ativa.</span><span class="sxs-lookup"><span data-stu-id="b958f-157">Sets the active technique.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="b958f-158">**ValidateTechnique**</span><span class="sxs-lookup"><span data-stu-id="b958f-158">**ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)           | <span data-ttu-id="b958f-159">Valide uma técnica.</span><span class="sxs-lookup"><span data-stu-id="b958f-159">Validate a technique.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="b958f-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="b958f-160">Remarks</span></span>

<span data-ttu-id="b958f-161">A interface ID3DXEffect é obtida chamando [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)ou [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span><span class="sxs-lookup"><span data-stu-id="b958f-161">The ID3DXEffect interface is obtained by calling [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md), or [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span></span>

<span data-ttu-id="b958f-162">O tipo LPD3DXEFFECT é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="b958f-162">The LPD3DXEFFECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a><span data-ttu-id="b958f-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b958f-163">Requirements</span></span>



| <span data-ttu-id="b958f-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="b958f-164">Requirement</span></span> | <span data-ttu-id="b958f-165">Valor</span><span class="sxs-lookup"><span data-stu-id="b958f-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b958f-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b958f-166">Header</span></span><br/>  | <dl> <span data-ttu-id="b958f-167"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b958f-167"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b958f-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b958f-168">Library</span></span><br/> | <dl> <span data-ttu-id="b958f-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b958f-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b958f-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="b958f-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b958f-171">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="b958f-171">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="b958f-172">Interfaces de efeito</span><span class="sxs-lookup"><span data-stu-id="b958f-172">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b958f-173">**D3DXCreateEffect**</span><span class="sxs-lookup"><span data-stu-id="b958f-173">**D3DXCreateEffect**</span></span>](d3dxcreateeffect.md)
</dt> <dt>

[<span data-ttu-id="b958f-174">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="b958f-174">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> <dt>

[<span data-ttu-id="b958f-175">**D3DXCreateEffectFromResource**</span><span class="sxs-lookup"><span data-stu-id="b958f-175">**D3DXCreateEffectFromResource**</span></span>](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




