---
title: Renderização de Multiple-Pass
description: A renderização de várias passagens é um processo no qual um aplicativo atravessa seu grafo de cena várias vezes para produzir uma saída a ser renderizada para a exibição.
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fcf7f3f04bd641fdf82c9cf317e8a2ec99e85c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292390"
---
# <a name="multiple-pass-rendering"></a><span data-ttu-id="52110-103">Renderização de Multiple-Pass</span><span class="sxs-lookup"><span data-stu-id="52110-103">Multiple-Pass Rendering</span></span>

<span data-ttu-id="52110-104">A renderização de várias passagens é um processo no qual um aplicativo atravessa seu grafo de cena várias vezes para produzir uma saída a ser renderizada para a exibição.</span><span class="sxs-lookup"><span data-stu-id="52110-104">Multiple-pass rendering is a process in which an application traverses its scene graph multiple times in order to produce an output to render to the display.</span></span> <span data-ttu-id="52110-105">A renderização de passagem múltipla melhora o desempenho porque divide cenas complexas em tarefas que podem ser executadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="52110-105">Multiple-pass rendering improves performance because it breaks up complex scenes into tasks that can run concurrently.</span></span>

<span data-ttu-id="52110-106">Para executar a renderização de várias passagens, você cria um contexto adiado e uma lista de comandos para cada passagem adicional.</span><span class="sxs-lookup"><span data-stu-id="52110-106">To perform multiple-pass rendering, you create a deferred context and command list for each additional pass.</span></span> <span data-ttu-id="52110-107">Enquanto o aplicativo atravessa o grafo de cena, ele registra comandos (por exemplo, renderização de comandos como [**draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) em um contexto adiado.</span><span class="sxs-lookup"><span data-stu-id="52110-107">While the application traverses the scene graph, it records commands (for example, rendering commands such as [**Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) into a deferred context.</span></span> <span data-ttu-id="52110-108">Depois que o aplicativo termina a passagem, ele chama o método [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) no contexto adiado.</span><span class="sxs-lookup"><span data-stu-id="52110-108">After the application finishes the traversal, it calls the [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) method on the deferred context.</span></span> <span data-ttu-id="52110-109">Por fim, o aplicativo chama o método [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) no contexto imediato para executar os comandos em cada lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="52110-109">Finally, the application calls the [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) method on the immediate context to execute the commands in each command list.</span></span>

<span data-ttu-id="52110-110">O pseudocódigo a seguir mostra como executar a renderização de várias passagens:</span><span class="sxs-lookup"><span data-stu-id="52110-110">The following pseudocode shows how to perform multiple-pass rendering:</span></span>

``` syntax
{
 ImmCtx->SetRenderTarget( pRTViewOfResourceX );
 DefCtx1->SetTexture( pSRView1OfResourceX );
 DefCtx2->SetTexture( pSRView2OfResourceX );

 for () // Traverse the scene graph.
  {
    ImmCtx->Draw(); // Pass 0: immediate context renders primitives into resource X.

    // The following texturing by the deferred contexts occurs after the 
    // immediate context makes calls to ExecuteCommandList. 
    // Resource X is then comletely updated by the immediate context. 
    DefCtx1->Draw(); // Pass 1: deferred context 1 performs texturing from resource X.
    DefCtx2->Draw(); // Pass 2: deferred context 2 performs texturing from resource X.
      }

  // Create command lists and record commands into them.
  DefCtx1->FinishCommandList( &pCL1 ); 
  DefCtx2->FinishCommandList( &pCL2 );

  ImmCtx->ExecuteCommandList( pCL1 ); // Execute pass 1.
  ImmCtx->ExecuteCommandList( pCL2 ); // Exeucte pass 2.
}
```

> [!Note]  
> <span data-ttu-id="52110-111">O contexto imediato modifica um recurso, que é associado ao contexto imediato como uma exibição de destino de renderização (RTV); por outro lado, cada contexto adiado simplesmente usa o recurso, que está associado ao contexto adiado como um modo de exibição de recurso de sombreador (SRV).</span><span class="sxs-lookup"><span data-stu-id="52110-111">The immediate context modifies a resource, which is bound to the immediate context as a render target view (RTV); in contrast, each deferred context simply uses the resource, which is bound to the deferred context as a shader resource view (SRV).</span></span> <span data-ttu-id="52110-112">Para obter mais informações sobre contextos imediatos e adiados, consulte [renderização imediata e adiada](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="52110-112">For more information about immediate and deferred contexts, see [Immediate and Deferred Rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="52110-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52110-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52110-114">Renderização</span><span class="sxs-lookup"><span data-stu-id="52110-114">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




