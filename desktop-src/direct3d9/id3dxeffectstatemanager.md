---
description: Essa é uma interface implementada pelo usuário que permite que um usuário defina o estado do dispositivo de um efeito.
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: Interface ID3DXEffectStateManager (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298695"
---
# <a name="id3dxeffectstatemanager-interface"></a><span data-ttu-id="69a70-103">Interface ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="69a70-103">ID3DXEffectStateManager interface</span></span>

<span data-ttu-id="69a70-104">Essa é uma interface implementada pelo usuário que permite que um usuário defina o estado do dispositivo de um efeito.</span><span class="sxs-lookup"><span data-stu-id="69a70-104">This is a user-implemented interface that allows a user to set the device state from an effect.</span></span> <span data-ttu-id="69a70-105">Cada um dos métodos nesta interface deve ser implementado pelo usuário e, em seguida, será usado como retornos de chamada para o aplicativo quando ocorrer uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="69a70-105">Each of the methods in this interface must be implemented by the user and will then be used as callbacks to the application when either of the following occur:</span></span>

-   <span data-ttu-id="69a70-106">Um efeito chama [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="69a70-106">An effect calls [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="69a70-107">O estado do efeito é atualizado dinamicamente chamando a API de alteração de estado apropriada.</span><span class="sxs-lookup"><span data-stu-id="69a70-107">Effect state is dynamically updated by calling the appropriate state change API.</span></span> <span data-ttu-id="69a70-108">Consulte páginas de método individual para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="69a70-108">See individual method pages for details.</span></span>

<span data-ttu-id="69a70-109">Quando um aplicativo usa o Gerenciador de estado para implementar retornos de chamada personalizados, um efeito não salva e restaura automaticamente o estado ao chamar [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md).</span><span class="sxs-lookup"><span data-stu-id="69a70-109">When an application uses the state manager to implement custom callbacks, an effect no longer automatically saves and restores state when calling [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="69a70-110">Como o aplicativo implementou um comportamento personalizado de salvar e restaurar nos retornos de chamada, esse comportamento automático é ignorado.</span><span class="sxs-lookup"><span data-stu-id="69a70-110">Because the application has implemented a custom save and restore behavior in the callbacks, this automatic behavior is bypassed.</span></span>

## <a name="members"></a><span data-ttu-id="69a70-111">Membros</span><span class="sxs-lookup"><span data-stu-id="69a70-111">Members</span></span>

<span data-ttu-id="69a70-112">A interface **ID3DXEffectStateManager** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="69a70-112">The **ID3DXEffectStateManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="69a70-113">**ID3DXEffectStateManager** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="69a70-113">**ID3DXEffectStateManager** also has these types of members:</span></span>

-   [<span data-ttu-id="69a70-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="69a70-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="69a70-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="69a70-115">Methods</span></span>

<span data-ttu-id="69a70-116">A interface **ID3DXEffectStateManager** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="69a70-116">The **ID3DXEffectStateManager** interface has these methods.</span></span>



| <span data-ttu-id="69a70-117">Método</span><span class="sxs-lookup"><span data-stu-id="69a70-117">Method</span></span>                                                                                | <span data-ttu-id="69a70-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="69a70-118">Description</span></span>                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69a70-119">**Clarear**</span><span class="sxs-lookup"><span data-stu-id="69a70-119">**LightEnable**</span></span>](id3dxeffectstatemanager--lightenable.md)                           | <span data-ttu-id="69a70-120">Uma função de retorno de chamada que deve ser implementada por um usuário para habilitar/desabilitar uma luz.</span><span class="sxs-lookup"><span data-stu-id="69a70-120">A callback function that must be implemented by a user to enable/disable a light.</span></span><br/>                                 |
| [<span data-ttu-id="69a70-121">**SetFVF**</span><span class="sxs-lookup"><span data-stu-id="69a70-121">**SetFVF**</span></span>](id3dxeffectstatemanager--setfvf.md)                                     | <span data-ttu-id="69a70-122">Uma função de retorno de chamada que deve ser implementada por um usuário para definir um código FVF.</span><span class="sxs-lookup"><span data-stu-id="69a70-122">A callback function that must be implemented by a user to set a FVF code.</span></span><br/>                                         |
| [<span data-ttu-id="69a70-123">**SetLight**</span><span class="sxs-lookup"><span data-stu-id="69a70-123">**SetLight**</span></span>](id3dxeffectstatemanager--setlight.md)                                 | <span data-ttu-id="69a70-124">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma luz.</span><span class="sxs-lookup"><span data-stu-id="69a70-124">A callback function that must be implemented by a user to set a light.</span></span><br/>                                            |
| [<span data-ttu-id="69a70-125">**SetMaterial**</span><span class="sxs-lookup"><span data-stu-id="69a70-125">**SetMaterial**</span></span>](id3dxeffectstatemanager--setmaterial.md)                           | <span data-ttu-id="69a70-126">Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do material.</span><span class="sxs-lookup"><span data-stu-id="69a70-126">A callback function that must be implemented by a user to set material state.</span></span><br/>                                     |
| [<span data-ttu-id="69a70-127">**SetNPatchMode**</span><span class="sxs-lookup"><span data-stu-id="69a70-127">**SetNPatchMode**</span></span>](id3dxeffectstatemanager--setnpatchmode.md)                       | <span data-ttu-id="69a70-128">Uma função de retorno de chamada que deve ser implementada por um usuário para definir o número de segmentos de subdivisão para N-patches.</span><span class="sxs-lookup"><span data-stu-id="69a70-128">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span><br/>   |
| [<span data-ttu-id="69a70-129">**SetPixelShader**</span><span class="sxs-lookup"><span data-stu-id="69a70-129">**SetPixelShader**</span></span>](id3dxeffectstatemanager--setpixelshader.md)                     | <span data-ttu-id="69a70-130">Uma função de retorno de chamada que deve ser implementada por um usuário para definir um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="69a70-130">A callback function that must be implemented by a user to set a pixel shader.</span></span><br/>                                     |
| [<span data-ttu-id="69a70-131">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="69a70-131">**SetPixelShaderConstantB**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | <span data-ttu-id="69a70-132">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes booleanas do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="69a70-132">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="69a70-133">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="69a70-133">**SetPixelShaderConstantF**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | <span data-ttu-id="69a70-134">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de ponto flutuante do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="69a70-134">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="69a70-135">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="69a70-135">**SetPixelShaderConstantI**</span></span>](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | <span data-ttu-id="69a70-136">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="69a70-136">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |
| [<span data-ttu-id="69a70-137">**Setrenderingstate**</span><span class="sxs-lookup"><span data-stu-id="69a70-137">**SetRenderState**</span></span>](id3dxeffectstatemanager--setrenderstate.md)                     | <span data-ttu-id="69a70-138">Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado de renderização.</span><span class="sxs-lookup"><span data-stu-id="69a70-138">A callback function that must be implemented by a user to set render state.</span></span><br/>                                       |
| [<span data-ttu-id="69a70-139">**Setsamplestate**</span><span class="sxs-lookup"><span data-stu-id="69a70-139">**SetSamplerState**</span></span>](id3dxeffectstatemanager--setsamplerstate.md)                   | <span data-ttu-id="69a70-140">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma amostra.</span><span class="sxs-lookup"><span data-stu-id="69a70-140">A callback function that must be implemented by a user to set a sampler.</span></span><br/>                                          |
| [<span data-ttu-id="69a70-141">**SetTexture**</span><span class="sxs-lookup"><span data-stu-id="69a70-141">**SetTexture**</span></span>](id3dxeffectstatemanager--settexture.md)                             | <span data-ttu-id="69a70-142">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma textura.</span><span class="sxs-lookup"><span data-stu-id="69a70-142">A callback function that must be implemented by a user to set a texture.</span></span><br/>                                          |
| [<span data-ttu-id="69a70-143">**SetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="69a70-143">**SetTextureStageState**</span></span>](id3dxeffectstatemanager--settexturestagestate.md)         | <span data-ttu-id="69a70-144">Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="69a70-144">A callback function that must be implemented by a user to set the texture stage state.</span></span><br/>                            |
| [<span data-ttu-id="69a70-145">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="69a70-145">**SetTransform**</span></span>](id3dxeffectstatemanager--settransform.md)                         | <span data-ttu-id="69a70-146">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma transformação.</span><span class="sxs-lookup"><span data-stu-id="69a70-146">A callback function that must be implemented by a user to set a transform.</span></span><br/>                                        |
| [<span data-ttu-id="69a70-147">**SetVertexShader**</span><span class="sxs-lookup"><span data-stu-id="69a70-147">**SetVertexShader**</span></span>](id3dxeffectstatemanager--setvertexshader.md)                   | <span data-ttu-id="69a70-148">Uma função de retorno de chamada que deve ser implementada por um usuário para definir um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="69a70-148">A callback function that must be implemented by a user to set a vertex shader.</span></span><br/>                                    |
| [<span data-ttu-id="69a70-149">**SetVertexShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="69a70-149">**SetVertexShaderConstantB**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantb.md) | <span data-ttu-id="69a70-150">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes booleanas do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="69a70-150">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="69a70-151">**SetVertexShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="69a70-151">**SetVertexShaderConstantF**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantf.md) | <span data-ttu-id="69a70-152">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de ponto flutuante do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="69a70-152">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="69a70-153">**SetVertexShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="69a70-153">**SetVertexShaderConstantI**</span></span>](id3dxeffectstatemanager--setvertexshaderconstanti.md) | <span data-ttu-id="69a70-154">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="69a70-154">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="69a70-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="69a70-155">Remarks</span></span>

<span data-ttu-id="69a70-156">Um usuário cria uma interface ID3DXEffectStateManager implementando uma classe derivada dessa interface e implementando todos os métodos de interface.</span><span class="sxs-lookup"><span data-stu-id="69a70-156">A user creates an ID3DXEffectStateManager interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span> <span data-ttu-id="69a70-157">Depois que a interface é criada, você pode obter ou definir o Gerenciador de estado dentro de um efeito usando [**ID3DXEffect:: Getstatemanager**](id3dxeffect--getstatemanager.md) e [**ID3DXEffect:: setstatemanager**](id3dxeffect--setstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="69a70-157">Once the interface is created, you can get or set the state manager within an effect using [**ID3DXEffect::GetStateManager**](id3dxeffect--getstatemanager.md) and [**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md).</span></span>

<span data-ttu-id="69a70-158">O tipo LPD3DXEFFECTSTATEMANAGER é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="69a70-158">The LPD3DXEFFECTSTATEMANAGER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a><span data-ttu-id="69a70-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69a70-159">Requirements</span></span>



| <span data-ttu-id="69a70-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="69a70-160">Requirement</span></span> | <span data-ttu-id="69a70-161">Valor</span><span class="sxs-lookup"><span data-stu-id="69a70-161">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="69a70-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69a70-162">Header</span></span><br/>  | <dl> <span data-ttu-id="69a70-163"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="69a70-163"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="69a70-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69a70-164">Library</span></span><br/> | <dl> <span data-ttu-id="69a70-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69a70-165"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="69a70-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="69a70-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69a70-167">Interfaces de efeito</span><span class="sxs-lookup"><span data-stu-id="69a70-167">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
