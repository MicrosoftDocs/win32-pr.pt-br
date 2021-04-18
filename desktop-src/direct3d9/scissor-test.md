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
# <a name="scissor-test-direct3d-9"></a>Teste de tesoura (Direct3D 9)

O teste de tesoura escolhe os pixels que estão fora do retângulo da mola, uma subseção retangular definida pelo usuário do destino de renderização.

O retângulo de mola pode ser usado para indicar a área do destino de renderização onde o mundo do jogo é desenhado. A área fora do retângulo é reescolheda e pode ser dedicada à GUI de um jogo. O teste de tesoura não pode selecionar áreas não retangulares.

Retângulos de recorte não podem ser definidos com maior que o destino de renderização, mas podem ser definidos com maior do que o visor.

O retângulo da mola é gerenciado por um estado de processamento do dispositivo. Um teste de tesoura é habilitado ou desabilitado definindo-se o RenderState como **verdadeiro** ou **falso**. Esse teste é executado depois que a cor do fragmento é computada, mas antes do teste alfa. [**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) redefine o retângulo de mola para o destino de processamento completo, análogo à redefinição do visor. [**IDirect3DDevice9:: SetScissorRect**](/windows/desktop/api) é registrado por Stateblocks e [**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) com a configuração de todos os Estados (D3DSBT \_ todos os valores em [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)). O teste de tesoura também afeta a operação [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) do dispositivo.


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



O retângulo de tesoura padrão é o visor completo.

O teste de recorte é feito logo após o processamento de pixel ser concluído por um sombreador de pixel ou pelo pipeline de função fixo, conforme mostrado no diagrama a seguir.

![diagrama de quando o teste de tesoura é executado em relação a outras etapas](images/scissor-test.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de pixel](pixel-pipeline.md)
</dt> </dl>

 

 
