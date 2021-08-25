---
title: Aplicar uma técnica (Direct3D 11)
description: Saiba como definir o estado de efeito no dispositivo para o Direct3D 11 depois que as constantes, texturas e o estado do sombreador forem declarados e inicializados.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b53eb5f60c80baf69199885f8036a9e92ac1572fe8339bd6d4a96454adb0121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792036"
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

 

 




