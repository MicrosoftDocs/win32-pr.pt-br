---
title: Aplicar uma técnica (Direct3D 11)
description: Com as constantes, texturas e o estado do sombreador declarados e inicializados, a única coisa que resta fazer é definir o estado do efeito no dispositivo.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e67668b27c1f0271974f20edc62619a7b1ae8ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005607"
---
# <a name="apply-a-technique-direct3d-11"></a>Aplicar uma técnica (Direct3D 11)

Com as constantes, texturas e o estado do sombreador declarados e inicializados, a única coisa que resta fazer é definir o estado do efeito no dispositivo.

## <a name="set-non-shader-state-in-the-device"></a>Definir o estado de não sombreador no dispositivo

Um estado de pipeline não é definido por um efeito. Por exemplo, limpar um destino de renderização prepara o destino de renderização para dados. Antes de definir o estado de efeito no dispositivo, aqui está um exemplo de limpeza de buffers de saída.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Definir estado de efeito no dispositivo

Definir o estado de efeito é feito aplicando o estado de efeito dentro do loop de processamento. Isso é feito de fora no. Ou seja, selecione uma técnica e, em seguida, defina o estado de cada uma das passagens (dependendo do resultado desejado).


```
    D3D11_TECHNIQUE_DESC techDesc;
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

[Renderizando um efeito (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




