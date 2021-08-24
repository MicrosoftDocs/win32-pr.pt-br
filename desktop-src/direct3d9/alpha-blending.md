---
description: Saiba mais sobre a combinação alfa. A combinação alfa é usada para exibir uma imagem que tem pixels transparentes ou semi transparentes.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Combinação alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081c194b9eae85dca5599f2bf9f779d1cd896c8a37641df5105bb049b4a5bc22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751576"
---
# <a name="alpha-blending-direct3d-9"></a>Combinação alfa (Direct3D 9)

A combinação alfa é usada para exibir uma imagem que tem pixels transparentes ou semi transparentes. Além de um canal de cores vermelho, verde e azul, cada pixel em um bitmap alfa tem um componente de transparência conhecido como seu canal alfa. O canal alfa normalmente contém tantos bits quanto um canal de cores. Por exemplo, um canal alfa de 8 bits pode representar 256 níveis de transparência, de 0 (o pixel inteiro é transparente) a 255 (o pixel inteiro é opaco). A lista a seguir mostra alguns efeitos especiais que você pode criar usando a combinação alfa.

A cor pode ser definida com ou sem valores alfa. A cor sem alfa é A cor RGB com alfa é armazenada como ARGB. Dados de vértice, dados de material e dados de textura podem ser usados para dar transparência ao objeto. O buffer de quadro também pode ser usado para gerar efeitos de transparência.

-   [Vértice Alfa (Direct3D 9)](vertex-alpha.md)
-   [Material Alfa (Direct3D 9)](material-alpha.md)
-   [Alfa de textura (Direct3D 9)](texture-alpha.md)
-   [Buffer de quadro alfa (Direct3D 9)](frame-buffer-alpha.md)
-   [Renderizar alfa de destino (Direct3D 9)](render-target-alpha.md)

Exemplos que demonstram alfa incluem:

-   [Minguação (Direct3D 9)](billboarding.md)
-   [Nuvens, Smoke e Trails DeIa (Direct3D 9)](clouds--smoke--and-vapor-trails.md)
-   [Incêndio, incêndios e explosão (Direct3D 9)](fire--flares--and-explosions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct3D Rendering](direct3d-rendering.md)
</dt> </dl>

 

 



