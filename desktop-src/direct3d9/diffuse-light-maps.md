---
description: Quando exibidas por uma fonte de luz, as superfícies fosco exibem reflexão difusa de luz.
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: Luz difusa Mapas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758fc2b5054a30bf8df703941b3cedf0810c378a5fb459d8c5783bb295ff9abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044444"
---
# <a name="diffuse-light-maps-direct3d-9"></a>Luz difusa Mapas (Direct3D 9)

Quando exibidas por uma fonte de luz, as superfícies fosco exibem reflexão difusa de luz. O brilho da luz difusa depende da distância da fonte de luz e do ângulo entre a superfície normal e o vetor de direção da fonte de luz. Os efeitos de iluminação difusa simulados com cálculos de iluminação produzem apenas efeitos gerais.

Seu aplicativo pode simular uma iluminação difusa mais complexa com mapas de luz de textura. Faça isso adicionando o mapa de luz difuso à textura base, conforme mostrado no exemplo de código C++ a seguir.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexDiffuseLightMap is a valid pointer to a texture that contains 
// RGB diffuse light map data.

// Set the base texture.
d3dDevice->SetTexture(0,lptexBaseTexture );

// Set the base texture operation and args.
d3dDevice->SetTextureStageState(0,D3DTSS_COLOROP,
                                D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the diffuse light map.
d3dDevice->SetTexture(1,lptexDiffuseLightMap );

// Set the blend stage.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de luz com texturas](light-mapping-with-textures.md)
</dt> </dl>

 

 



