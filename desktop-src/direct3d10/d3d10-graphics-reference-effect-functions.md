---
description: 'Esta seção contém informações sobre as seguintes funções de efeito:'
ms.assetid: b76643f0-387f-49c6-80e5-4d7b406b4db7
title: Funções de efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111fdcb34bbf1d9a86a295e62f734938991dda99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501000"
---
# <a name="effect-functions-direct3d-10"></a><span data-ttu-id="9340d-103">Funções de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="9340d-103">Effect Functions (Direct3D 10)</span></span>

<span data-ttu-id="9340d-104">Esta seção contém informações sobre as seguintes funções de efeito:</span><span class="sxs-lookup"><span data-stu-id="9340d-104">This section contains information about the following effect functions:</span></span>



| <span data-ttu-id="9340d-105">Funções</span><span class="sxs-lookup"><span data-stu-id="9340d-105">Functions</span></span>                                                                      | <span data-ttu-id="9340d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="9340d-106">Description</span></span>                                                         |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="9340d-107">**D3D10CompileEffectFromMemory**</span><span class="sxs-lookup"><span data-stu-id="9340d-107">**D3D10CompileEffectFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)           | <span data-ttu-id="9340d-108">Compile um efeito.</span><span class="sxs-lookup"><span data-stu-id="9340d-108">Compile an effect.</span></span>                                                  |
| [<span data-ttu-id="9340d-109">**D3D10CreateEffectFromMemory**</span><span class="sxs-lookup"><span data-stu-id="9340d-109">**D3D10CreateEffectFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createeffectfrommemory)             | <span data-ttu-id="9340d-110">Crie um efeito.</span><span class="sxs-lookup"><span data-stu-id="9340d-110">Create an effect.</span></span>                                                   |
| [<span data-ttu-id="9340d-111">**D3D10CreateEffectPoolFromMemory**</span><span class="sxs-lookup"><span data-stu-id="9340d-111">**D3D10CreateEffectPoolFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createeffectpoolfrommemory)     | <span data-ttu-id="9340d-112">Crie um pool de efeitos.</span><span class="sxs-lookup"><span data-stu-id="9340d-112">Create an effect pool.</span></span>                                              |
| [<span data-ttu-id="9340d-113">**D3D10CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="9340d-113">**D3D10CreateStateBlock**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createstateblock)                         | <span data-ttu-id="9340d-114">Crie um bloco de estado.</span><span class="sxs-lookup"><span data-stu-id="9340d-114">Create a state block.</span></span>                                               |
| [<span data-ttu-id="9340d-115">**D3D10DisassembleEffect**</span><span class="sxs-lookup"><span data-stu-id="9340d-115">**D3D10DisassembleEffect**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10disassembleeffect)                       | <span data-ttu-id="9340d-116">Desmonte um efeito compilado nas instruções do assembly do sombreador.</span><span class="sxs-lookup"><span data-stu-id="9340d-116">Disassemble a compiled effect into shader assembly instructions.</span></span>    |
| [<span data-ttu-id="9340d-117">**D3D10StateBlockMaskDifference**</span><span class="sxs-lookup"><span data-stu-id="9340d-117">**D3D10StateBlockMaskDifference**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdifference)         | <span data-ttu-id="9340d-118">Combine duas máscaras de bloco de estado com um XOR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="9340d-118">Combine two state-block masks with a bitwise XOR.</span></span>                   |
| [<span data-ttu-id="9340d-119">**D3D10StateBlockMaskDisableAll**</span><span class="sxs-lookup"><span data-stu-id="9340d-119">**D3D10StateBlockMaskDisableAll**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdisableall)         | <span data-ttu-id="9340d-120">Desabilitar captura de estado.</span><span class="sxs-lookup"><span data-stu-id="9340d-120">Disable state capturing.</span></span>                                            |
| [<span data-ttu-id="9340d-121">**D3D10StateBlockMaskDisableCapture**</span><span class="sxs-lookup"><span data-stu-id="9340d-121">**D3D10StateBlockMaskDisableCapture**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdisablecapture) | <span data-ttu-id="9340d-122">Desabilite a captura de estado com uma máscara de bloco de estado.</span><span class="sxs-lookup"><span data-stu-id="9340d-122">Disable state capturing with a state-block mask.</span></span>                    |
| [<span data-ttu-id="9340d-123">**D3D10StateBlockMaskEnableAll**</span><span class="sxs-lookup"><span data-stu-id="9340d-123">**D3D10StateBlockMaskEnableAll**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskenableall)           | <span data-ttu-id="9340d-124">Habilite uma máscara de bloco de estado para capturar e aplicar todas as variáveis de estado.</span><span class="sxs-lookup"><span data-stu-id="9340d-124">Enable a state-block mask to capture and apply all state variables.</span></span> |
| [<span data-ttu-id="9340d-125">**D3D10StateBlockMaskEnableCapture**</span><span class="sxs-lookup"><span data-stu-id="9340d-125">**D3D10StateBlockMaskEnableCapture**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskenablecapture)   | <span data-ttu-id="9340d-126">Habilite um intervalo de valores de estado em uma máscara de bloco de estado.</span><span class="sxs-lookup"><span data-stu-id="9340d-126">Enable a range of state values in a state block mask.</span></span>               |
| [<span data-ttu-id="9340d-127">**D3D10StateBlockMaskGetSetting**</span><span class="sxs-lookup"><span data-stu-id="9340d-127">**D3D10StateBlockMaskGetSetting**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskgetsetting)         | <span data-ttu-id="9340d-128">Obter um elemento em uma máscara de bloco de estado.</span><span class="sxs-lookup"><span data-stu-id="9340d-128">Get an element in a state-block mask.</span></span>                               |
| [<span data-ttu-id="9340d-129">**D3D10StateBlockMaskIntersect**</span><span class="sxs-lookup"><span data-stu-id="9340d-129">**D3D10StateBlockMaskIntersect**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskintersect)           | <span data-ttu-id="9340d-130">Combine duas máscaras de bloco de estado com um AND bit a bit.</span><span class="sxs-lookup"><span data-stu-id="9340d-130">Combine two state-block masks with a bitwise AND.</span></span>                   |
| [<span data-ttu-id="9340d-131">**D3D10StateBlockMaskUnion**</span><span class="sxs-lookup"><span data-stu-id="9340d-131">**D3D10StateBlockMaskUnion**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskunion)                   | <span data-ttu-id="9340d-132">Combine duas máscaras de bloco de estado com um OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="9340d-132">Combine two state-block masks with a bitwise OR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="9340d-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9340d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9340d-134">Referência de efeito</span><span class="sxs-lookup"><span data-stu-id="9340d-134">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



