---
description: O blender de buffer de quadro agora pode combinar canais alfa independentes da combinação de canais de cores em destinos de renderização. Esse controle é habilitado com um novo estado de renderização, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Renderizar alfa de destino (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5d4701b2d09334d605cf2c90ef0e03b06ea7886ea875ce8ec8ff9cbc428ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797931"
---
# <a name="render-target-alpha-direct3d-9"></a>Renderizar alfa de destino (Direct3D 9)

O blender de buffer de quadro agora pode combinar canais alfa independentes da combinação de canais de cores em destinos de renderização. Esse controle é habilitado com um novo estado de renderização, D3DRS \_ SEPARATEALPHABLENDENABLE.

Quando D3DRS \_ SEPARATEALPHABLENDENABLE é definido como **FALSE** (que é a condição padrão), os fatores de combinação de destino de renderização e as operações aplicadas ao alfa são os mesmos definidos para combinar canais de cores. Um driver precisa definir o limite D3DPMISCCAPS SEPARATEALPHABLEND para indicar que ele pode dar suporte à combinação alfa de destino \_ de renderização. Certifique-se de habilitar o ALPHABLEND D3DRS \_ para dizer ao pipeline que a combinação alfa é necessária.

Para controlar os fatores no canal alfa dos blenders de destino de renderização, dois novos estados de renderização são definidos da seguinte forma:


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



Assim como os D3DRS SRCBLEND e D3DRS DESTBLEND, eles podem ser definidos como um dos valores na \_ \_ enumeração [**D3DBLEND.**](./d3dblend.md) As configurações de combinação de origem e destino podem ser combinadas de várias maneiras, dependendo das configurações nos membros SrcBlendCaps e DestBlendCaps [**de D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

A combinação alfa é feita da seguinte forma:

renderTargetAlpha = (alfa<sub>em</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)

Em que:

-   alpha<sub>in</sub> é o valor alfa de entrada.
-   srcBlendOp é um dos fatores de combinação em [**D3DBLEND.**](./d3dblend.md)
-   BlendOp é um dos fatores de combinação [**em D3DBLENDOP.**](./d3dblendop.md)
-   alpha<sub>rt</sub> é o valor alfa de destino de renderização.
-   destBlendOp é um dos fatores de combinação em [**D3DBLEND.**](./d3dblend.md)
-   renderTargetAlpha é o valor alfa mesclado final.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Combinação alfa](alpha-blending.md)
</dt> </dl>

 

 
