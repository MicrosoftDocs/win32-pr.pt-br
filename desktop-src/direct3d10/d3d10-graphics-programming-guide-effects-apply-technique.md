---
description: Com as constantes, texturas e o estado do sombreador declarados e inicializados, a única coisa que resta fazer é definir o estado do efeito no dispositivo.
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: Aplicar uma técnica (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7cc48c9115dfb81c1688a3a499e24d46cc563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456948"
---
# <a name="apply-a-technique-direct3d-10"></a><span data-ttu-id="3c36d-103">Aplicar uma técnica (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3c36d-103">Apply a Technique (Direct3D 10)</span></span>

<span data-ttu-id="3c36d-104">Com as constantes, texturas e o estado do sombreador declarados e inicializados, a única coisa que resta fazer é definir o estado do efeito no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c36d-104">With the constants, textures, and shader state declared and initialized, the only thing left to do is to set the effect state in the device.</span></span>

## <a name="set-non-shader-state-in-the-device"></a><span data-ttu-id="3c36d-105">Definir o estado de não sombreador no dispositivo</span><span class="sxs-lookup"><span data-stu-id="3c36d-105">Set Non-Shader State in the Device</span></span>

<span data-ttu-id="3c36d-106">Um estado de pipeline não é definido por um efeito.</span><span class="sxs-lookup"><span data-stu-id="3c36d-106">Some pipeline state is not set by an effect.</span></span> <span data-ttu-id="3c36d-107">Por exemplo, limpar um destino de renderização prepara o destino de renderização para dados.</span><span class="sxs-lookup"><span data-stu-id="3c36d-107">For example clearing a render target prepares the render target for data.</span></span> <span data-ttu-id="3c36d-108">Antes de definir o estado de efeito no dispositivo, aqui está um exemplo de limpeza de buffers de saída.</span><span class="sxs-lookup"><span data-stu-id="3c36d-108">Before setting the effect state in the device, here is an example of clearing output buffers.</span></span>


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a><span data-ttu-id="3c36d-109">Definir estado de efeito no dispositivo</span><span class="sxs-lookup"><span data-stu-id="3c36d-109">Set Effect State in the Device</span></span>

<span data-ttu-id="3c36d-110">Definir o estado de efeito é feito aplicando o estado de efeito dentro do loop de processamento.</span><span class="sxs-lookup"><span data-stu-id="3c36d-110">Setting effect state is done by applying the effect state within the render loop.</span></span> <span data-ttu-id="3c36d-111">Isso é feito de fora no.</span><span class="sxs-lookup"><span data-stu-id="3c36d-111">This is done from the outside in.</span></span> <span data-ttu-id="3c36d-112">Ou seja, selecione uma técnica e, em seguida, defina o estado de cada uma das passagens (dependendo do resultado desejado).</span><span class="sxs-lookup"><span data-stu-id="3c36d-112">That is, select a technique, and then set the state for each of the passes (depending on your desired result).</span></span>


```
    D3D10_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



<span data-ttu-id="3c36d-113">Um efeito não renderiza nada, ele simplesmente define o estado de efeito para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c36d-113">An effect doesn't render anything, it simply sets effect state to the device.</span></span> <span data-ttu-id="3c36d-114">O código de renderização é chamado após o estado do efeito atualizar o estado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c36d-114">The rendering code is called after the effect state updates device state.</span></span> <span data-ttu-id="3c36d-115">Neste exemplo, a chamada DrawIndexed executa a renderização.</span><span class="sxs-lookup"><span data-stu-id="3c36d-115">In this example, the DrawIndexed call performs the rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c36d-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c36d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c36d-117">Renderizando um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3c36d-117">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



