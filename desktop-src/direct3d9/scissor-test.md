---
description: O teste de tesoura escolhe os pixels que estão fora do retângulo da mola, uma subseção retangular definida pelo usuário do destino de renderização.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Teste de tesoura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105763510"
---
# <a name="scissor-test-direct3d-9"></a><span data-ttu-id="2d06a-103">Teste de tesoura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2d06a-103">Scissor Test (Direct3D 9)</span></span>

<span data-ttu-id="2d06a-104">O teste de tesoura escolhe os pixels que estão fora do retângulo da mola, uma subseção retangular definida pelo usuário do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="2d06a-104">The scissor test culls pixels that are outside of the scissor rectangle, a user-defined rectangular sub-section of the render target.</span></span>

<span data-ttu-id="2d06a-105">O retângulo de mola pode ser usado para indicar a área do destino de renderização onde o mundo do jogo é desenhado.</span><span class="sxs-lookup"><span data-stu-id="2d06a-105">The scissor rectangle could be used to indicate the area of the render target where the game world is drawn.</span></span> <span data-ttu-id="2d06a-106">A área fora do retângulo é reescolheda e pode ser dedicada à GUI de um jogo.</span><span class="sxs-lookup"><span data-stu-id="2d06a-106">The area outside the rectangle is culled and could be devoted to a game's GUI.</span></span> <span data-ttu-id="2d06a-107">O teste de tesoura não pode selecionar áreas não retangulares.</span><span class="sxs-lookup"><span data-stu-id="2d06a-107">The scissor test cannot cull non-rectangular areas.</span></span>

<span data-ttu-id="2d06a-108">Retângulos de recorte não podem ser definidos com maior que o destino de renderização, mas podem ser definidos com maior do que o visor.</span><span class="sxs-lookup"><span data-stu-id="2d06a-108">Scissor rectangles cannot be set larger than the render target, but they can be set larger than the viewport.</span></span>

<span data-ttu-id="2d06a-109">O retângulo da mola é gerenciado por um estado de processamento do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2d06a-109">The scissor rectangle is managed by a device render state.</span></span> <span data-ttu-id="2d06a-110">Um teste de tesoura é habilitado ou desabilitado definindo-se o RenderState como **verdadeiro** ou **falso**.</span><span class="sxs-lookup"><span data-stu-id="2d06a-110">A scissor test is enabled or disabled by setting the renderstate to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="2d06a-111">Esse teste é executado depois que a cor do fragmento é computada, mas antes do teste alfa.</span><span class="sxs-lookup"><span data-stu-id="2d06a-111">This test is performed after the fragment color is computed but before alpha testing.</span></span> <span data-ttu-id="2d06a-112">[**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) redefine o retângulo de mola para o destino de processamento completo, análogo à redefinição do visor.</span><span class="sxs-lookup"><span data-stu-id="2d06a-112">[**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) resets the scissor rectangle to the full render target, analogous to the viewport reset.</span></span> <span data-ttu-id="2d06a-113">[**IDirect3DDevice9:: SetScissorRect**](/windows/desktop/api) é registrado por Stateblocks e [**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) com a configuração de todos os Estados (D3DSBT \_ todos os valores em [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span><span class="sxs-lookup"><span data-stu-id="2d06a-113">[**IDirect3DDevice9::SetScissorRect**](/windows/desktop/api) is recorded by stateblocks, and [**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) with the all state setting (D3DSBT\_ALL value in [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span></span> <span data-ttu-id="2d06a-114">O teste de tesoura também afeta a operação [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2d06a-114">The scissor test also affects the device [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) operation.</span></span>


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



<span data-ttu-id="2d06a-115">O retângulo de tesoura padrão é o visor completo.</span><span class="sxs-lookup"><span data-stu-id="2d06a-115">The default scissor rectangle is the full viewport.</span></span>

<span data-ttu-id="2d06a-116">O teste de recorte é feito logo após o processamento de pixel ser concluído por um sombreador de pixel ou pelo pipeline de função fixo, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d06a-116">Scissor testing is done just after pixel processing is completed by a pixel shader or the fixed function pipeline, as shown in the following diagram.</span></span>

![diagrama de quando o teste de tesoura é executado em relação a outras etapas](images/scissor-test.png)

## <a name="related-topics"></a><span data-ttu-id="2d06a-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d06a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d06a-119">Pipeline de pixel</span><span class="sxs-lookup"><span data-stu-id="2d06a-119">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
