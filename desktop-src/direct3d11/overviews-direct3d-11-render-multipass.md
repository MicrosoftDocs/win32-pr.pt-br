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
# <a name="multiple-pass-rendering"></a>Renderização de Multiple-Pass

A renderização de várias passagens é um processo no qual um aplicativo atravessa seu grafo de cena várias vezes para produzir uma saída a ser renderizada para a exibição. A renderização de passagem múltipla melhora o desempenho porque divide cenas complexas em tarefas que podem ser executadas simultaneamente.

Para executar a renderização de várias passagens, você cria um contexto adiado e uma lista de comandos para cada passagem adicional. Enquanto o aplicativo atravessa o grafo de cena, ele registra comandos (por exemplo, renderização de comandos como [**draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) em um contexto adiado. Depois que o aplicativo termina a passagem, ele chama o método [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) no contexto adiado. Por fim, o aplicativo chama o método [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) no contexto imediato para executar os comandos em cada lista de comandos.

O pseudocódigo a seguir mostra como executar a renderização de várias passagens:

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
> O contexto imediato modifica um recurso, que é associado ao contexto imediato como uma exibição de destino de renderização (RTV); por outro lado, cada contexto adiado simplesmente usa o recurso, que está associado ao contexto adiado como um modo de exibição de recurso de sombreador (SRV). Para obter mais informações sobre contextos imediatos e adiados, consulte [renderização imediata e adiada](overviews-direct3d-11-render-multi-thread-render.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




