---
description: Seu aplicativo geralmente renderizará cenas 3D de forma mais realista se ele usar mapas de luz coloridos. Um mapa de luz colorido usa os dados RGB no mapa de luz para saber da iluminação.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Color Light Mapas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbff9fe246131fc90bda8ac9b5f1c49cd2413c412a7b3da5c013b1e936aa6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989296"
---
# <a name="color-light-maps-direct3d-9"></a>Color Light Mapas (Direct3D 9)

Seu aplicativo geralmente renderizará cenas 3D de forma mais realista se ele usar mapas de luz coloridos. Um mapa de luz colorido usa os dados RGB no mapa de luz para saber da iluminação.

O exemplo de código C++ a seguir demonstra o mapeamento de luz com dados de cor RGB.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



Este exemplo define o mapa claro como a primeira textura. Em seguida, ele define o estado do primeiro estágio de mesclagem para modular os dados de textura de entrada. Ele usa a primeira textura e a cor atual do primitivo como argumentos para a operação de modular.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de luz com texturas](light-mapping-with-textures.md)
</dt> </dl>

 

 



