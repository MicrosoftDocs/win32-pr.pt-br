---
description: O misturador de buffer de quadro agora pode misturar canais alfa independentemente da mistura de canal de cor em destinos de renderização. Esse controle é habilitado com um novo estado de renderização, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Processamento alfa de destino (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500156"
---
# <a name="render-target-alpha-direct3d-9"></a>Processamento alfa de destino (Direct3D 9)

O misturador de buffer de quadro agora pode misturar canais alfa independentemente da mistura de canal de cor em destinos de renderização. Esse controle é habilitado com um novo estado de renderização, D3DRS \_ SEPARATEALPHABLENDENABLE.

Quando D3DRS \_ SEPARATEALPHABLENDENABLE é definido como **false** (que é a condição padrão), os fatores de mesclagem de destino de renderização e as operações aplicadas a Alpha são iguais às definidas para mesclagem de canais de cores. Um driver precisa definir o limite de D3DPMISCCAPS \_ SEPARATEALPHABLEND para indicar que ele pode dar suporte à mesclagem alfa de destino de renderização. Certifique-se de habilitar D3DRS \_ ALPHABLEND para informar ao pipeline que a mistura alfa é necessária.

Para controlar os fatores no canal alfa dos misturadores de destino de renderização, dois novos Estados de renderização são definidos da seguinte maneira:


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



Como o D3DRS \_ SRCBLEND e D3DRS \_ DESTBLEND, eles podem ser definidos como um dos valores na enumeração [**D3DBLEND**](./d3dblend.md) . As configurações de mesclagem de origem e destino podem ser combinadas de várias maneiras, dependendo das configurações nos membros SrcBlendCaps e DestBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

A combinação alfa é feita da seguinte maneira:

renderTargetAlpha = (Alpha<sub>em</sub> \* srcBlendOp) BlendOp (Alpha<sub>RT</sub> \* destBlendOp)

Em que:

-   Alfa<sub>in</sub> é o valor alfa de entrada.
-   srcBlendOp é um dos fatores de mistura em [**D3DBLEND**](./d3dblend.md).
-   BlendOp é um dos fatores de mistura em [**D3DBLENDOP**](./d3dblendop.md).
-   o Alpha<sub>RT</sub> é o valor alfa do destino de renderização.
-   destBlendOp é um dos fatores de mistura em [**D3DBLEND**](./d3dblend.md).
-   renderTargetAlpha é o valor alfa combinado final.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem alfa](alpha-blending.md)
</dt> </dl>

 

 
