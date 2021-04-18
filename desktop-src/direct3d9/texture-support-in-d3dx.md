---
description: D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente do Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Suporte a textura em D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9c8d6da498a47d14fe57ca770ba96a6852ae41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105764437"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a>Suporte a textura em D3DX (Direct3D 9)

D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente do Direct3D.

## <a name="textures"></a>Texturas

Há suporte para várias texturas diferentes nos tópicos a seguir.

-   Suporte a textura padrão do mipmapped. Consulte [geração automática de mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).
-   Suporte ao mapa do cubo. Consulte [mapeamento de ambiente cúbico (Direct3D 9)](cubic-environment-mapping.md).
-   Suporte a textura de volume. Consulte [recursos de textura de volume (Direct3D 9)](volume-texture-resources.md).
-   Suporte a mapeamento de ambiente. Consulte [mapeamento de ambiente (Direct3D 9)](environment-mapping.md).
-   Suporte ao mapeamento de relevo. Consulte [mapeamento de relevo (Direct3D 9)](bump-mapping.md).

### <a name="texture-color-conversion"></a>Conversão de cores de textura

Ao usar qualquer uma das funções D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx ou D3DXCreateVolumeTexturexxx, talvez seja necessário executar a conversão de cores. Por exemplo, uma superfície pode ser do tipo RGBA e a outra pode ser UVWQ. Para casos de formatos diferentes, a sequência de conversão é a seguinte:

### <a name="mapping-rgba-to-uvwq"></a>Mapeando RGBA para UVWQ

-   R <-> U, o canal R é mapeado para o canal U ou vice-versa.
-   G <-> V, G Channel é mapeado para o canal V ou vice-versa.
-   B <-> W, o canal B é mapeado para o canal W ou vice-versa.
-   R <-> Q/L, um canal é mapeado para o canal Q ou L (dependendo de qual está disponível no formato de destino) ou vice-versa.


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a>Mapeamento de UV para RGBA

-   U <-> R, o canal U é mapeado para o canal R ou vice-versa.
-   V <-> G, V Channel é mapeado para o canal G, ou vice-versa.
-   1 <-> B, 1 é mapeado para o canal B ou vice-versa.
-   1 <-> A, 1 é mapeado para um canal, ou vice-versa.

Se um canal não existir na origem, será considerado 1 (com exceção de A8, em que R, G, B será considerado 0). Por exemplo:


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



