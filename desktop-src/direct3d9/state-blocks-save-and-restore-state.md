---
description: Um bloco de estado é um grupo de Estados de dispositivo.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: Estado de salvamento e restauração de blocos de estado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8f19d6409e0dc9c40f1d4c7711440a0dc09fe2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919691"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a><span data-ttu-id="93247-103">Estado de salvamento e restauração de blocos de estado (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="93247-103">State Blocks Save and Restore State (Direct3D 9)</span></span>

<span data-ttu-id="93247-104">Um bloco de estado é um grupo de Estados de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93247-104">A state block is a group of device states.</span></span> <span data-ttu-id="93247-105">O estado do dispositivo é composto de estado de renderização, estado de vértice, estado de pixel ou todos os itens acima.</span><span class="sxs-lookup"><span data-stu-id="93247-105">Device state is made up of render state, vertex state, pixel state, or all of the above.</span></span> <span data-ttu-id="93247-106">Um bloco de estado contém um instantâneo do estado atual de um dispositivo ou você pode criar um bloco de estado que registra cada alteração de estado que seu aplicativo faz.</span><span class="sxs-lookup"><span data-stu-id="93247-106">A state block contains a snapshot of a device's current state, or you can create a state block that records each state change that your application makes.</span></span>

## <a name="capture-a-block-of-state"></a><span data-ttu-id="93247-107">Capturar um bloco de estado</span><span class="sxs-lookup"><span data-stu-id="93247-107">Capture a Block of State</span></span>

<span data-ttu-id="93247-108">Escolha o tipo de estado que você deseja capturar e crie um bloco de estado como este:</span><span class="sxs-lookup"><span data-stu-id="93247-108">Choose the type of state that you want to capture, and create a state block like this:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



<span data-ttu-id="93247-109">[**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) cria um bloco de estado e captura automaticamente o estado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93247-109">[**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) creates a state block, and automatically captures the device state.</span></span> <span data-ttu-id="93247-110">O estado do dispositivo é especificado pelo tipo de bloco de estado no primeiro argumento.</span><span class="sxs-lookup"><span data-stu-id="93247-110">The device state is specified by the state block type in the first argument.</span></span> <span data-ttu-id="93247-111">Esse Estado pode ser um dos seguintes: todo o estado do dispositivo (consulte [salvar todos os Estados do dispositivo com um StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), todo o estado de pixel (consulte [economizando estado de pixel com um StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)) ou todo o estado de vértice (consulte [salvar Estados de vértice com um StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="93247-111">This state can be one of the following: all device state (see [Saving All Device States with a StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), all pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)), or all vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>

<span data-ttu-id="93247-112">O sistema de efeitos usa um bloco de estado para salvar o estado.</span><span class="sxs-lookup"><span data-stu-id="93247-112">The effect system uses a state block to save state.</span></span> <span data-ttu-id="93247-113">Após [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) ser chamado, um bloco de estado é criado e o estado é capturado.</span><span class="sxs-lookup"><span data-stu-id="93247-113">After [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called, a state block is created and state is captured.</span></span> <span data-ttu-id="93247-114">Quando [**ID3DXEffect:: End**](id3dxeffect--end.md) é chamado, o estado do bloco de estado é reaplicado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93247-114">When [**ID3DXEffect::End**](id3dxeffect--end.md) is called, the state block state is reapplied to the device.</span></span>

## <a name="capture-individual-states"></a><span data-ttu-id="93247-115">Capturar Estados individuais</span><span class="sxs-lookup"><span data-stu-id="93247-115">Capture Individual States</span></span>

<span data-ttu-id="93247-116">Para salvar uma sequência de estado Personalizada, empacote o estado que você deseja salvar em um par [**IDirect3DDevice9:: BeginStateBlock**](/windows/desktop/api) e [**IDirect3DDevice9:: EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) .</span><span class="sxs-lookup"><span data-stu-id="93247-116">To save a custom state sequence, wrap the state that you want to save in a [**IDirect3DDevice9::BeginStateBlock**](/windows/desktop/api) and [**IDirect3DDevice9::EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) pair.</span></span> <span data-ttu-id="93247-117">BeginStateBlock informa ao dispositivo atual para configurar um bloco de estado e adicioná-lo a cada alteração de estado que ocorre até que EndStateBlock seja chamado.</span><span class="sxs-lookup"><span data-stu-id="93247-117">BeginStateBlock tells the current device to set up a state block and add to it every state change that occurs until EndStateBlock is called.</span></span> <span data-ttu-id="93247-118">Veja um exemplo:</span><span class="sxs-lookup"><span data-stu-id="93247-118">Here's an example:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



<span data-ttu-id="93247-119">Isso irá salvar qualquer número de alterações de estado em qualquer sequência para um stateblock personalizado.</span><span class="sxs-lookup"><span data-stu-id="93247-119">This will save any number of state changes in any sequence to a custom stateblock.</span></span> <span data-ttu-id="93247-120">Posteriormente, quando você quiser usar o stateblock para redefinir o estado do dispositivo, chame [**IDirect3DStateBlock9:: apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span><span class="sxs-lookup"><span data-stu-id="93247-120">Later, when you want to use the stateblock to reset the device state, call [**IDirect3DStateBlock9::Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span></span> <span data-ttu-id="93247-121">Isso substituirá apenas o estado do dispositivo que foi capturado no bloco de estado.</span><span class="sxs-lookup"><span data-stu-id="93247-121">This will overwrite only the device state that has been captured in the state block.</span></span> <span data-ttu-id="93247-122">Qualquer outro Estado de dispositivo que não foi capturado com o stateblock personalizado não será alterado.</span><span class="sxs-lookup"><span data-stu-id="93247-122">Any other device state that was not captured with the custom stateblock will not be changed.</span></span> <span data-ttu-id="93247-123">Mais uma vez, como o objeto stateblock é uma interface, você precisará liberá-lo quando terminar.</span><span class="sxs-lookup"><span data-stu-id="93247-123">Once again, since the stateblock object is an interface, you will need to release it when you are done with it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93247-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93247-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93247-125">Estados (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="93247-125">States (Direct3D 9)</span></span>](states.md)
</dt> </dl>

 

 
