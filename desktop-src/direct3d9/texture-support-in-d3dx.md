---
description: Saiba mais sobre o suporte à textura no D3DX. D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Suporte à textura no D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f31a597ddcab317477d31e0d833c9da96f71ed4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404599"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a>Suporte à textura no D3DX (Direct3D 9)

D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente Direct3D.

## <a name="textures"></a>Texturas

Há suporte para muitas texturas diferentes nos tópicos a seguir.

-   Suporte à textura mapeada padrão. Consulte [Geração automática de Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).
-   Suporte ao mapa de cubo. Consulte [Mapeamento de ambiente cúbica (Direct3D 9)](cubic-environment-mapping.md).
-   Suporte à textura de volume. Consulte [Recursos de textura de volume (Direct3D 9)](volume-texture-resources.md).
-   Suporte ao mapeamento de ambiente. Consulte [Mapeamento de ambiente (Direct3D 9)](environment-mapping.md).
-   Suporte ao mapeamento de aumento. Consulte [Mapeamento de aumento (Direct3D 9)](bump-mapping.md).

### <a name="texture-color-conversion"></a>Conversão de cor de textura

Ao usar qualquer uma das funções D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx ou D3DXCreateVolumeTexturexxx, a conversão de cores pode precisar ser executada. Por exemplo, uma superfície pode ser do tipo RGBA e a outra pode ser UVWQ. Para casos de formatos diferentes, a sequência de conversão é a seguinte:

### <a name="mapping-rgba-to-uvwq"></a>Mapeando RGBA para UVWQ

-   R <-> U, o canal R é mapeado para o canal U ou vice-versa.
-   G <-> V, o canal G é mapeado para o canal V ou vice-versa.
-   B <-> W, o canal B é mapeado para o canal W ou vice-versa.
-   Um <-> P/L, um canal é mapeado para o canal Q ou L (dependendo de qual está disponível no formato de destino) ou vice-versa.


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a>Mapeando UV para RGBA

-   U <-> R, o canal U é mapeado para o canal R ou vice-versa.
-   V <-> G, o canal V é mapeado para o canal G ou vice-versa.
-   1 <-> B, 1 é mapeado para o canal B ou vice-versa.
-   1 <-> A, 1 é mapeado para o canal A ou vice-versa.

Se um canal não existir na origem, supõe-se que seja 1 (com exceção de A8, em que R,G,B é presumido como 0). Por exemplo:


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[D3dx](d3dx.md)
</dt> </dl>

 

 



