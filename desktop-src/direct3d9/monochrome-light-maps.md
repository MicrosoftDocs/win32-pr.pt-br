---
description: Algumas placas aceleradoras 3D mais antigas não oferecem suporte à mesclagem de textura com o valor de alfa do pixel de destino.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Mapas de luz monocromática (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac6f62aaba08ac6c8e1116a0bc5059fed3dea19da51d83b034bfae79653ed5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728233"
---
# <a name="monochrome-light-maps-direct3d-9"></a>Mapas de luz monocromática (Direct3D 9)

Algumas placas aceleradoras 3D mais antigas não oferecem suporte à mesclagem de textura com o valor de alfa do pixel de destino. Consulte [mesclagem de textura alfa (Direct3D 9)](alpha-texture-blending.md) para obter mais informações. Em geral, esses adaptadores também não oferecem suporte à mistura de múltipla textura. Se o app for executado em um adaptador desse tipo, ele pode usar a mistura da textura de passagem múltipla para executar o mapeamento de luzes monocromáticas.

Para executar o mapeamento de luzes monocromáticas, um app armazena as informações de iluminação nos dados de alfa das texturas de mapa de luzes. O app usa os recursos de filtragem de textura do Direct3D para realizar um mapeamento de cada pixel na imagem do primitivo para um texel correspondente no mapa de luz. Ele define o fator de mesclagem de origem para o valor de alfa do texel correspondente.

O exemplo a seguir ilustra como um aplicativo pode usar uma textura como um mapa claro monocromático:


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



Como os adaptadores de vídeo que não dão suporte à mesclagem alfa de destino normalmente não dão suporte a várias mesclagens de textura, este exemplo define o mapa claro como a primeira textura, que está disponível em todas as placas aceleradoras 3D. O código de exemplo define a operação de cor para o estágio de mesclagem da textura para misturar os dados de textura com a cor existente do primitivo. Em seguida, ele seleciona a primeira textura e a cor existente do primitivo como os dados de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento claro com texturas](light-mapping-with-textures.md)
</dt> </dl>

 

 



