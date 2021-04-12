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
# <a name="apply-a-technique-direct3d-10"></a>Aplicar uma técnica (Direct3D 10)

Com as constantes, texturas e o estado do sombreador declarados e inicializados, a única coisa que resta fazer é definir o estado do efeito no dispositivo.

## <a name="set-non-shader-state-in-the-device"></a>Definir o estado de não sombreador no dispositivo

Um estado de pipeline não é definido por um efeito. Por exemplo, limpar um destino de renderização prepara o destino de renderização para dados. Antes de definir o estado de efeito no dispositivo, aqui está um exemplo de limpeza de buffers de saída.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Definir estado de efeito no dispositivo

Definir o estado de efeito é feito aplicando o estado de efeito dentro do loop de processamento. Isso é feito de fora no. Ou seja, selecione uma técnica e, em seguida, defina o estado de cada uma das passagens (dependendo do resultado desejado).


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



Um efeito não renderiza nada, ele simplesmente define o estado de efeito para o dispositivo. O código de renderização é chamado após o estado do efeito atualizar o estado do dispositivo. Neste exemplo, a chamada DrawIndexed executa a renderização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizando um efeito (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



