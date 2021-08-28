---
description: O teste de tesoura corta pixels que estão fora do retângulo de tesoura, uma subseção retangular definida pelo usuário do destino de renderização.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Teste de tesoura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d44b7670d67e7944e9d6e2587ed0011a6244eecef509495b90c71ff0753073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746507"
---
# <a name="scissor-test-direct3d-9"></a>Teste de tesoura (Direct3D 9)

O teste de tesoura corta pixels que estão fora do retângulo de tesoura, uma subseção retangular definida pelo usuário do destino de renderização.

O retângulo de tesoura pode ser usado para indicar a área do destino de renderização em que o mundo do jogo é desenhado. A área fora do retângulo é rebaixada e pode ser dedicada à GUI de um jogo. O teste de tesoura não pode refutar áreas não retangulares.

Retângulos de tesoura não podem ser definidos maiores do que o destino de renderização, mas podem ser definidos maiores do que o viewport.

O retângulo de tesoura é gerenciado por um estado de renderização do dispositivo. Um teste de tesoura é habilitado ou desabilitado definindo o renderstate **como TRUE** ou **FALSE.** Esse teste é executado depois que a cor do fragmento é calculada, mas antes do teste alfa. [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) redefine o retângulo de tesoura para o destino de renderização completo, análogo à redefinição do viewport. [**IDirect3DDevice9::SetScissorRect**](/windows/desktop/api) é registrado por stateblocks e [**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) com a configuração de todos os estados (valor D3DSBT \_ ALL em [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)). O teste de tesoura também afeta a [**operação IDirect3DDevice9::Clear do**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) dispositivo.


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



O retângulo de tesoura padrão é o viewport completo.

O teste de tesoura é feito logo após o processamento de pixel ser concluído por um sombreador de pixel ou pelo pipeline de funções fixas, conforme mostrado no diagrama a seguir.

![diagrama de quando o teste de tesoura é executado em relação a outras etapas](images/scissor-test.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 
